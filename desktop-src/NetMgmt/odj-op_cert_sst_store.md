---
title: OP_CERT_SST_STORE
description: Definição de IDL de OP_CERT_SST_STORE
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104369004"
---
# <a name="op_cert_sst_store-structure"></a>Estrutura de OP_CERT_SST_STORE

Contém um repositório de certificados serializado.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>Membros

### <a name="storelocation"></a>StoreLocation

Contém um identificador para o repositório de certificados de [**locais de armazenamento do sistema**](../seccrypto/system-store-locations.md).

### <a name="pstorename"></a>pStoreName

Contém o nome da loja.

### <a name="cbsst"></a>cbSst

Contém o tamanho de pSst em bytes.

### <a name="psst"></a>pSst

Contém um repositório de certificados serializado (consulte [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)