---
title: Componentes MIDLRT e Windows Runtime
description: Mostra como criar arquivos de metadados (. winmd) que representam a API para componentes de Windows Runtime personalizados.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- MIDL do compilador MIDL
- MIDL do compilador MIDL, MIDL e Windows Runtime winrt
- MIDL de Windows Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104499187"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="ff66c-106">Componentes MIDLRT e Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="ff66c-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="ff66c-107">Mostra como criar arquivos de metadados (. winmd) que representam a API para componentes de Windows Runtime personalizados.</span><span class="sxs-lookup"><span data-stu-id="ff66c-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="ff66c-108">Use o compilador MIDLRT para compilar arquivos de metadados (. winmd) para seus componentes de Windows Runtime personalizados.</span><span class="sxs-lookup"><span data-stu-id="ff66c-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="ff66c-109">Quando os arquivos de metadados são gerados, você pode redação-los em um pacote mais eficiente usando o utilitário MDMERGE.</span><span class="sxs-lookup"><span data-stu-id="ff66c-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="ff66c-110">Para obter mais informações, consulte [MDMERGE e arquivos de metadados](mdmerge-and-metadata-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff66c-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="ff66c-111">O uso de MIDLRT é semelhante ao uso do compilador MIDL.</span><span class="sxs-lookup"><span data-stu-id="ff66c-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="ff66c-112">Execute MIDLRT na linha de comando usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="ff66c-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="ff66c-113">**midlrt**  *<* **Opções** _>_ do **nome do arquivo. idl**</span><span class="sxs-lookup"><span data-stu-id="ff66c-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="ff66c-114">onde **as opções** \* < \* _>_ representam as opções de linha de comando que você deseja usar e filename. idl é o nome do arquivo IDL a ser compilado.</span><span class="sxs-lookup"><span data-stu-id="ff66c-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="ff66c-115">A lista a seguir mostra as opções de linha de comando que o MIDLRT.EXE usa.</span><span class="sxs-lookup"><span data-stu-id="ff66c-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="ff66c-116">**\_classe/enum**</span><span class="sxs-lookup"><span data-stu-id="ff66c-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="ff66c-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="ff66c-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="ff66c-118">**/nomidl**</span><span class="sxs-lookup"><span data-stu-id="ff66c-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="ff66c-119">**/nomd**</span><span class="sxs-lookup"><span data-stu-id="ff66c-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="ff66c-120">**\_prefixo/NS**</span><span class="sxs-lookup"><span data-stu-id="ff66c-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="ff66c-121">**/winmd**</span><span class="sxs-lookup"><span data-stu-id="ff66c-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="ff66c-122">**/winrt**</span><span class="sxs-lookup"><span data-stu-id="ff66c-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="ff66c-123">Uma lista completa dos comutadores e opções do compilador MIDLRT está disponível quando você usa o compilador MIDLRT [**/Help**](-help-.md) e/?</span><span class="sxs-lookup"><span data-stu-id="ff66c-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="ff66c-124">comutadores.</span><span class="sxs-lookup"><span data-stu-id="ff66c-124">switches.</span></span> <span data-ttu-id="ff66c-125">As opções são organizadas por categorias.</span><span class="sxs-lookup"><span data-stu-id="ff66c-125">The switches are organized by categories.</span></span> <span data-ttu-id="ff66c-126">Para obter mais informações, consulte a [referência de Command-Line MIDL](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="ff66c-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff66c-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff66c-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff66c-128">MDMERGE e arquivos de metadados</span><span class="sxs-lookup"><span data-stu-id="ff66c-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




