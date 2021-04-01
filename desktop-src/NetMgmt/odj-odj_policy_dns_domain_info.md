---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: Definição de IDL de ODJ_POLICY_DNS_DOMAIN_INFO
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 36b7759451811844a91b3ee66ff3460fa4c4db34
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103642947"
---
# <a name="odj_policy_dns_domain_info-structure"></a>Estrutura de ODJ_POLICY_DNS_DOMAIN_INFO

Contém informações sobre o domínio e a floresta para os quais um cliente deve ser associado.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _ODJ_POLICY_DNS_DOMAIN_INFO
{
    ODJ_UNICODE_STRING Name;
    ODJ_UNICODE_STRING DnsDomainName;
    ODJ_UNICODE_STRING DnsForestName;
    GUID DomainGuid;
    PODJ_SID Sid;
} ODJ_POLICY_DNS_DOMAIN_INFO;
```

## <a name="members"></a>Membros

### <a name="name"></a>Nome

Deve ser definido como um nome de domínio NetBIOS.

### <a name="dnsdomainname"></a>DnsDomainName

Deve ser definido como um nome de domínio no formato DNS.

### <a name="dnsforestname"></a>DnsForestName

Deve ser definido como um nome de floresta no formato DNS.

### <a name="domainguid"></a>DomainGuid

Deve ser definido como o GUID de domínio.

### <a name="sid"></a>Sid

Deve ser definido como o SID do domínio.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_cadeia de \_ caracteres Unicode ODJ**](odj-odj_unicode_string.md)

[**ODJ \_ Sid**](odj-odj_sid.md)
