---
title: Sintaxe geral da linha de comando MIDL
description: O compilador MIDL processa um arquivo IDL e um arquivo de configuração de aplicativo opcional (ACF) para gerar um conjunto de arquivos de saída.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- referência de linha de comando MIDL, sintaxe geral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3d3ded263237dffa425cebe3dea49b169e3494045cfc8b0d27cc249c5ebed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118384259"
---
# <a name="general-midl-command-line-syntax"></a>Sintaxe geral da linha de comando MIDL

O compilador MIDL processa um arquivo IDL e um arquivo de configuração de aplicativo opcional (ACF) para gerar um conjunto de arquivos de saída. Os atributos especificados na lista de atributos de interface do arquivo IDL determinam se o compilador gera arquivos de origem para uma interface RPC ou para uma interface OLE personalizada.

## <a name="switch-options"></a>Opções de opção

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*
</dt> <dd>

Especifica opções de linha de comando do compilador MIDL. As opções podem aparecer em qualquer sequência.

</dd> <dt>

<span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*opções de opção*
</dt> <dd>

Especifica as opções associadas a cada opção. As opções válidas são descritas na entrada de referência para cada opção do compilador MIDL.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

Especifica o nome do arquivo IDL. Esse arquivo geralmente tem a extensão .idl, mas pode ter outro ou nenhum.

</dd> </dl>

## <a name="remarks"></a>Comentários

As listas a seguir mostram os nomes padrão dos arquivos gerados para um arquivo IDL chamado Name.idl. Você pode usar opções de linha de comando para substituir esses nomes padrão. Observe que o nome do arquivo IDL pode ter uma extensão diferente de .idl ou nenhuma extensão.

Por padrão (ou seja, se a lista [](object.md) de atributos de interface não contém o objeto ou atributo [**local),**](local.md) o compilador gera os seguintes arquivos para uma [interface RPC](files-generated-for-an-rpc-interface.md):

-   Stub do cliente (nome \_ c.c)
-   Stub do servidor \_ (nome s.c)
-   Arquivo de cabeça (name.h)

Quando o [**atributo**](object.md) de objeto aparece na lista de atributos de interface, o compilador gera os seguintes arquivos para uma interface COM:

-   Arquivo proxy de interface (nome \_ p.c)
-   Arquivo de header da interface (name.h)
-   Arquivo UUID de interface (nome \_ I.c)

Quando o [**atributo local**](local.md) aparece na lista de atributos de interface, o compilador gera apenas o arquivo de header da interface, Name.h.

O compilador MIDL fornecido com o Microsoft RPC invoca o pré-processador C conforme necessário para processar o arquivo IDL. Ele não invoca automaticamente o compilador C para compilar arquivos gerados.

> [!Note]  
> O compilador MIDL fornecido com o Microsoft RPC usa uma sintaxe de linha de comando diferente do compilador de IDL de DCE.

 

O compilador MIDL alterna [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) afetam o arquivo stub do servidor.

A partir do MIDL versão 6.0.359, a opção de linha de comando padrão para o compilador MIDL é [**/Oicf**](-oi.md)Â [**/robust.**](-robust.md) Para desabilitar /robust, especifique a [**opção /no \_ robust.**](-no-robust.md)

## <a name="the-header-file"></a>O arquivo de header

O arquivo de header contém definições de todos os tipos de dados e operações declarados no arquivo IDL. O arquivo de header deve ser incluído por todos os módulos de aplicativo que chamam as operações definidas, implementam as operações definidas ou manipulam os tipos definidos.

As opções [**/header**](-header.md) e [**/out**](-out.md) do compilador MIDL afetam o arquivo de header.

 

 




