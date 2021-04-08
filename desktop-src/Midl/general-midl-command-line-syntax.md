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
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="fe91b-104">Sintaxe de linha de comando MIDL geral</span><span class="sxs-lookup"><span data-stu-id="fe91b-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="fe91b-105">O compilador MIDL processa um arquivo IDL e um arquivo de configuração de aplicativo opcional (ACF) para gerar um conjunto de arquivos de saída.</span><span class="sxs-lookup"><span data-stu-id="fe91b-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="fe91b-106">Os atributos especificados na lista de atributos da interface do arquivo IDL determinam se o compilador gera arquivos de origem para uma interface RPC ou para uma interface OLE personalizada.</span><span class="sxs-lookup"><span data-stu-id="fe91b-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="fe91b-107">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="fe91b-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="fe91b-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*opção de linha de comando*</span><span class="sxs-lookup"><span data-stu-id="fe91b-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="fe91b-109">Especifica opções de linha de comando do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="fe91b-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="fe91b-110">As opções podem aparecer em qualquer sequência.</span><span class="sxs-lookup"><span data-stu-id="fe91b-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="fe91b-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*opções de opção*</span><span class="sxs-lookup"><span data-stu-id="fe91b-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="fe91b-112">Especifica as opções associadas a cada comutador.</span><span class="sxs-lookup"><span data-stu-id="fe91b-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="fe91b-113">As opções válidas são descritas na entrada de referência para cada comutador de compilador de MIDL.</span><span class="sxs-lookup"><span data-stu-id="fe91b-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="fe91b-114"><span id="filename"></span><span id="FILENAME"></span>*nome do arquivo*</span><span class="sxs-lookup"><span data-stu-id="fe91b-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="fe91b-115">Especifica o nome do arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fe91b-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="fe91b-116">Normalmente, esse arquivo tem a extensão. idl, mas ele pode ter outro ou nenhum.</span><span class="sxs-lookup"><span data-stu-id="fe91b-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fe91b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe91b-117">Remarks</span></span>

<span data-ttu-id="fe91b-118">As listas a seguir mostram os nomes padrão dos arquivos gerados para um arquivo IDL chamado name. idl.</span><span class="sxs-lookup"><span data-stu-id="fe91b-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="fe91b-119">Você pode usar opções de linha de comando para substituir esses nomes padrão.</span><span class="sxs-lookup"><span data-stu-id="fe91b-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="fe91b-120">Observe que o nome do arquivo IDL pode ter uma extensão diferente de. IDL ou nenhuma extensão.</span><span class="sxs-lookup"><span data-stu-id="fe91b-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="fe91b-121">Por padrão (ou seja, se a lista de atributos de interface não contiver o [**objeto**](object.md) ou o atributo [**local**](local.md) ), o compilador gerará os seguintes arquivos para uma [interface RPC](files-generated-for-an-rpc-interface.md):</span><span class="sxs-lookup"><span data-stu-id="fe91b-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="fe91b-122">Stub do cliente (nome \_ c. c)</span><span class="sxs-lookup"><span data-stu-id="fe91b-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="fe91b-123">Stub do servidor (nome \_ s. c)</span><span class="sxs-lookup"><span data-stu-id="fe91b-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="fe91b-124">Arquivo de cabeçalho (Name. h)</span><span class="sxs-lookup"><span data-stu-id="fe91b-124">Header file (name.h)</span></span>

<span data-ttu-id="fe91b-125">Quando o atributo de [**objeto**](object.md) aparece na lista de atributos de interface, o compilador gera os seguintes arquivos para uma interface com:</span><span class="sxs-lookup"><span data-stu-id="fe91b-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="fe91b-126">Arquivo de proxy da interface (nome \_ p. c)</span><span class="sxs-lookup"><span data-stu-id="fe91b-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="fe91b-127">Arquivo de cabeçalho de interface (Name. h)</span><span class="sxs-lookup"><span data-stu-id="fe91b-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="fe91b-128">Arquivo UUID da interface (name \_ I. c)</span><span class="sxs-lookup"><span data-stu-id="fe91b-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="fe91b-129">Quando o atributo [**local**](local.md) aparece na lista atributo de interface, o compilador gera apenas o arquivo de cabeçalho de interface, Name. h.</span><span class="sxs-lookup"><span data-stu-id="fe91b-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="fe91b-130">O compilador MIDL fornecido com o Microsoft RPC invoca o pré-processador C conforme necessário para processar o arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fe91b-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="fe91b-131">Ele não invoca automaticamente o compilador C para compilar arquivos gerados.</span><span class="sxs-lookup"><span data-stu-id="fe91b-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="fe91b-132">O compilador MIDL fornecido com o Microsoft RPC usa uma sintaxe de linha de comando diferente do compilador de IDL do DCE.</span><span class="sxs-lookup"><span data-stu-id="fe91b-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="fe91b-133">O compilador MIDL alterna [**/env**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) afeta o arquivo stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="fe91b-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="fe91b-134">Começando com o MIDL versão 6.0.359, a opção de linha de comando padrão para o compilador MIDL é [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span><span class="sxs-lookup"><span data-stu-id="fe91b-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="fe91b-135">Para desabilitar o/robust, especifique a opção [**// \_ robusta**](-no-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="fe91b-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="fe91b-136">O arquivo de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe91b-136">The Header File</span></span>

<span data-ttu-id="fe91b-137">O arquivo de cabeçalho contém definições de todos os tipos de dados e operações declaradas no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="fe91b-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="fe91b-138">O arquivo de cabeçalho deve ser incluído por todos os módulos de aplicativo que chamam as operações definidas, implementar as operações definidas ou manipular os tipos definidos.</span><span class="sxs-lookup"><span data-stu-id="fe91b-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="fe91b-139">O compilador MIDL alterna [**/header**](-header.md) e [**/out**](-out.md) afeta o arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="fe91b-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




