---
title: opção/no_robust
description: O comutador de// \_ avançado orienta o compilador MIDL a desabilitar explicitamente o recurso de linha de comando/robust. A opção de linha de comando/robust e seus recursos associados são a configuração de compilador padrão para MIDL versão 6.0.359 e posterior.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust MIDL do comutador
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808851"
---
# <a name="no_robust-switch"></a>// \_ comutador robusto

O comutador de **// \_ avançado** orienta o compilador MIDL a desabilitar explicitamente o recurso de linha de comando [**/robust**](-robust.md) . A opção de linha de comando **/robust** e seus recursos associados são a configuração de compilador padrão para MIDL versão 6.0.359 e posterior.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Com o MIDL versão 6.0.359 e posterior, o compilador MIDL define [**/robust**](-robust.md) por padrão. A opção de linha de comando de **// \_ eficiência avançada** deve ser usada para desabilitar o recurso **/robust** se os stubs gerados precisarem ser executados no Microsoft WindowsÂ NT, no WindowsÂ 95/98 ou no WindowsÂ me.

## <a name="examples"></a>Exemplos

**MIDL/ \_ robusto filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




