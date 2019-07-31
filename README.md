# statsQ
Mini Stats Language in Q to track Unix Stats

__Compilation of readPid.cpp is__:

`g++ -shared -fPIC -fexceptions readPid.cpp -o $QHOME/libso/readPid.so`

__Compilation of cpu.c is__: 
(From https://code.kx.com/v2/interfaces/using-c-functions/)

`cc -I. -fPIC -shared -o ~/q/libso/cpu.so cpu.c`


### Instructions:

Place the following files under QHOME directory:
1) `Entire libso directory`
2) `d.k`
3) `d.q` 


### Typical Outputs:

Only works for Unix-based systems

```
q)d)a:([] a: til 1000000)
+(,`a)!,0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 2..
time                 | 4
mem                  | 8536816
cpudiff              | 15008888
rchar                | 97
wchar                | 80
syscr                | 2
syscw                | 1
read_bytes           | 0
write_bytes          | 0
cancelled_write_bytes| 0
utime                | 0
stime                | 0
cutime               | 0
cstime               | 0
starttime            | 0
```
`Note:` There's a base of 97 rchar which "seems to be present" due to the implicit cost of running the set of codes above
