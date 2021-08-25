---
title: ODJ_WIN7BLOB
description: Definição de IDL de ODJ_WIN7BLOB
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ab6f6582b23d6e65866ba1380b696fab6d8313578fab47ad5dda999b09a1caa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911586"
---
# <a name="odj_win7blob-structure"></a>Estrutura de ODJ_WIN7BLOB

Contém as informações básicas necessárias para ingressar um cliente em um domínio.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>Membros

### <a name="lpdomain"></a>lpDomain

Deve ser definido como o nome de domínio.

### <a name="lpmachinename"></a>lpMachineName

Deve ser definido como o nome do computador.

### <a name="lpmachinepassword"></a>lpMachinePassword

Deve ser definido como uma senha de texto não criptografado para a conta de computador identificada por lpMachineName

### <a name="dnsdomaininfo"></a>DnsDomainInfo

Contém informações sobre o domínio que está sendo ingressado.

### <a name="dcinfo"></a>DcInfo

Contém informações de nomenclatura e endereçamento sobre o controlador de domínio que foi usado para criar a conta de computador Active Directory.

### <a name="options"></a>Opções

Deve ser definido como zero.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_informações de \_ \_ domínio DNS da política \_ ODJ**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



