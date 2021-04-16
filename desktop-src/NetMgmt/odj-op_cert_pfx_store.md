---
title: OP_CERT_PFX_STORE
description: Definição de IDL de OP_CERT_PFX_STORE
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105772757"
---
# <a name="op_cert_pfx_store-structure"></a>Estrutura de OP_CERT_PFX_STORE

Contém uma estrutura PFX serializada.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>Membros

### <a name="ptemplatename"></a>pTemplateName

Deve ser definido como o nome do modelo de certificado usado para criar o certificado.

### <a name="ulprivatekeyexportpolicy"></a>ulPrivateKeyExportPolicy

Contém um valor da enumeração [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .

### <a name="ppolicyserverurl"></a>pPolicyServerUrl

Deve ser definido a URL do servidor de política.

### <a name="ulpolicyserverurlflags"></a>ulPolicyServerUrlFlags

Contém um valor da enumeração [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .

### <a name="ppolicyserverid"></a>pPolicyServerId

Contém uma cadeia de caracteres que identifica exclusivamente o servidor de políticas

### <a name="cbpfx"></a>cbPfx

Contém o tamanho de pPfx em bytes.

### <a name="ppfx"></a>pPfx

Contém uma estrutura PFX serializada (consulte [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)
