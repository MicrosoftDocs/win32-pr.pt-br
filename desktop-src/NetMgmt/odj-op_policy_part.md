---
title: OP_POLICY_PART
description: Definição de IDL de OP_POLICY_PART
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104366869"
---
# <a name="op_policy_part-structure"></a>Estrutura de OP_POLICY_PART

Contém uma matriz de estruturas de OP_POLICY_ELEMENT_LIST.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>Membros

### <a name="celementlists"></a>cElementLists

Contém o número de elementos em pElementLists.

### <a name="pelementlists"></a>pElementLists

Contém uma matriz de estruturas de OP_POLICY_ELEMENT_LIST.

### <a name="extension"></a>Extensão

Reservado para uso futuro e deve conter todos os zeros.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_lista de \_ elementos de política op \_**](odj-op_policy_element_list.md)
