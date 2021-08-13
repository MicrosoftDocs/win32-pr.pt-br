---
title: comutador/RPCSS
description: A opção/RPCSS, quando especificada, atua como se o atributo de alocação de habilitação \_ fosse especificado em todas as operações da interface. O uso desse atributo não é recomendado.
ms.assetid: a4507779-7d07-4517-8592-39f0d9460bc3
keywords:
- MIDL do comutador/RPCSS
topic_type:
- apiref
api_name:
- /rpcss
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e0c3087f47bd12c852ef168b2684d5b094239cdac45933c8e7d831fc6461c1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643736"
---
# <a name="rpcss-switch"></a>comutador/RPCSS

A opção **/RPCSS** , quando especificada, atua como se o atributo de [**\_ alocação de habilitação**](enable-allocate.md) fosse especificado em todas as operações da interface. O uso desse atributo não é recomendado.

``` syntax
midl /rpcss
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

No modo padrão, o pacote RpcSs será habilitado somente se o procedimento ou a interface tiver o atributo [**habilitar \_ alocação**](enable-allocate.md) ou o comutador **/RPCSS** for especificado na linha de comando. No modo **/OSF** , o stub do lado do servidor habilita o pacote de alocação do RPCSS.

## <a name="examples"></a>Exemplos

**MIDL/RPCSS filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**Habilitar \_ alocação**](enable-allocate.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 




