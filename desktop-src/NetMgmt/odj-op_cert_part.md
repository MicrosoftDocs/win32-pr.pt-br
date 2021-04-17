---
title: OP_CERT_PART
description: Definição de IDL de OP_CERT_PART
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105798319"
---
# <a name="op_cert_part-structure"></a>Estrutura de OP_CERT_PART

Contém repositórios de certificados e PFX serializados.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>Membros

### <a name="cpfxstores"></a>cPfxStores

Contém o número de elementos em pPfxStores.

### <a name="ppfxstores"></a>pPfxStores

Contém uma matriz de estruturas de OP_CERT_PFX_STORE.

### <a name="csststores"></a>cSstStores

Contém o número de elementos em pSstStores.

### <a name="psststores"></a>pSstStores

Contém uma matriz de estruturas de OP_CERT_SST_STORE.

### <a name="extension"></a>Extensão

Reservado para uso futuro e deve conter todos os zeros.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_ \_ repositório pfx de certificado op \_**](odj-op_cert_pfx_store.md)

[**\_ \_ repositório SST do certificado op \_**](odj-op_cert_sst_store.md)

[**BLOB de OP \_**](odj-op_blob.md)

