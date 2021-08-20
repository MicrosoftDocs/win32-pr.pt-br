---
title: /no_format_opt switch
description: A opção /no \_ format opt altera a maneira como MIDL otimiza descritores de tipo \_ e procedimento.
ms.assetid: 721ac828-7b47-4991-8bce-f9babf6c77a8
keywords:
- /no_format_opt com a opção MIDL
topic_type:
- apiref
api_name:
- /no_format_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93753d1aa73d378ff093cf2d315e144461f466a42910e1778060be05defb911a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014134"
---
# <a name="no_format_opt-switch"></a>/no \_ format \_ opt switch

A **opção /no \_ format \_ opt** altera a maneira como MIDL otimiza descritores de tipo e procedimento.

``` syntax
midl /no_format_opt
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Por padrão, MIDL elimina descritores de tipo e procedimento duplicados para reduzir o tamanho do código stub gerado. O uso **da opção /no \_ format \_ opt** desliga esse comportamento de otimização.

## <a name="examples"></a>Exemplos

**midl /no \_ format \_ opt mylean.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> </dl>

 

 




