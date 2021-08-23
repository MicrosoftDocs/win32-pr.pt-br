---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART IDL Definition
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: fa6853846695c02aabf85d0be865254608b9d4c00f39a372e99f1332e6eb4003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012454"
---
# <a name="op_joinprov2_part-structure"></a>OP_JOINPROV2_PART estrutura

Contém informações adicionais usadas para configurar um cliente ingressando em um domínio.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>Membros

### <a name="dwflags"></a>dwFlags

Deve ser definido como zero ou um dos seguintes valores:

|Valor|Significado|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|O site especificado em lpSiteName DEVE ser considerado o site permanente para o cliente.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Contém o nome Netbios da conta do computador no formato Unicode.

### <a name="lpsitename"></a>lpSiteName

Contém o nome do site do Active Directory que o cliente deve usar.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Contém o nome de domínio DNS primário que o cliente deve usar.

### <a name="dwreserved"></a>dwReserved

Reservado para uso futuro e deve ser definido como 0.

### <a name="lpreserved"></a>lpReserved

Reservado para uso futuro e deve ser definido como NULL.

## <a name="see-also"></a>Confira também

[**Definições de IDL de Junção de Domínio Offline**](odj-idl.md)
