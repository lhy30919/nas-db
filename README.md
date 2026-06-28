# nas-db
<a href="https://little-sulfur-621.notion.site/38cd3925342b809bb27ae693e4476f34" target="_blank">
    📄 Notion에서 보기
</a>
```markdown
# roles/nas-db/tasks

## 📋 Playbook 설명

| No | Playbook | 설명 |
|:--:|----------|------|
| 1 | `init_01_hostname.yaml` | 호스트명(Hostname) 설정 |
| 2 | `nfs_01_server.yaml` | NFS 서버 설치 및 공유 디렉터리 구성 |
| 3 | `nfs_02_client.yaml` | NFS 클라이언트 설치 및 마운트 설정 |
| 4 | `db_01_install_server.yaml` | MariaDB 서버 설치 |
| 5 | `db_02_mycnf_common.yaml` | MariaDB 공통(my.cnf) 설정 적용 |
| 6 | `db_03_firewall.yaml` | MariaDB 서비스 방화벽 설정 |
| 7 | `db_04_root_init.yaml` | MariaDB Root 계정 초기화 및 보안 설정 |
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
```
