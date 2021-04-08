---
title: Sintaxe de linha de comando MIDL geral
description: O compilador MIDL processa um arquivo IDL e um arquivo de configuração de aplicativo opcional (ACF) para gerar um conjunto de arquivos de saída.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- MIDL de referência de linha de comando, sintaxe geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822982"
---
# <a name="general-midl-command-line-syntax"></a>Sintaxe de linha de comando MIDL geral

O compilador MIDL processa um arquivo IDL e um arquivo de configuração de aplicativo opcional (ACF) para gerar um conjunto de arquivos de saída. Os atributos especificados na lista de atributos da interface do arquivo IDL determinam se o compilador gera arquivos de origem para uma interface RPC ou para uma interface OLE personalizada.

## <a name="switch-options"></a>Opções de comutação

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*opção de linha de comando*
</dt> <dd>

Especifica opções de linha de comando do compilador MIDL. As opções podem aparecer em qualquer sequência.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*opções de opção*
</dt> <dd>

Especifica as opções associadas a cada comutador. As opções válidas são descritas na entrada de referência para cada comutador de compilador de MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*
</dt> <dd>

Especifica o nome do arquivo IDL. Normalmente, esse arquivo tem a extensão. idl, mas ele pode ter outro ou nenhum.

</dd> </dl>

## <a name="remarks"></a>Comentários

As listas a seguir mostram os nomes padrão dos arquivos gerados para um arquivo IDL chamado name. idl. Você pode usar opções de linha de comando para substituir esses nomes padrão. Observe que o nome do arquivo IDL pode ter uma extensão diferente de. IDL ou nenhuma extensão.

Por padrão (ou seja, se a lista de atributos de interface não contiver o [**objeto**](object.md) ou o atributo [**local**](local.md) ), o compilador gerará os seguintes arquivos para uma [interface RPC](files-generated-for-an-rpc-interface.md):

-   Stub do cliente (nome \_ c. c)
-   Stub do servidor (nome \_ s. c)
-   Arquivo de cabeçalho (Name. h)

Quando o atributo de [**objeto**](object.md) aparece na lista de atributos de interface, o compilador gera os seguintes arquivos para uma interface com:

-   Arquivo de proxy da interface (nome \_ p. c)
-   Arquivo de cabeçalho de interface (Name. h)
-   Arquivo UUID da interface (name \_ I. c)

Quando o atributo [**local**](local.md) aparece na lista atributo de interface, o compilador gera apenas o arquivo de cabeçalho de interface, Name. h.

O compilador MIDL fornecido com o Microsoft RPC invoca o pré-processador C conforme necessário para processar o arquivo IDL. Ele não invoca automaticamente o compilador C para compilar arquivos gerados.

> [!Note]  
> O compilador MIDL fornecido com o Microsoft RPC usa uma sintaxe de linha de comando diferente do compilador de IDL do DCE.

 

O compilador MIDL alterna [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) afeta o arquivo stub do servidor.

Começando com o MIDL versão 6.0.359, a opção de linha de comando padrão para o compilador MIDL é [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md). Para desabilitar o/robust, especifique a opção [**// \_ robusta**](-no-robust.md) .

## <a name="the-header-file"></a>O arquivo de cabeçalho

O arquivo de cabeçalho contém definições de todos os tipos de dados e operações declaradas no arquivo IDL. O arquivo de cabeçalho deve ser incluído por todos os módulos de aplicativo que chamam as operações definidas, implementar as operações definidas ou manipular os tipos definidos.

O compilador MIDL alterna [**/header**](-header.md) e [**/out**](-out.md) afeta o arquivo de cabeçalho.

 

 




