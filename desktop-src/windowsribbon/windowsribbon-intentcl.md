---
title: Compilando marcação da faixa de medida
description: Para que o Windows Ribbon Framework consuma o arquivo de marcação da faixa de faixas, o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Faixa de-se do Windows, compilando marcação
- Faixa de faixas, compilando marcação
- Faixa de da de Windows, fluxo de trabalho do compilador
- Faixa de medida, fluxo de trabalho do compilador
- Windows Ribbon, compilador de comando de interface do usuário (UICC.exe)
- Faixa de comandos, compilador de comando de interface do usuário (UICC.exe)
- Compilador de comando de interface do usuário (UICC.exe)
- UICC.exe (compilador de comando de interface do usuário)
- Compilando a marcação da faixa de da Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498764"
---
# <a name="compiling-ribbon-markup"></a><span data-ttu-id="7b52f-112">Compilando marcação da faixa de medida</span><span class="sxs-lookup"><span data-stu-id="7b52f-112">Compiling Ribbon Markup</span></span>

<span data-ttu-id="7b52f-113">Para que o Windows Ribbon Framework consuma o arquivo de [marcação da faixa de faixas](windowsribbon-schema.md) , o arquivo de marcação deve ser compilado em um arquivo de recurso de formato binário.</span><span class="sxs-lookup"><span data-stu-id="7b52f-113">For the Windows Ribbon framework to consume the [Ribbon markup](windowsribbon-schema.md) file, the markup file must be compiled into a binary format resource file.</span></span> <span data-ttu-id="7b52f-114">Um compilador de marcação dedicado, o UICC (compilador de comando de interface do usuário), está incluído no SDK (Software Development Kit) do Windows (7,0 ou posterior) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="7b52f-114">A dedicated markup compiler, the UI Command Compiler (UICC), is included with the Windows Software Development Kit (SDK) (7.0 or later) for this purpose.</span></span> <span data-ttu-id="7b52f-115">Além de compilar a versão binária da marcação, o UICC gera um arquivo de cabeçalho de definição de ID (. h) que expõe todos os elementos de marcação para o aplicativo host da faixa de versões e um arquivo de recurso (. rc) que é usado para vincular recursos de imagem e de cadeia de caracteres ao aplicativo host no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="7b52f-115">In addition to compiling the binary version of the markup, the UICC generates an ID definition header (.h) file that exposes all markup elements to the Ribbon host application and a resource (.rc) file that is used to link image and string resources to the host application at build time.</span></span>

-   [<span data-ttu-id="7b52f-116">Fluxo de trabalho do compilador</span><span class="sxs-lookup"><span data-stu-id="7b52f-116">Compiler Workflow</span></span>](#compiler-workflow)
-   [<span data-ttu-id="7b52f-117">Sintaxe de linha de comando</span><span class="sxs-lookup"><span data-stu-id="7b52f-117">Command-Line Syntax</span></span>](#command-line-syntax)
    -   [<span data-ttu-id="7b52f-118">Argumentos e opções</span><span class="sxs-lookup"><span data-stu-id="7b52f-118">Arguments and Options</span></span>](#arguments-and-options)
    -   [<span data-ttu-id="7b52f-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7b52f-119">Example</span></span>](#example)
-   [<span data-ttu-id="7b52f-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b52f-120">Related topics</span></span>](#related-topics)

## <a name="compiler-workflow"></a><span data-ttu-id="7b52f-121">Fluxo de trabalho do compilador</span><span class="sxs-lookup"><span data-stu-id="7b52f-121">Compiler Workflow</span></span>

<span data-ttu-id="7b52f-122">O fluxo de trabalho do compilador de marcação da faixa de opções é ilustrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b52f-122">The workflow of the Ribbon markup compiler is illustrated in the following diagram.</span></span>

![diagrama mostrando o fluxo de trabalho do compilador de marcação da faixa de Ribbon.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a><span data-ttu-id="7b52f-124">Sintaxe da linha de comando</span><span class="sxs-lookup"><span data-stu-id="7b52f-124">Command-Line Syntax</span></span>

<span data-ttu-id="7b52f-125">A sintaxe de linha de comando para o compilador de marcação da faixa de opções é mostrada no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b52f-125">The command-line syntax for the Ribbon markup compiler is shown in the following example.</span></span>


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a><span data-ttu-id="7b52f-126">Argumentos e opções</span><span class="sxs-lookup"><span data-stu-id="7b52f-126">Arguments and Options</span></span>

<span data-ttu-id="7b52f-127">Os argumentos e as opções para essa ferramenta são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7b52f-127">The arguments and options for this tool are described in the following table.</span></span>

> [!Note]  
> <span data-ttu-id="7b52f-128">As opções de linha de comando listadas devem ser especificadas na ordem especificada.</span><span class="sxs-lookup"><span data-stu-id="7b52f-128">The command-line options listed must be specified in the order given.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b52f-129">Opção</span><span class="sxs-lookup"><span data-stu-id="7b52f-129">Option</span></span></th>
<th><span data-ttu-id="7b52f-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="7b52f-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b52f-131">verga<headerFile></span><span class="sxs-lookup"><span data-stu-id="7b52f-131">/header:<headerFile></span></span></td>
<td><span data-ttu-id="7b52f-132">Gere um arquivo de cabeçalho chamado <headerFile> que contenha os símbolos de recurso de ID de comando de marcação.</span><span class="sxs-lookup"><span data-stu-id="7b52f-132">Generate a header file called <headerFile> that contains the markup Command ID resource symbols.</span></span> <span data-ttu-id="7b52f-133">Se omitido, um arquivo de cabeçalho não será gerado.</span><span class="sxs-lookup"><span data-stu-id="7b52f-133">If omitted, a header file is not generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b52f-134">/res<resourceFile></span><span class="sxs-lookup"><span data-stu-id="7b52f-134">/res:<resourceFile></span></span></td>
<td><span data-ttu-id="7b52f-135">Gerar um arquivo de recurso chamado <resourceFile> que vincula todos os recursos de imagem e de cadeia de caracteres, o arquivo de marcação binária e o arquivo de cabeçalho ao aplicativo host no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="7b52f-135">Generate a resource file called <resourceFile> that links all image and string resources, the binary markup file, and the header file to the host application at build time.</span></span> <span data-ttu-id="7b52f-136">Se omitido, um arquivo de recurso não será gerado.</span><span class="sxs-lookup"><span data-stu-id="7b52f-136">If omitted, a resource file is not generated.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b52f-137">/Name<ribbonName></span><span class="sxs-lookup"><span data-stu-id="7b52f-137">/name:<ribbonName></span></span></td>
<td><span data-ttu-id="7b52f-138">O nome do recurso para o arquivo de marcação binária que é registrado no <resourceFile> .</span><span class="sxs-lookup"><span data-stu-id="7b52f-138">The resource name for the binary markup file that is logged in the <resourceFile>.</span></span> <span data-ttu-id="7b52f-139">O padrão é APPLICATION_RIBBON.</span><span class="sxs-lookup"><span data-stu-id="7b52f-139">The default is APPLICATION_RIBBON.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b52f-140">/W{0\1\2}</span><span class="sxs-lookup"><span data-stu-id="7b52f-140">/W{0\1\2}</span></span></td>
<td><span data-ttu-id="7b52f-141">Filtre as mensagens de evento com base na severidade.</span><span class="sxs-lookup"><span data-stu-id="7b52f-141">Filter the event messages based on severity.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7b52f-142">0</span><span class="sxs-lookup"><span data-stu-id="7b52f-142">0</span></span><br/></td>
<td><span data-ttu-id="7b52f-143">Mensagens de erro somente.</span><span class="sxs-lookup"><span data-stu-id="7b52f-143">Error messages only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b52f-144">1</span><span class="sxs-lookup"><span data-stu-id="7b52f-144">1</span></span><br/></td>
<td><span data-ttu-id="7b52f-145">Mensagens de erro e de aviso apenas.</span><span class="sxs-lookup"><span data-stu-id="7b52f-145">Error and Warning messages only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b52f-146"><strong>2</strong></span><span class="sxs-lookup"><span data-stu-id="7b52f-146"><strong>2</strong></span></span><br/></td>
<td><span data-ttu-id="7b52f-147">Padrão.</span><span class="sxs-lookup"><span data-stu-id="7b52f-147">Default.</span></span> <br/> <span data-ttu-id="7b52f-148">Mensagens de erro, aviso e informativas.</span><span class="sxs-lookup"><span data-stu-id="7b52f-148">Error, Warning, and Informational messages.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a><span data-ttu-id="7b52f-149">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7b52f-149">Example</span></span>

<span data-ttu-id="7b52f-150">O exemplo a seguir demonstra como usar o compilador de marcação da faixa de opções para gerar um conjunto típico de arquivos de recurso para um aplicativo da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="7b52f-150">The following example demonstrates how to use the Ribbon markup compiler to generate a typical set of resource files for a Ribbon application.</span></span>

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a><span data-ttu-id="7b52f-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b52f-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b52f-152">Declarando comandos e controles com marcação de faixa de medida</span><span class="sxs-lookup"><span data-stu-id="7b52f-152">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="7b52f-153">Criando um aplicativo de faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="7b52f-153">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





