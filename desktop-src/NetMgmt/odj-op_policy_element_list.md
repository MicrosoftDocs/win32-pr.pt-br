---
title: OP_POLICY_ELEMENT_LIST
description: Definição de IDL de OP_POLICY_ELEMENT_LIST
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103642949"
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
