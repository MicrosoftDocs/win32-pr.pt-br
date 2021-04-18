---
title: opção/use_epv
description: A \_ opção/use EPV instrui o compilador MIDL a gerar código stub de servidor que chama a rotina de aplicativo de servidor por meio de um vetor de ponto de entrada (EPV), em vez de uma chamada estática. O uso desse atributo não é recomendado.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv MIDL do comutador
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105785439"
---
# <a name="use_epv-switch"></a>\_comutador/use EPV

A opção **/use \_ EPV** INSTRUI o compilador MIDL a gerar código stub de servidor que chama a rotina de aplicativo de servidor por meio de um vetor de ponto de entrada (EPV), em vez de uma chamada estática. O uso desse atributo não é recomendado.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos exigem ligação estática para a rotina de aplicativo do servidor. O compilador MIDL gera tal chamada por padrão. No entanto, se um aplicativo exigir que o stub do servidor chame a rotina de aplicativo do servidor usando o EPV, a opção **/use \_ EPV** deverá ser especificada. Quando a opção **/use \_ EPV** é especificada, o compilador MIDL gera um EPV padrão. Esse EPV padrão será usado se o aplicativo não registrar outro EPV por meio da chamada [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .

## <a name="examples"></a>Exemplos

**MIDL/use \_ EPV** *filename * * *. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/ \_ \_ EPV padrão**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 