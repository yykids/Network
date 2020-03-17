## Network > Release Notes

### 2020. 03. 24.

#### 기능 개선

##### Load Balancer

* Cert Manager 서비스를 통한 인증서 관리기능이 추가 되었습니다.
* Cert Manager 서비스에 인증서를 등록하고 리스너에 해당 인증서를 연결하면 이메일로 인증서 만료일 알람을 받을 수 있습니다.

### Feb. 25, 2020

#### Feature Updates

##### Security Groups

* Added "Description" for the rule of security group. Description can be included for each rule of security group.

### Dec. 24, 2019

#### More Features

##### DNS Plus

* Added GSLB (Global Server Load Balancing) to allow stable load balancing of traffic at an endpoint server.
* The GSLB domain can be configured either, according to routing rules, Disaster Recovery (DR), Random, or Global Load Balancing. 
* The pool serves as a grouping element for endpoint servers at the minimum unit so as to apply the routing rule. 
* Health check is conducted on a regular basis for endpoint servers included to a pool so as to support stable services. Health check is supported for HTTP/HTTPS/TCP. 

#### Feature Updates

##### DNS Plus

* Updated to select user's GSLB domain for CNAME record set type, for creating/updating the record set. 

### Dec. 17. 2019.

#### Feature Updates
* [Korea/Japan/US Region] Every network interface connected with an instance can be assosicated with each floating IP. 

### Oct. 29, 2019.

#### Feature Updates

##### Load Balancer

* Added the feature of notification via web console, for chain certificate registration, when an individual certificate which is included in the certificate file has an invalid format.

### Aug. 27, 2019 

#### Feature Updates 

##### Load Balancer

* It is available to specify TLS version to communicate with clients via TERMINATED_HTTPS load balancer.
    * For more details on the setting of load balancer in TLS version, see [user guide](https://docs.toast.com/en/Network/Load%20Balancer/en/overview/#ssltls-version-for-load-balancer).

##### DNS Plus

* Exceeded the maximum available number of record sets to be created. For each DNS zone, up to 5,000 record sets can be created. 
* Modified, in the query of record set statistics for CNAME, to query A record set type along with AAAA record set type. 

### June 25, 2019

#### Release of New Products

##### DNS Plus

* DNS Plus provides features for domain management.
* It is easy to configure a DNS server.

### May 30, 2019

#### Updates

##### Load Balancer

* [Japan Region] IP access control is available.
    * IP-based access control is available for load balancer.
    * For more details on IP access control, see user guides.

### 2019. 05. 28.

#### 기능 변경

##### VPC

* [한국 리전] 피어링 생성 기능을 다시 사용할 수 있습니다.

### 2019. 04. 25.

#### 기능 개선

##### Load Balancer

* IP 접근제어 기능을 사용할 수 있습니다.
    * IP를 기반으로 한 접근제어 기능을 로드밸런서에서 사용할 수 있습니다.
    * IP 접근제어 기능에 대한 자세한 사항은 사용자가이드 문서를 참고해주세요.
    * 유선으로 설정 요청하신 제어 대상 IP 목록은 Default 라는 이름의 IP 접근제어 그룹에 자동 반영되었습니다.

### 2018. 12. 27.

#### 기능 변경

##### VPC

* 피어링 된 두 VPC 사이의 통신 시 패킷 플러딩이 발생할 가능성이 있어, 당분간 새로운 피어링 생성 기능을 제공하지 않습니다.
	기존에 만들어진 피어링의 통신에는 문제가 없으며 피어링 생성을 제외한 나머지 기능은 그대로 제공됩니다.

### 2018. 11. 27.

#### 버그 수정

##### Load Balancer

* 로드 밸런서에 리스너를 추가 생성하는 경우, 비활성화된 인스턴스에 추가된 인스턴스 멤버가 활성화된채 생성되는 버그를 수정하였습니다.

#### 기능 개선

##### Load Balancer

* 로드밸런싱 통계 기능이 추가되어 다음 통계량이 차트 형식으로 제공됩니다.
    * 세션수, 클라이언트 초당 세션증가량, 인스턴스 초당 세션 증가량, In 트래픽량, Out 트래픽량, 로드밸런싱 제외 개수
    * 삭제된 로드밸런서, 리스너, 멤버에 대한 통계량은 제공되지 않습니다.
    * 트래픽량에는 L2, L3, L4 헤더가 포함되지 않습니다.
    * 자세한 사항은 사용자가이드 문서를 참고해주세요.


### 2018. 09. 20.

#### 버그 수정

##### Load Balancer

* Load Balancer에 Member로 등록된 Instance를 삭제할 때 일부 Listener의 Member가 남아있는 문제를 수정했습니다.

#### 기능 개선

##### Load Balancer

* 전용 로드밸런서 서비스가 추가되었습니다. 
* 전용 로드밸런서는 하드웨어 자원을 선점하여 생성되기에 1Gbps의 대역폭과 48만 동시세션을 지원합니다.

### 2018. 08. 28.

#### 버그 수정

##### VPC

* 라우트가 존재하는 서브넷을 가진 VPC에 대해 삭제를 시도할 수 있는 문제를 수정했습니다.

#### 기능 변경

##### VPC

* 서브넷, 라우팅 테이블, 라우트에 대해 최대 생성 가능 개수를 조정했습니다.
* VPC의 리소스 별 최대 생성 가능 개수는 각 리소스 생성 창의 우측 설명 부분에서 확인하실 수 있습니다.
    * 서브넷: VPC당 10개까지 생성이 가능합니다.
    * 라우팅 테이블: VPC당 10개까지 생성이 가능합니다.
    * 라우트: 라우팅 테이블당 10개까지 생성이 가능합니다.

##### Load Balancer

* TCP, HTTPS 프로토콜을 사용하는 경우 클라이언트의 IP를 알기 위해 Proxy Protocol을 활성화할 수 있습니다.
* Load Balancer의 Keepalive timeout 값을 설정할 수 있습니다.


### 2018. 04. 24.

#### 버그 수정

##### VPC

* 피어링 시 로컬 VPC의 인스턴스에서 피어 VPC의 로드밸런서로 접속이 원활하지 않은 문제를 수정했습니다.

#### 기능 개선

##### VPC

* VPC, 서브넷, 라우팅테이블, 인터넷게이트웨이의 개요 페이지에서 연결된 리소스 정보를 확인할 수 있습니다.

##### Floating IP

* Floating IP 목록에 페이지네이션 기능을 적용했습니다.

##### Security Group

* Rule 편집 기능이 추가되었습니다.

##### Load Balancer

* Keepalive Timeout을 5분으로 변경하였습니다.
* Listener의 세션 제한값을 최대 60,000 까지 설정할 수 있습니다.

### 2018. 03. 22.

#### 버그 수정

##### VPC

* 새로 추가한 서브넷에 인스턴스를 연결하면 DHCP를 통해 IP를 받아오지 못하는 문제를 수정했습니다.
* 라우팅 정책을 추가할 때 기존 라우팅 정책의 타겟과 동일한 타겟을 입력할 수 있는 문제를 수정했습니다.
* Floating IP가 연결된 인스턴스에서 간헐적으로 다른 서브넷에 위치한 인스턴스와 통신이 되지 않는 문제를 수정했습니다.

### 2018. 02. 22.

#### 버그 수정

##### VPC

* Floating IP가 연결된 인스턴스에서 로컬 네트워크로 트래픽이 전달되지 않는 문제를 수정했습니다.

#### 기능 개선

##### Network 기본 모델로 VPC를 도입했습니다.

* 서브넷을 여러개 사용할 수 있습니다.
* 서브넷 단위로 포트를 생성하여 인스턴스에 연결할 수 있습니다.
* 라우팅 정책을 추가할 수 있습니다.
* VPC간 통신을 위해 피어링 기능이 추가되었습니다.
* 인스턴스에 여러 VPC 포트를 추가하거나 삭제할 수 있습니다.
* 자세한 내용은 VPC Overview와 사용자 가이드를 참고해주시기 바랍니다.


### 2017. 11. 23.

#### 버그 수정

##### Load Balancer
* Load Balancer 생성시 리스너의 연결 제한값이 잘못 표기되는 현상을 수정하였습니다.

### 2017. 10. 26.

#### 버그 수정

##### Load Balancer
* Load Balancer 생성시 인증서가 등록되지 않는 버그가 수정되었습니다.

### 2017. 09. 21.

#### 기능 추가

##### Public API 추가

* Object Storage에 이어 Compute&Network 상품을 API를 이용해 관리할 수 있습니다.
* 현재 제한적인 기능만 이용할 수 있으며, 추후 API 추가를 통해 기능이 확장되었습니다.

#### 버그 수정

* Project에 Admin 권한이 없는 사용자가 security group을 수정할 수 없도록 수정되었습니다.
* Project에 Admin 권한이 없는 사용자에게는 Network 메뉴가 노출되지 않도록 수정되었습니다.

### 2017. 08. 24.

#### 버그 수정

##### Load Balancer
* Load Balancer 서비스의 세션 지속성 항목이 제대로 표시되지 않던 버그가 수정되었습니다.

### 2017. 04. 20.

#### 버그 수정
##### Load Balancer
* Listener에 인증서 파일 업로드시 간헐적으로 인증서 등록창이 사라지는 버그가 수정되었습니다.


### 2017. 03. 23.

#### 버그 수정
##### Floating IP
* Floating IP 연결 팝업에서 "생성" 버튼이 노출되지 않는 문제가 수정되었습니다.


### 2017. 02. 23.

#### 기능 개선/변경

##### Load Balancer

* 로드밸런서에 등록된 리스너가 1개일 경우 삭제할 수 없다는 것을 알리도록 변경합니다.
	  * 기존에도 삭제가 되지 않았으나 사용자에게 별다른 알림이 없어 혼동을 주었습니다.
	  * 이제 사용자에게 명시적으로 삭제할 수 없다고 메시지를 공지하도록 변경합니다.

##### Floating IP

* Floating IP 삭제 시 인스턴스 혹은 로드밸런서가 연결되어 있을 경우 삭제 할 수 없도록 변경합니다.
	  * 기존에는 인스턴스나 로드밸런서가 연결되어 있는 Floating IP를 삭제할 수 있어 서비스에 장애를 일으킬 수 있었습니다.
	  * 이런 실수를 미연에 방지할 수 있도록 연결이 있는 Floating IP는 삭제할 수 없도록 변경합니다.
* 명칭변경 : '포트' -> '네트워크 인터페이스'
	  * 인스턴스에 Floating IP를 붙일 때 대상이 되는 명칭을 기존 “포트”에서 “네트워크 인터페이스”로 변경합니다.


### 2017. 01. 19.

#### 버그 수정
##### Load Balancer
* Load Balancer 생성시 연결 제한 설정이 적용되지 않는 문제를 수정하였습니다.



### 2016. 12. 22.

#### 버그 수정

##### Load Balancer
* Health Check Protocol이 TCP인 경우 Listener 내용 수정이 안되는 문제를 수정하였습니다.

##### Floating IP
* Floating IP에 연결된 Load Balancer의 이름이 노출되지 않는 문제를 수정하였습니다.

##### Security Group
* 중복된 Rule 추가 시 Security Group 목록이 사라지는 문제를 수정하였습니다.






### 2016. 12. 08.

#### 버그 수정

##### Load Balancer
* Load Balancer의 Heath check url이 미노출되는 문제를 수정하였습니다.
* Listener 수정 버튼 클릭시 기등록한 Health Check URL이 아닌 "/"로 노출되는 문제를 수정하였습니다.








### 2016. 11. 29.

#### 버그 수정
##### Load Balancer
* TERMINATED_HTTPS type의 Load Balancer 생성이 실패하던 문제를 수정하였습니다.



### 2016. 11. 24.

#### 기능 개선/변경
##### Load Balancer
* Load Balancer의 Listener별 세션 제한 값을 노출하도록 변경하였습니다.

#### 버그 수정
##### Load Balancer
* 특정 Project에서 Load Balancer 생성 실패하던 문제를 수정하였습니다.



### 2016. 08. 04.

#### 기능 개선/변경
##### Load Balancer
* Load Balancer의 SSL offloading 기능을 추가하였습니다.

#### 버그 수정
##### Load Balancer
* Load Balancer 제거 시 간헐적으로 정상 종료되지 않던 문제를 수정하였습니다.
