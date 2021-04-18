---
title: force_allocate atributo
description: O atributo ACF \ Force \_ ALLOCATE \ força um parâmetro de ponteiro a ser alocado usando a alocação de \_ usuário MIDL \_ em vez de otimizar a alocação.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate do atributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f73d0386d786e4d3004c78b1acccda7e9be8fc16
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104453996"
---
# <a name="force_allocate-attribute"></a>forçar \_ alocação de atributo

O atributo ACF de \[ **\_ realocação Force** \] força um parâmetro de ponteiro a ser alocado usando a [**\_ \_ alocação de usuário MIDL**](midl-user-allocate-1.md) em vez de otimizar a alocação.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parâmetros

Este atributo não tem parâmetros.

## <a name="remarks"></a>Comentários

O RPC tenta minimizar as alocações de memória no servidor fornecendo ponteiros para buffers de memória internos. Essa abordagem pode causar problemas para aplicativos que tentam chamar diretamente [**o \_ usuário MIDL \_ gratuitamente**](midl-user-free-1.md) em ponteiros fornecidos por RPC, porque um ponteiro otimizado não pode ser liberado. A marcação de um parâmetro com **\[ forçar \_ alocação \]** impedirá essa otimização para todos os ponteiros que a derivam.

Outro uso comum para a **\[ \_ distribuição \] forçada** é garantir o alinhamento da memória que está sendo apontada se um aplicativo exigir um alinhamento maior do que a da memória apontada. Por exemplo, os aplicativos geralmente passam dados em uma matriz genérica de bytes em vez de usar o tipo real, mas um byte só é garantido para ser alinhado em 1, o que pode causar problemas para aplicativos que assumem um alinhamento maior. Ao marcar o parâmetro com **\[ forçar \_ alocação \]**, o aplicativo pode garantir que toda a memória apontada terá um alinhamento igual ao que é garantido pelo [**usuário de MIDL \_ \_ alocar**](midl-user-allocate-1.md).

## <a name="examples"></a>Exemplos

``` syntax
/* IDL file */
void Func1([in, out, string] char **ppstr);
void Func2([in] long s, [in, size_is(s)] byte *pData);

/* ACF file */

/* e.g. The application wishes to call midl_user_free on *ppstr and supply a new pointer */
Func1([force_allocate] pstr);

/* e.g. pData really points to a structure that needs an alignment greater than 1 */
Func2([force_allocate] pData);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[Evitando a ocultação de informações](/windows/desktop/WinProg64/avoiding-information-hiding)
</dt> <dt>

[Criando interfaces compatíveis com 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**\_alocar usuário de MIDL \_**](midl-user-allocate-1.md)
</dt> <dt>

[**usuário de MIDL \_ \_ gratuito**](midl-user-free-1.md)
</dt> <dt>

[**aloca**](allocate.md)
</dt> </dl>

 

 