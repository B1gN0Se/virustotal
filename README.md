# Installation 

```sh
git clone https://github.com/b1gn0se/virustotal.git
```

```sh
cd virustotal
```


create a 3 accounts [https://www.virustotal.com/gui/join-us](https://www.virustotal.com/gui/join-us) and copy the 3 api keys ===>

```sh
nano virustotal.sh
```

paste 3 api keys here ....


```sh
  if [ $api_key_index -eq 1 ]; then
    api_key="key-1"
  elif [ $api_key_index -eq 2 ]; then
    api_key="key-2"
  else
    api_key="key-3"
  fi
```

**Ex**

```sh
  if [ $api_key_index -eq 1 ]; then
    api_key="XXXXXXXXXXXXXX1"
  elif [ $api_key_index -eq 2 ]; then
    api_key="XXXXXXXXXXXXXX2"
  else
    api_key="XXXXXXXXXXXXXX3"
  fi
```


**next step**

`chmod +x virustotal.sh` 


# Usage

Create sub domain file `EX` ===> `subdomain.txt`  ===> `wihtout http/s` 

**===>**


```sh
./virustotal.sh subdomain.txt | tee results.txt 
```

**===>**


```sh
cat results.txt | egrep 'http|https' > endpoints.txt
```

