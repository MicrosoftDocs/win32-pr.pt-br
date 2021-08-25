---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL Definition
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8ad479c2e24d8c38e87a2100658be2afcf37d70d321e99433e3b05a3af35fa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911476"
---
# <a name="op_policy_part-structure"></a>OP_POLICY_PART estrutura

Contém uma matriz de OP_POLICY_ELEMENT_LIST estruturas.

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

Contém uma matriz de OP_POLICY_ELEMENT_LIST estruturas.

### <a name="extension"></a>Extensão

Reservado para uso futuro e deve conter todos os zeros.

## <a name="see-also"></a>Confira também

[**Definições de IDL de Junção de Domínio Offline**](odj-idl.md)

[**LISTA DE \_ ELEMENTOS \_ DE POLÍTICA \_ OP**](odj-op_policy_element_list.md)
