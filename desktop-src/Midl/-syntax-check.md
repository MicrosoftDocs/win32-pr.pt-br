---
title: /syntax_check switch
description: A opção de \_ verificação /syntax indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check com a opção MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f65b22e6c921a37083486dbdb10eddc5316a372200bdd145af282f6879cc99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991874"
---
# <a name="syntax_check-switch"></a>Opção de \_ verificação /sintaxe

A **opção de verificação \_ /syntax** indica que o compilador verifica apenas a sintaxe e não gera arquivos de saída.

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Essa opção substitui todas as outras opções que especificam informações sobre arquivos de saída.

Você também pode especificar o modo de verificação de sintaxe com a opção do compilador MIDL [**/Zs**](-zs.md).

## <a name="examples"></a>Exemplos

**midl /Zs filename.idl**

**midl /syntax \_ check filename.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/zs**](-zs.md)
</dt> </dl>

 

 




