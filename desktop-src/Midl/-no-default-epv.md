---
title: opção/no_default_epv
description: A \_ opção EPV padrão de// \_ r instrui o compilador MIDL a não gerar um vetor de ponto de entrada (EPV) padrão. O uso desse atributo não é recomendado.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /no_default_epv MIDL do comutador
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917192"
---
# <a name="no_default_epv-switch"></a>\_opção de EPV padrão de//. \_

A **opção \_ \_ EPV padrão de//** r instrui o compilador MIDL a não gerar um vetor de ponto de entrada (EPV) padrão. O uso desse atributo não é recomendado.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Nesse caso, o aplicativo deve registrar um EPV com a chamada [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) . Compare essa opção com o comutador [**/use \_ EPV**](-use-epv.md) .

## <a name="examples"></a>Exemplos

**MIDL/ \_ Default \_ EPV filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/Use \_ EPV**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 