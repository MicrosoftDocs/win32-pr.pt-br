---
title: Opção /Zs
description: A opção /Zs indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /Zs switch MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92bd2321567bbc565d3198fe5ebf5c98a3d8df440ea967409830c8e73488609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014014"
---
# <a name="zs-switch"></a>Opção /Zs

A **opção /Zs** indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Essa opção substitui todas as outras opções que especificam informações sobre arquivos de saída.

Você também pode especificar o modo de verificação de sintaxe com a opção do compilador MIDL [**/verificação de \_ sintaxe**](-syntax-check.md).

## <a name="examples"></a>Exemplos

**midl /Zs filename.idl**

**midl /syntax \_ check filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sintaxe \_ check**](-syntax-check.md)
</dt> </dl>

 

 




