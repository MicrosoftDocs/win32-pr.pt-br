---
title: OP_JOINPROV2_PART
description: Definição de IDL de OP_JOINPROV2_PART
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104084985"
---
# <a name="op_joinprov2_part-structure"></a>Estrutura de OP_JOINPROV2_PART

Contém informações adicionais usadas para configurar um cliente associado a um domínio.

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
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|O site especificado em lpSiteName deve ser considerado o site permanente para o cliente.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Contém o nome NetBIOS da conta do computador no formato Unicode.

### <a name="lpsitename"></a>lpSiteName

Contém o nome do site de Active Directory que o cliente deve usar.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Contém o nome de domínio DNS primário que o cliente deve usar.

### <a name="dwreserved"></a>dwReserved

Reservado para uso futuro e deve ser definido como 0.

### <a name="lpreserved"></a>lpReserved

Reservado para uso futuro e deve ser definido como nulo.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)
