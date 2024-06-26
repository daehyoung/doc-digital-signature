# 디지털 서명(Digital Signature)
디지털 서명은 일반적으로 다음과 같은 과정으로 이루어집니다:

1. **해시 생성**: 먼저 트랜잭션의 주요 내용이나 데이터에 대한 해시(고유한 고정 길이의 문자열)를 생성합니다. 해시 함수는 임의의 크기의 데이터를 입력으로 받아 이를 고정 크기의 고유한 해시 값으로 변환하는 알고리즘입니다. 이러한 해시 값은 데이터의 내용이 조금만 변경되어도 전혀 다른 값이 되는 특성을 가지고 있습니다.

2. **서명 생성**: 그 다음, 개인 키를 사용하여 해당 해시 값을 서명합니다. 이 서명은 공개 키로 검증할 수 있으며, 해당 트랜잭션이 해당 개인 키에 의해 서명되었음을 증명합니다.

3. **서명 확인**: 트랜잭션을 수신한 사람은 해당 공개 키를 사용하여 서명된 해시 값을 확인합니다. 이를 통해 트랜잭션이 원래의 발신자에 의해 서명되었는지를 확인할 수 있습니다.

이 과정을 통해 디지털 서명은 트랜잭션의 무결성을 보장하고, 특정 개인 또는 엔터티가 해당 트랜잭션을 서명했음을 증명합니다. 또한, 개인 키는 해당 사용자에게만 알려진 비밀이므로, 서명을 생성한 사용자가 누구인지를 확인할 수 있습니다. 이를 통해 트랜잭션의 무결성과 인증을 보장하고, 서명 부인 방지를 달성할 수 있습니다.


# 디지털 서명 검증
디지털 서명을 검증하려면 해당 서명을 생성한 개인의 공개 키를 알고 있어야 합니다. 공개 키는 디지털 서명의 검증에 사용되며, 이를 통해 서명이 해당 개인에 의해 생성되었음을 확인할 수 있습니다.

따라서 디지털 서명을 검증하기 위해서는 해당 서명을 생성한 개인의 공개 키를 따로 보관해야 합니다. 이 공개 키는 서명을 생성한 개인에게 속하며, 일반적으로 공개적으로 공개될 수 있습니다. 이 공개 키는 서명을 검증하는 데 사용되며, 서명이 해당 개인에 의해 생성되었음을 확인하는 데 필요합니다.

디지털 서명의 검증 과정에서는 다음과 같은 단계가 수행됩니다:

1. 서명을 생성한 개인의 공개 키를 획득합니다.
2. 트랜잭션에 대한 해시 값을 생성합니다.
3. 서명된 해시 값과 해당 공개 키를 사용하여 서명을 검증합니다.

이를 통해 서명이 원래의 발신자에 의해 생성되었는지를 확인할 수 있습니다. 따라서 서명을 검증하기 위해서는 해당 개인의 공개 키를 알고 있어야 합니다.


# 서명 부인 방지(Non-repudiation)

서명 부인 방지(Non-repudiation)는 보안 및 암호학에서 중요한 개념 중 하나입니다. 이는 한 당사자가 한 행동이나 트랜잭션을 나중에 부인하지 못하도록 하는 것을 의미합니다. 다시 말해, 한 번 발생한 행동에 대해 당사자가 그것을 나중에 부인할 수 없도록 하는 것입니다.

서명 부인 방지는 주로 디지털 서명(Digital Signature) 기술과 밀접하게 관련되어 있습니다. 디지털 서명은 전자 문서나 데이터의 무결성과 인증을 보장하기 위해 사용됩니다. 디지털 서명을 생성하는 데 사용되는 개인 키는 오직 해당 사용자만 가지고 있으므로, 해당 서명은 해당 사용자에게만 속한다고 간주됩니다.

디지털 서명은 다음과 같은 특성을 가집니다:

1. **서명 생성자 식별**: 디지털 서명은 서명을 생성한 개인을 식별할 수 있어야 합니다. 이를 통해 해당 서명이 어떤 사용자에 의해 생성되었는지를 추적할 수 있습니다.

2. **서명의 무결성 보장**: 디지털 서명은 서명이 생성된 후에 원본 데이터가 변경되지 않았음을 보장해야 합니다. 즉, 서명된 데이터가 무결성을 유지해야 합니다.

3. **서명 부인 방지**: 디지털 서명은 해당 사용자가 해당 서명을 생성했음을 부인하지 못하도록 보장해야 합니다. 이는 서명이 생성된 후에는 해당 사용자가 그것을 부인할 수 없음을 의미합니다.

서명 부인 방지는 디지털 서명 기술이 제공하는 가장 중요한 보안 속성 중 하나이며, 특히 전자상거래와 같은 온라인 트랜잭션에서 매우 중요한 역할을 합니다. 이를 통해 당사자간의 신뢰를 구축하고, 서명된 문서나 트랜잭션의 법적 유효성을 보장할 수 있습니다.


