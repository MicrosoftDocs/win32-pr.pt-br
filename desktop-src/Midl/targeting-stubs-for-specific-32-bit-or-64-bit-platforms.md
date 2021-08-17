---
title: Direcionamento de stubs para plataformas específicas de 32 ou 64 bits
description: Alguns dos recursos do Microsoft RPC e do MIDL 3.0 e compiladores posteriores são específicos da plataforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL de plataformas de 32 bits
- MIDL de plataformas de 64 bits
- stubs MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e0f78e47ed078bf7cd1fd78fa8730b597554a6c8ba1ed4fc5a67bc562e7d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641166"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Direcionamento de stubs para plataformas específicas de 32 ou 64 bits

Alguns dos recursos do Microsoft RPC e do MIDL 3.0 e compiladores posteriores são específicos da plataforma.

Como precaução, os compiladores MIDL 3.0 e posteriores geram proteção que facilitam a verificação de compatibilidade durante a fase de compilação C. MIDL gera dois tipos de proteção: uma proteção dependente da plataforma (32 bits versus 64 bits) e uma proteção dependente de versão (dependência do conjunto de recursos). Por exemplo, MIDL gera a seguinte proteção para impedir a compilação C de um stub de 32 bits para outras plataformas:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

A proteção dependente de versão é disparada por um conjunto de recursos encontrados nos arquivos IDL processados e pela opção [**/target.**](-target.md) Por exemplo, se a interface usar recursos com suporte apenas no Windows 2000 ou posterior, o MIDL gerará uma proteção com a macro TARGET \_ IS \_ NT50 \_ OU \_ POSTERIOR.

As macros de proteção, definidas em Rpcndr.h, dependem da configuração de WINVER e WIN32 WINNT e são avaliadas pelo \_ \_ compilador C/C++.

Se, no momento da compilação C, você receber uma mensagem de erro indicando que precisa de uma plataforma específica para executar um stub, primeiro verifique se você não usou um recurso que não está disponível nessa plataforma. Os recursos que disparam uma proteção específica são listados no corpo da proteção. No exemplo anterior, a opção do compilador -Oicf disparou a proteção. Recursos importantes desse tipo incluem a opção [**/robust**](-robust.md) e o atributo assíncrono disponível no Windows 2000 e posterior, o construtor de tipo de \[ [](async.md) \] pipe, [](pipe.md) a opção do compilador /Oif e os atributos de \[ [**\_ marshal**](user-marshal.md) de usuário e marshal de \] \[ [**\_**](wire-marshal.md) \] transmissão. Stubs que usam esses recursos não serão executados em sistemas anteriores.

Se você sabe que sua plataforma de destino está correta para os recursos que está usando e ainda recebe um erro, talvez seja necessário definir as variáveis de ambiente adequadamente.

**Para criar para o Windows 2000 ou versões posteriores**

-   Adicione esta linha ao makefile:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**/target**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**Async**](async.md)
</dt> <dt>

[**async \_ uuid**](async-uuid.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**Tubo**](pipe.md)
</dt> <dt>

[**wire \_ marshal**](wire-marshal.md)
</dt> <dt>

[**marshal \_ de usuário**](user-marshal.md)
</dt> <dt>

[Marshaling de tipos de dados OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




