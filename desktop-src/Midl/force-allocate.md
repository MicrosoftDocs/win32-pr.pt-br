---
title: force_allocate atributo
description: O atributo ACF \ force allocate\ força a alocação de um parâmetro de ponteiro usando a alocação de usuário médio em vez de \_ otimizar a \_ \_ alocação.
ms.assetid: 40e3a7d9-7e4f-4e3d-8c82-fb6ef567f293
keywords:
- force_allocate atributo MIDL
topic_type:
- apiref
api_name:
- force_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c82e1665e4c49461c3c7bd1c315b31f4f72c7e3f0e5331d9f0326347d36105
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582156"
---
# <a name="force_allocate-attribute"></a>atributo force \_ allocate

A alocação de força de atributo do ACF força a alocação de um parâmetro de ponteiro usando a alocação de usuário médio em vez de \[ **\_** otimizar \] a [**\_ \_**](midl-user-allocate-1.md) alocação.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ force_allocate [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="parameters"></a>Parâmetros

Esse atributo não tem parâmetros.

## <a name="remarks"></a>Comentários

O RPC tenta minimizar as alocações de memória no servidor fornecendo ponteiros para buffers de memória internos. Essa abordagem pode causar problemas para aplicativos que tentam chamar diretamente o usuário [**midl \_ \_ gratuitamente**](midl-user-free-1.md) em ponteiros fornecidos pelo RPC, porque um ponteiro que foi otimizado não pode ser liberado. Marcar um parâmetro com **\[ \_ alocação de força \]** impedirá essa otimização para todos os ponteiros que o derivam.

Outro uso comum para **\[ \_ \] alocar** à força é garantir o alinhamento da memória que está sendo apontada se um aplicativo exigir um alinhamento maior que o da memória apontada. Por exemplo, os aplicativos geralmente passam dados em uma matriz genérica de bytes em vez de usar o tipo real, mas um byte só tem a garantia de ser alinhado em 1, o que pode causar problemas para aplicativos que assumem um alinhamento maior. Marcando o parâmetro com **\[ \_ \] alocação** de força , o aplicativo pode garantir que toda a memória apontada terá um alinhamento igual ao garantido pelo usuário médio [**\_ \_ alocar**](midl-user-allocate-1.md).

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

[Projetando interfaces compatíveis com 64 bits](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)
</dt> <dt>

[**midl \_ user \_ allocate**](midl-user-allocate-1.md)
</dt> <dt>

[**midl \_ user \_ free**](midl-user-free-1.md)
</dt> <dt>

[**Alocar**](allocate.md)
</dt> </dl>

 

 