---
title: opção/app_config
description: A \_ opção/app config seleciona o modo de configuração de aplicativo, que permite que você use algumas palavras-chave ACF no arquivo IDL. Com essa opção de compilador MIDL, você pode omitir o ACF e especificar uma interface em um único arquivo IDL.
ms.assetid: 8d12a0ed-7eaa-4ebc-a961-b726aefefadc
keywords:
- /app_config MIDL do comutador
topic_type:
- apiref
api_name:
- /app_config
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717d5234bd419fec7107a6d983ece026b4558935
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364953"
---
# <a name="app_config-switch"></a>\_opção de configuração/app

A opção **/app \_ config** seleciona o modo de configuração de aplicativo, que permite que você use algumas palavras-chave ACF no arquivo IDL. Com essa opção de compilador MIDL, você pode omitir o ACF e especificar uma interface em um único arquivo IDL.

``` syntax
midl /app_config
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

O Microsoft RPC dá suporte ao uso dos seguintes atributos de ACF no arquivo IDL:

-   \_Identificador implícito
-   \_Identificador automático
-   \_Identificador explícito

Versões futuras do Microsoft RPC podem dar suporte ao uso de outros atributos de ACF no arquivo IDL. A opção de **\_ configuração/app** representa uma extensão da Microsoft para a especificação uso-DCE e, como tal, é mutuamente exclusiva com a opção [**/OSF**](-osf.md) .

Para obter mais informações relacionadas à opção de **\_ configuração/app** , consulte arquivo de [configuração de aplicativo (ACF)](application-configuration-file-acf-.md) e [arquivo de definição de interface (IDL)](interface-definition-idl-file.md).

## <a name="examples"></a>Exemplos

**MIDL/app \_ config filename. idl**

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




