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
ms.openlocfilehash: dabdd6340005c4e56080dc91bdd372a858e0e7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006394"
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

 

 




