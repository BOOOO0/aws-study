# IAM 개요

- IAM은 AWS의 계정과 계정의 권한을 관리하는 서비스입니다.

- AWS 서비스와 리소스에 대한 접근을 관리합니다.

- `사용자, 그룹, 역할, 정책`으로 구성되어 있습니다.

- 리전에 속하는 서비스가 아닌 글로벌 서비스입니다.

- 계정 보안 강화를 위해 루트 계정은 최초 계정 생성 이후 사용하지 않고 사용자 계정(IAM 계정)으로 서비스를 사용하고 각 사용자 계정에 최소한의 권한만 부여해야 합니다(최소 권한의 원칙).

## 루트 계정으로만 할 수 있는 작업

- 계정 이름, 이메일 주소, 루트 계정 암호, 액세스 키에 대한 부분은 루트 계정에서만 가능합니다.

- IAM 관리자가 한 계정의 권한을 취소했을 경우 그것을 복원하기 위해 루트 계정을 사용합니다.

- Billing and Cost Management 콘솔(요금 청구 관련)에 대한 IAM 계정의 액세스를 활성화하는 권한도 루트 계정만이 가지고 있습니다. 그리고 세금과 관련된 조회도 루트 계정만이 권한을 가지고 있습니다.

- AWS 계정을 닫는 것, AWS Support Plan을 변경하는 것을 루트 계정이 담당합니다.

- 마켓 플레이스에 인스턴스를 판매하기 위해 판매자로 등록할 경우에도 루트 계정이 필요합니다.

- Amazon S3 버킷의 데이터를 삭제할 때 MFA Delete를 활성화하도록 하는 경우에도 루트 계정이 필요합니다.

- 잘못된 VPC ID나 VPC 엔드포인트 ID가 들어있는 Amazon S3 버킷 정책을 편집하거나 삭제할 때도 필요합니다.

- GovCloud등록에도 필요합니다.

## 사용자

- 사람, ID, 계정 등을 의미합니다.

## 그룹

- 사용자의 모음입니다. 재무팀, 개발팀 등 팀 단위를 지칭합니다.

## 역할

- AWS 리소스에서 사용하는 자격 증명입니다. 예를 들어 EC2에서 S3, RDS 같은 AWS 리소스에 액세스하는 경우에 이 권한을 역할로서 부여합니다.

## 정책

- 사용자, 그룹, 역할에 대한 권한의 정의입니다. 어떤 것을 할 수 있고 없는 지를 나눕니다. JSON문서로 구성되어 있습니다.