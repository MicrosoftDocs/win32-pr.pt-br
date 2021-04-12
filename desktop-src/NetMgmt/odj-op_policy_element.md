---
title: OP_POLICY_ELEMENT
description: Definição de IDL de OP_POLICY_ELEMENT
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104294650"
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