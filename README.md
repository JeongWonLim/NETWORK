## IP (Internet Procotol)

### Network ID 와 Host ID

## IP Class
IpV4 기준 각 8바이트씩 옥텟으로 끊어져 총 4개로 이루어져있다. 그러므로 총 사용 가능한 IP수는 0~ 2^32 개이다.

### 탄생배경
초창기 IP주소를 설계할 때 40억개 정도면 충분하다고 생각했지만 현재 많은 인류가 네트워크로 연결된 기기를 사용하게 되므로써 IP를 개별적으로 모두 부여할 수 없게 되었다. 대안으로 IPv6라는 대안이 나오기는 하였지만 네트워크 인프라는 이미 IPv4로 구성되어 있었기 때문에 이를 효과적으로 활용할 수 있는 방안을 도입하기 위해 **클래스**의 개념이 등장하였다.

### NetworkID 와 HostID
네트워크 클래스의 개념이 생기면서 IP를 NetworkID 부분과 HostID 부분으로 나누게 되었는데, NetworkID는 라우터에서 라우터 사이로 라우팅 하는 과정에서 사용되며 HostID는 라우터 내의 연결된 Host를 찾는다.


### A Class
IP주소의 첫 비트가 0인 클래스, 0.0.0.0 ~ 127.0.0.0 까지 사용할 수 있다. 네트워크 ID는 앞 8 비트 호스트 ID는 나머지 24비틑 사용하게 된다. 그러므로 호스트는 총 2^24개인 16,777,214 개만큼 호스트의 수로 사용할 수 있다.  
일반적으로 ISP 네트워크처럼 큰 네트워크 주소로 사용될 때 사용한다.

### B Class
IP주소의 첫 비트가 1인 클래스, 128.0.0.0 ~ 191.255.0.0 가지 사용할 수 있다. 네트워크 ID는 앞 16비트, 호스트ID는 나머지 16비트를 사용하게 된다. 호스트는 총 2^16개인 65,534 개만큼 호스트의 수로 사용가능하다.
중간 정도의 네트워크 주소로 사용된다. 조직 

### C Class
IP의 첫 주소가 110인 클래스, 192.0.0.0 ~ 223.255.255.0 까지 사용가능하다. 네트워크ID는 앞 24비트, 호스트ID는 나머지 8비트로 사용하게 된다. 호스트는 총 2^8 개인 254 개만큼 호스트의 수로 사용가능하다.
작은 네트워크에서 사용된다

### D Class
224.0.0.0 ~ 239.255.255.255 일반 IP주소로는 사용 불가하다. 멀티캐슽트를 위해서 존재하는 네트워크
* 멀티캐스트 : 한 번의 메시지 송신으로 특정 네트워크 안에 있는 여러 컴퓨터에게 전송할 수 있도록 하는 기술
멀티캐스팅

### E Class
240.0.0.0 ~ 255.255.255.255 일반 IP주소로 사용 불가능하다. 이미 예약된 주소로 미래에 사용될 용도로 구분해 놓은 네트워크이다.

### 현재 시점
현재 시점에서는 IP를 클래스 형태로 나눠서 사용하지 않는다. 호스트의 수가 너무 낭비 될 수 있다는 이유에서 사용하지는 않고 현재는 클래스가 없는 CIDR 기법을 적용하여 사용중이다.


