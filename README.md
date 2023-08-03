# Rocky-Linux

CentOS7 차이점
1. 패키지 관리 명령어
   - yum과 dnf 같이 사용 가능
   - CentOS 8과 같음
   - 둘다 RHEP 8버전 기반이기 때문

3. 웹 3tier 구성 (nginx - tomcat - mariaDB)
   - 기존 centOS와 다른점 못찾음

4. firewalld 및 iptables 미설치 (AWS AMI 기준 )

5. NTP 관련 데몬 및 명령어 변경
   - ntpd -> chronyd
   - ntpdate -> chronyc sources

6. 설정 관련 파일 변경
   - tcp_wrappers 모듈 비활성화
      - host.allow / host.deny 파일 사용 안함
   - 패스워드 복잡도 설정 파일 : /etc/pam.d/system-auth -> /etc/security/pwquality.conf
