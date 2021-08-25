---
title: ODJ_POLICY_DNS_DOMAIN_INFO
description: ODJ_POLICY_DNS_DOMAIN_INFO IDL Definition
ms.assetid: 44b1145f-3bdd-42cd-a88f-9b41888cc644
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: d0a83ccade72a11449ca0cc9b35b9fc58e9c53d48f8248a9f6074cdb087cc0c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911587"
---
# <a name="odj_policy_dns_domain_info-structure"></a>ODJ_POLICY_DNS_DOMAIN_INFO estrutura

Contém informações sobre o domínio e a floresta aos que um cliente deve ser ingressado.

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

Deve ser definido como um nome de domínio Netbios.

### <a name="dnsdomainname"></a>DnsDomainName

Deve ser definido como um nome de domínio no formato DNS.

### <a name="dnsforestname"></a>DnsForestName

Deve ser definido como um nome de floresta no formato DNS.

### <a name="domainguid"></a>DomainGuid

Deve ser definido como o guid de domínio.

### <a name="sid"></a>Sid

Deve ser definido como o sid de domínio.

## <a name="see-also"></a>Confira também

[**Definições de IDL de Junção de Domínio Offline**](odj-idl.md)

[**CADEIA DE \_ CARACTERES UNICODE ODJ \_**](odj-odj_unicode_string.md)

[**SID do ODJ \_**](odj-odj_sid.md)
