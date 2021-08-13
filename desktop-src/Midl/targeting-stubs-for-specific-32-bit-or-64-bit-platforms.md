---
title: Direcionando stubs para plataformas específicas de 32 bits ou 64 bits
description: Alguns dos recursos do Microsoft RPC e do MIDL 3,0 e dos compiladores posteriores são específicos da plataforma.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- MIDL plataformas de 32 bits
- MIDL plataformas de 64 bits
- MIDL de stubs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e0f78e47ed078bf7cd1fd78fa8730b597554a6c8ba1ed4fc5a67bc562e7d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641166"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a>Direcionando stubs para plataformas específicas de 32 bits ou 64 bits

Alguns dos recursos do Microsoft RPC e do MIDL 3,0 e dos compiladores posteriores são específicos da plataforma.

Como precaução, os compiladores MIDL 3,0 e posterior geram proteções que facilitam a verificação de compatibilidade durante a fase de compilação da C. O MIDL gera dois tipos de guardas: uma proteção dependente de plataforma (32 bits versus 64 bits) e uma proteção dependente de versão (dependência de conjunto de recursos). Por exemplo, MIDL gera a seguinte proteção para evitar a compilação C de um stub de 32 bits para outras plataformas:

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

A proteção dependente de versão é disparada por um conjunto de recursos encontrados nos arquivos IDL processados e pela opção [**/target**](-target.md) . Por exemplo, se a interface usar recursos com suporte apenas no WindowsÂ 2000 ou posterior, MIDL gerará uma proteção com o destino \_ é \_ NT50 \_ ou \_ macro posterior.

As macros de proteção, definidas em Rpcndr. h, dependem da configuração de WINVER e \_ Win32 \_ winnt e são avaliadas pelo compilador C/C++.

Se, em tempo de compilação C, você receber uma mensagem de erro indicando que precisa de uma plataforma específica para executar um stub, primeiro verifique se você não usou um recurso que não esteja disponível nesta plataforma. Os recursos que disparam um determinado protetor são listados no corpo da proteção. No exemplo anterior, a opção de compilador-Oicf disparou a proteção. Os recursos notáveis desse tipo incluem a opção [**/robust**](-robust.md) e o \[ atributo [**async**](async.md) \] disponíveis no WindowsÂ 2000 e posterior, o construtor de tipo de [**pipe**](pipe.md) , a opção de compilador/OIF e os \[ atributos [**\_ marshaling do usuário**](user-marshal.md) \] e \[ [**Wire \_ Marshal**](wire-marshal.md) \] . Os stubs que usam esses recursos não serão executados em sistemas anteriores.

Se você souber que a plataforma de destino está correta para os recursos que está usando e ainda receber um erro, talvez seja necessário definir as variáveis de ambiente adequadamente.

**Para compilar para o WindowsÂ 2000 ou versões posteriores**

-   Adicione esta linha ao seu makefile:

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**/debug**](-target.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**Async**](async.md)
</dt> <dt>

[**\_UUID assíncrono**](async-uuid.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**conexão**](pipe.md)
</dt> <dt>

[**\_marshaling de transmissão**](wire-marshal.md)
</dt> <dt>

[**Marshal do usuário \_**](user-marshal.md)
</dt> <dt>

[Empacotamento de tipos de dados OLE](marshaling-ole-data-types.md)
</dt> </dl>

 

 




