---
title: /use_epv switch
description: A opção /use epv direciona o compilador MIDL para gerar o código stub do servidor que chama a rotina do aplicativo do servidor por meio de um vetor de ponto de entrada (epv), em vez de por uma chamada \_ estática. O uso desse atributo não é recomendado.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /use_epv com a opção MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 614abaf4c124aa0a6e1ca5f7da347ab4a9a2264e174c91734e6a75b188500a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014054"
---
# <a name="use_epv-switch"></a>/use \_ a opção epv

A **opção /use \_ epv** direciona o compilador MIDL para gerar o código stub do servidor que chama a rotina do aplicativo do servidor por meio de um vetor de ponto de entrada (epv), em vez de por uma chamada estática. O uso desse atributo não é recomendado.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos exigem vinculação estática à rotina de aplicativo do servidor. O compilador MIDL gera essa chamada por padrão. No entanto, se um aplicativo exigir que o stub do servidor chame a rotina de aplicativo do servidor usando o epv, a opção **/use \_ epv** deverá ser especificada. Quando a **opção /use \_ epv** é especificada, o compilador MIDL gera um epv padrão. Esse epv padrão será usado se o aplicativo não registrar outro epv por meio da [**chamada RpcServerRegisterIf.**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)

## <a name="examples"></a>Exemplos

**midl /use \_ epv** *filename***.idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Arquivo IDL (definição de interface)](interface-definition-idl-file.md)
</dt> <dt>

[**/no \_ \_ epv padrão**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 