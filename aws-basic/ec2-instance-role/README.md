# EC2 인스턴스에 역할 부여하기

- 예시로 EC2 서버에서 IAM 서비스에 접근할 수 있는 역할을 부여해보겠습니다.

- 우선 IAM 서비스에서 역할을 생성해야 합니다. AWS 서비스에서 일반 사용 사례 중 EC2를 선택합니다.

- 정책 중 IAMReadOnlyAccess를 선택하고 역할의 이름을 설정해서 생성합니다.

- EC2 인스턴스로 돌아가서 우측 상단 작업 항목을 클릭하고 보안 항목에 IAM 역할 수정을 클릭해서 생성해둔 IAM 역할을 선택합니다.

## EC2 서버에서 IAM 역할 목록 확인

- `aws iam list-roles`명령어로 목록을 확인할 수 있습니다.

- `aws iam list-users`명령어로 IAM 사용자들의 정보를 확인할 수 있습니다.