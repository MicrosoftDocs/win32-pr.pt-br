---
title: OP_POLICY_ELEMENT_LIST
description: Definição de IDL de OP_POLICY_ELEMENT_LIST
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 1fde1bb1d2794be4fd1bf799282a0257b78ae213453566208ff64bcf7a312654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796856"
---
# <a name="op_policy_element_list-structure"></a>Estrutura de OP_POLICY_ELEMENT_LIST

Define uma chave de registro raiz e uma matriz de elementos de chave do registro a serem configurados sob essa chave.

## <a name="syntax"></a>Sintaxe

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>Membros

### <a name="psource"></a>pSource

Contém o caminho do arquivo de Política de Grupo do qual os elementos contidos foram originados.

### <a name="ulrootkeyid"></a>ulRootKeyId

Contém o identificador da chave do registro raiz; no momento, deve ser definido como HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Contém o número de elementos em pElements.

### <a name="pelements"></a>pElements

Contém uma matriz de elementos de OP_POLICY_ELEMENT.

## <a name="see-also"></a>Confira também

[**Definições de IDL de ingresso no domínio offline**](odj-idl.md)

[**\_elemento de política op \_**](odj-op_policy_element.md)
