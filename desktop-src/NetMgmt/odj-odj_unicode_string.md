---
title: ODJ_UNICODE_STRING
description: Definição de IDL de ODJ_UNICODE_STRING
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "105798320"
---
# <a name="odj_unicode_string-structure"></a>Estrutura de ODJ_UNICODE_STRING

Contém uma cadeia de caracteres Unicode.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a>Membros

### <a name="length"></a>Comprimento

Deve ser definido como o número de bytes no buffer que contém a cadeia de caracteres, não incluindo o terminador nulo.

### <a name="maximumlength"></a>MaximumLength

Isso deve ser definido como o número total de bytes no buffer, não incluindo o terminador nulo.

### <a name="buffer"></a>Buffer

Deve ser uma cadeia de caracteres Unicode.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)
