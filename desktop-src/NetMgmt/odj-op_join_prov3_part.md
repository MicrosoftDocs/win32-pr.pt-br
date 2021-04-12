---
title: OP_JOINPROV3_PART
description: Definição de IDL de OP_JOINPROV3_PART
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104366866"
---
# <a name="op_joinprov3_part-structure"></a>Estrutura de OP_JOINPROV3_PART

Contém informações adicionais usadas para configurar um cliente associado a um domínio.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Membros

### <a name="rid"></a>Eliminá

Deve ser definido como o identificador relativo do SID da conta do computador

### <a name="lpsid"></a>lpSid

Deve ser definido como o SID da conta do computador no formato de cadeia de caracteres.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)
