---
title: MDMERGE e arquivos de metadados
description: Compõe vários arquivos de metadados (. winmd) em um número de arquivos de metadados de saída, com base no namespace.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- arquivo winmd
- Metadados do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916005"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="f1aca-106">MDMERGE e arquivos de metadados</span><span class="sxs-lookup"><span data-stu-id="f1aca-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="f1aca-107">Compõe vários arquivos de metadados (. winmd) em um número de arquivos de metadados de saída, com base no namespace.</span><span class="sxs-lookup"><span data-stu-id="f1aca-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="f1aca-108">Uso</span><span class="sxs-lookup"><span data-stu-id="f1aca-108">Usage</span></span>

<span data-ttu-id="f1aca-109">Execute MDMERGE na linha de comando usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="f1aca-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="f1aca-110"> *< ***Opções*** de mdmerge>*</span><span class="sxs-lookup"><span data-stu-id="f1aca-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="f1aca-111">em que *< ***Opções*** >* representa as opções de linha de comando que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="f1aca-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="f1aca-112">Gere arquivos de metadados para seus componentes de Windows Runtime personalizados usando o compilador MIDLRT.</span><span class="sxs-lookup"><span data-stu-id="f1aca-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="f1aca-113">Para obter mais informações, consulte [MIDLRT and Windows Runtime Components](midlrt-and-windows-runtime-components.md).</span><span class="sxs-lookup"><span data-stu-id="f1aca-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="f1aca-114">Opções de linha de comando</span><span class="sxs-lookup"><span data-stu-id="f1aca-114">Command-line switches</span></span>

<span data-ttu-id="f1aca-115">A lista a seguir mostra as opções de linha de comando que o MDMERGE usa.</span><span class="sxs-lookup"><span data-stu-id="f1aca-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="f1aca-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="f1aca-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="f1aca-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="f1aca-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="f1aca-118">**opção**</span><span class="sxs-lookup"><span data-stu-id="f1aca-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="f1aca-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="f1aca-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="f1aca-120">**/partial**</span><span class="sxs-lookup"><span data-stu-id="f1aca-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="f1aca-121">**/v**</span><span class="sxs-lookup"><span data-stu-id="f1aca-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="f1aca-122">Uma lista completa dos comutadores e opções do compilador MDMERGE está disponível quando você usa **-h** e **/?**</span><span class="sxs-lookup"><span data-stu-id="f1aca-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="f1aca-123">comutadores.</span><span class="sxs-lookup"><span data-stu-id="f1aca-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1aca-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1aca-124">Remarks</span></span>

<span data-ttu-id="f1aca-125">A composição de metadados permite que vários arquivos IDL contenham definições para Windows Runtime componentes no mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="f1aca-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="f1aca-126">Isso libera você da definição de todos os tipos em um namespace dentro de um único arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f1aca-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="f1aca-127">É provável que você tenha vários componentes Windows Runtime que seus aplicativos usam.</span><span class="sxs-lookup"><span data-stu-id="f1aca-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="f1aca-128">Ao executar a etapa final para produzir assemblies de metadados implantáveis Windows Runtime, você pode configurar o MDMERGE para mesclar componentes de vários diretórios de metadados, como aqueles que são instalados com o sistema (% WINDOWS% \\ System32 \\ WinMetadata), seus tipos de base e o diretório de Build do projeto atual.</span><span class="sxs-lookup"><span data-stu-id="f1aca-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="f1aca-129">Todos os tipos necessários são mesclados nos assemblies de metadados corretos, implantáveis, que você pode empacotar para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f1aca-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="f1aca-130">Você pode usar a opção [**/n**](-mdmerge-n.md) para especificar a profundidade de namespace com suporte para compor assemblies de metadados.</span><span class="sxs-lookup"><span data-stu-id="f1aca-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="f1aca-131">Isso permite configurar uma divisão a quente para seus componentes de Windows Runtime, de modo que apenas um único arquivo. winmd seja empacotado em vez de muitos.</span><span class="sxs-lookup"><span data-stu-id="f1aca-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="f1aca-132">Isso reduz os tempos de carregamento e a e/s de arquivo exigidos por seus aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f1aca-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1aca-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1aca-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1aca-134">Componentes MIDLRT e Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="f1aca-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




