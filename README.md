# Overall Comparison of the Performance Loss of Virtualization 

In this repository you will find all relevant files for a research project into Overall Comparison of the Performance Loss of Virtualization, done by Alexander Blaauwgeers & Kotaiba Alachkar in November 2017, for [Large Systems](https://www.os3.nl/2017-2018/courses/ls/start) course.


### Bash Script

#### ab4_hw.sh

```
#!/bin/bash
clear
echo "Start of experiment No. 4"
for i in {1..25}
	do
	echo "Round $i"
	echo "=== Round $i ===" >> abresult_hw.txt
	ab -n 1000 -c 100 -g abresult_hw_$i.tsv "http://app.hw.os5.nl/oscommerce/catalog/" >> abresult_hw.txt
	sleep 1
	done
	vim abresult_hw.txt -c "hardcopy > abresult_hw.pdf | q"
echo "Result has been saved."
```

#### ab3_vm.sh

```
#!/bin/bash
clear
echo "The script starts soon."
for i in {1..1}
	do
	echo "Round $i"
	echo "=== Round $i ===" >> abresult_vm.txt
	ab -n 10000 -c 100 -g abresult_vm_$i.tsv "http://app.vm.os5.nl/oscommerce/catalog/" >> abresult_vm.txt
	sleep 1
	done
	vim abresult_vm.txt -c "hardcopy > abresult_vm.pdf | q"
echo "The script is finished"
```

#### ab4_hw.sh

```
#!/bin/bash
clear
echo "The script starts soon."
for i in {1..10}
	do
	echo "Round $i"
	echo "=== Round $i ===" >> abresult_hw.txt
	ab -n 1000 -c 100 -g abresult_hw_$i.tsv "http://app.hw.os5.nl/oscommerce/catalog/" >> abresult_hw.txt
	sleep 1
	done
	vim abresult_hw.txt -c "hardcopy > abresult_hw.pdf | q"
echo "The script is finished"
```

#### ab3_vm.sh

```
#!/bin/bash
clear
echo "The script starts soon."
for i in {1..10}
	do
	echo "Round $i"
	echo "=== Round $i ===" >> abresult_vm.txt
	ab -n 1000 -c 100 -g abresult_vm_$i.tsv "http://app.vm.os5.nl/oscommerce/catalog/" >> abresult_vm.txt
	sleep 1
	done
	vim abresult_vm.txt -c "hardcopy > abresult_vm.pdf | q"
echo "The script is finished"
```

### GNUplot

#### DSK 1 HW

```
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_1.png" 
set  title  "Benchmark testing hw1webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_1.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_2.png" 
set  title  "Benchmark testing hw2webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_2.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_3.png" 
set  title  "Benchmark testing hw3webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_3.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_4.png" 
set  title  "Benchmark testing hw4webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_4.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_5.png" 
set  title  "Benchmark testing hw5webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_5.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_6.png" 
set  title  "Benchmark testing hw6webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_6.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_7.png" 
set  title  "Benchmark testing hw7webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_7.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_8.png" 
set  title  "Benchmark testing hw8webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_8.tsv"  every  :: 2  using  5  title  'response time' with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_9.png" 
set  title  "Benchmark testing hw9webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_9.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_10.png" 
set  title  "Benchmark testing hw10webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_10.tsv"  every  :: 2  using  5  title  'response time' with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_11.png" 
set  title  "Benchmark testing hw11webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_11.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_12.png" 
set  title  "Benchmark testing hw12webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_12.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_13.png" 
set  title  "Benchmark testing hw13webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_13.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_14.png" 
set  title  "Benchmark testing hw14webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_14.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_15.png" 
set  title  "Benchmark testing hw15webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_15.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_16.png" 
set  title  "Benchmark testing hw16webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_16.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_17.png" 
set  title  "Benchmark testing hw17webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_17.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_18.png" 
set  title  "Benchmark testing hw18webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_18.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_19.png" 
set  title  "Benchmark testing hw19webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_19.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_20.png" 
set  title  "Benchmark testing hw20webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_20.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_21.png" 
set  title  "Benchmark testing hw21webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_21.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_22.png" 
set  title  "Benchmark testing hw22webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_22.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_23.png" 
set  title  "Benchmark testing hw23webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_23.tsv"  every  :: 2  using  5  title  'response time' with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_hw_24.png" 
set  title  "Benchmark testing hw24webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_hw_24.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_hw_25.png" 
set  title  "Benchmark testing hw25webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_hw_25.tsv"  every  :: 2  using  5  title  "response time" with  lines
```


### DSK 2 VM

```
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_1.png" 
set  title  "Benchmark testing vm1webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_1.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_2.png" 
set  title  "Benchmark testing vm2webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_2.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_3.png" 
set  title  "Benchmark testing vm3webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_3.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_4.png" 
set  title  "Benchmark testing vm4webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_4.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_5.png" 
set  title  "Benchmark testing vm5webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_5.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_6.png" 
set  title  "Benchmark testing vm6webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_6.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_7.png" 
set  title  "Benchmark testing vm7webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_7.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_8.png" 
set  title  "Benchmark testing vm8webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_8.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_9.png" 
set  title  "Benchmark testing vm9webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_9.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_10.png" 
set  title  "Benchmark testing vm10webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_10.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_11.png" 
set  title  "Benchmark testing vm11webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_11.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_12.png" 
set  title  "Benchmark testing vm12webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_12.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_13.png" 
set  title  "Benchmark testing vm13webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_13.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_14.png" 
set  title  "Benchmark testing vm14webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_14.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_15.png" 
set  title  "Benchmark testing vm15webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_15.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_16.png" 
set  title  "Benchmark testing vm16webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_16.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_17.png" 
set  title  "Benchmark testing vm17webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_17.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_18.png" 
set  title  "Benchmark testing vm18webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_18.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_19.png" 
set  title  "Benchmark testing vm19webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_19.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_20.png" 
set  title  "Benchmark testing vm20webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_20.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_21.png" 
set  title  "Benchmark testing vm21webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_21.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_22.png" 
set  title  "Benchmark testing vm22webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_22.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_23.png" 
set  title  "Benchmark testing vm23webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_23.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  1 
set  output  "abresult_vm_24.png" 
set  title  "Benchmark testing vm24webo1" 
set  key  left  top 
set  grid  y 
set  xlabel  'requests' 
set  ylabel  "response time (ms)" 
set  datafile separator ' \ t ' 
plot  "abresult_vm_24.tsv"  every  :: 2  using  5  title  "response time" with  lines
 
set  terminal  png  size  750 , 400 
set  size  1 ,  the first 
set of  output  "abresult_vm_25.png" 
set  title  "Benchmark testing vm25webo1" 
set  key  left  top 
set of  grid  y 
set  xlabel  'requests is 
set  ylabel  "response time (ms)" 
set of  data file separator ' \ t ' 
plot  "abresult_vm_25.tsv"  every  :: 2  using  5  title  "response time" with  lines

```

With help of http://www.bradlanders.com/2013/04/15/apache-bench-and-gnuplot-youre-probably-doing-it-wrong/
