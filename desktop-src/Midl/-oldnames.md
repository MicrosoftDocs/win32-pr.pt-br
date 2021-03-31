---
title: comutador/OLDNAMES
description: A opção/OLDNAMES instrui o compilador MIDL a gerar nomes de interface que não incluem o número de versão.
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- MIDL do comutador/OLDNAMES
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cf861d2bf4f4123d7a1ee103e6966e5d404946
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640636"
---
# <a name="oldnames-switch"></a>comutador/OLDNAMES

A opção **/OLDNAMES** instrui o compilador MIDL a gerar nomes de interface que não incluem o número de versão.

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

O compilador MIDL incorpora o número de versão da interface no nome da interface que é gerado no stub (por exemplo, iface \_ v1 \_ 0 \_ ServerIfHandle). Esse formato de nomenclatura é consistente com o formato usado pelo compilador uso DCE IDL. No entanto, ele difere do formato de nomenclatura usado pelo compilador MIDL 1,0. O compilador MIDL 1,0 não incluiu números de versão em nomes de interface (por exemplo, iface \_ ServerIfHandle). A opção **/OLDNAMES** permite instruir o compilador MIDL a gerar nomes de interface que não incluem o número de versão. Dessa forma, o formato é consistente com nomes gerados pelo compilador MIDL 1,0.

Se você tiver um código de aplicativo de servidor que foi escrito para uso com um stub gerado pelo compilador MIDL 1,0 e se referir ao nome da interface gerada pelo MIDL (por exemplo, em uma chamada para [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)), você deverá alterá-lo para fazer referência ao estilo do nome da interface com suporte da versão 2,0 ou posterior do compilador MIDL. Como alternativa, você pode usar a opção **/OLDNAMES** ao invocar o compilador MIDL.

## <a name="examples"></a>Exemplos

**MIDL/OLDNAMES filename. idl**

## <a name="see-also"></a>Consulte também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[Arquivo de definição de interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 