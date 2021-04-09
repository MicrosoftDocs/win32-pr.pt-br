---
title: opção/ms_ext
description: Em vigor com a versão 3,0 do MIDL, os recursos habilitados pela \_ opção MS ext agora são o modo padrão para o compilador MIDL.
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext MIDL do comutador
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbccf1205c9a937b78b08c46f31bc09aa3b75c70
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007404"
---
# <a name="ms_ext-switch"></a>\_comutador/MS ext

Em vigor com a versão 3,0 do MIDL, os recursos habilitados pela opção **MS \_ ext** agora são o modo padrão para o compilador MIDL.

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Usar a opção não gerará um erro do compilador, portanto, você não precisa remover referências a **/MS \_ ext** ou [**/c \_ ext**](-c-ext.md) de um makefile existente.

As seguintes extensões da Microsoft para uso o DCE agora estão disponíveis por padrão:

-   Definições de interface para objetos OLE. Para obter mais informações sobre os arquivos gerados para interfaces OLE, consulte [arquivos gerados para uma interface com](files-generated-for-a-com-interface.md)
-   Um atributo de [**\[ retorno de chamada \]**](callback.md) que especifica uma função de retorno de chamada estática no cliente
-   [**\_ aspas de CPP**](cpp-quote.md)(*cadeia de \_ caracteres entre aspas*) e [**\# \_ eco de MIDL de pragma**](pragma.md)
-   [**WCHAR \_ t**](wchar-t.md) largo-tipos de caractere, constantes e cadeias de caracteres
-   [**inicialização de enumeração**](enum.md) (enumeradores esparsos)
-   Expressões como tamanho e especificadores de discriminador
-   [Manipular extensões](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [Herança de tipo de atributo de ponteiro](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [Várias interfaces](/windows/desktop/Rpc/registering-interfaces)
-   Definições fora do bloco de interface
-   Você pode omitir os [atributos direcionais](/windows/desktop/Rpc/directional-parameter-attributes) para \[ [**dentro**](in.md), [**fora**](out-idl.md)\]

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> <dt>

[Herança de tipo de atributo de ponteiro](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**configuração do/App \_**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 