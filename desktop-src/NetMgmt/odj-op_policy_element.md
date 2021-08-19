---
title: OP_POLICY_ELEMENT
description: Definição de IDL de OP_POLICY_ELEMENT
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983380"
---
# <a name="op_policy_element-structure"></a>Estrutura de OP_POLICY_ELEMENT

Define uma chave do registro e um nome de valor, tipo e valor que devem ser configurados sob essa chave.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>Membros

### <a name="pkeypath"></a>pKeyPath

Contém o caminho da chave do registro.

### <a name="pvaluename"></a>Valores principais

Contém o nome do valor do registro.

### <a name="ulvaluetype"></a>ulValueType

Contém um dos valores dos [tipos de valor do registro](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>cbValueData

Contém o tamanho de pValueData em bytes.

### <a name="ulvaluetype"></a>ulValueType

Contém o valor do valor do registro.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)