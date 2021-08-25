---
title: ODJ_UNICODE_STRING
description: ODJ_UNICODE_STRING definição de IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3578c62f110eafd053ed97bbe1f8b5015156d02c4b879ff8111ff13f28dfab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891235"
---
# <a name="odj_unicode_string-structure"></a>ODJ_UNICODE_STRING estrutura

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

Deve ser definido como o número de bytes em Buffer que contém a cadeia de caracteres, não incluindo o terminador NULL.

### <a name="maximumlength"></a>MaximumLength

Isso DEVE ser definido como o número total de bytes no Buffer, não incluindo o terminador NULL.

### <a name="buffer"></a>Buffer

Deve ser uma cadeia de caracteres Unicode.

## <a name="see-also"></a>Confira também

[**Definições de IDL de Junção de Domínio Offline**](odj-idl.md)
