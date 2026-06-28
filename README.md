# nas-db
<a href="https://little-sulfur-621.notion.site/38cd3925342b809bb27ae693e4476f34" target="_blank">
    📄 Notion에서 문서 보기
</a>

# roles/nas-db/tasks

## 📋 DB 파트 플레이북 설명

| No | tasks | 설명 |
|:--:|----------|------|
| 1 | `init_01_hostname.yaml` | 호스트명(Hostname) 설정 |
| 2 | `nfs_01_server.yaml` | NFS 서버 설치 및 공유 디렉터리 구성 |
| 3 | `nfs_02_client.yaml` | NFS 클라이언트 설치 및 마운트 설정 |
| 4 | `db_01_install_server.yaml` | MySQL 서버 설치 |
| 5 | `db_02_mycnf_common.yaml` | MySQL 공통(my.cnf) 설정 적용 |
| 6 | `db_03_firewall.yaml` | MySQL 서비스 방화벽 설정 |
| 7 | `db_04_root_init.yaml` | MySQL Root 계정 초기화 및 보안 설정 |
| 8 | `db_05_mycnf_master.yaml` | Master 서버용 my.cnf 설정 |
| 9 | `db_06_mycnf_slave.yaml` | Slave 서버용 my.cnf 설정 |
| 10 | `db_07_repl_user.yaml` | Replication 사용자 생성 및 권한 부여 |
| 11 | `db_08_gtid.yaml` | GTID 기반 Replication 설정 |
| 12 | `db_09_table.yaml` | 테스트 데이터베이스 및 테이블 생성 |
| 13 | `db_10_backup_user.yaml` | 백업 계정 생성 및 권한 설정 |
| 14 | `db_11_install_connector.yaml` | MHA Node(Connector) 설치 |
| 15 | `db_12_cron.yaml` | Cron 작업 등록 |
| 16 | `db_13_deploy_program.yaml` | 프로그램 및 설정 파일 배포 |
| 17 | `db_14_pri.yaml` | MHA Failover Priority 설정 |
| 18 | `db_15_mha_commoninstall.yaml` | MHA 공통 패키지 설치 |
| 19 | `db_16_mha_master.yaml` | MHA Master 노드 설정 |
| 20 | `db_17_mha_slave.yaml` | MHA Slave 노드 설정 |
| 21 | `db_18_mha_manager.yaml` | MHA Manager 설치 및 구성 |
| 22 | `db_test.yaml` | Replication 및 MHA 동작 테스트 |
| 23 | `main.yaml` | 전체 Playbook 실행 및 Task 순차 호출 |

## 📂 roles/nas-db/templates

| No | File Name | Description |
|:--:|-----------|-------------|
| 1 | `backup_program.py` | 각 서버의 데이터를 증분 백업하여 NAS에 저장하는 백업 프로그램 |
| 2 | `backup_to_db.py` | NAS에 저장된 백업 파일을 MariaDB에 업로드하는 프로그램 |
| 3 | `master_ip_failover.sh` | Master 장애 발생 시 VIP를 신규 Master로 이동하는 Failover 스크립트 |
| 4 | `master_ip_online_change.sh` | 계획된 Master 전환 시 서비스 중단 없이 VIP를 이동하는 스크립트 |
| 5 | `mha_auto_recovery.sh` | Failover 이후 신규 Master 환경을 자동 복구하고 서비스를 재구성하는 스크립트 |
| 6 | `mha_precheck.sh` | MHA 실행 전 Master·Slave 복제 상태 및 접속을 사전 점검하는 스크립트 |
