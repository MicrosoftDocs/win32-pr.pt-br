---
description: Demonstra como implementar uma extensão de namespace de Shell, incluindo o comportamento do menu de contexto e tarefas personalizadas no navegador.
title: Exemplo de provedor de dados do Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171550"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="51d9f-103">Exemplo de provedor de dados do Explorer</span><span class="sxs-lookup"><span data-stu-id="51d9f-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="51d9f-104">Demonstra como implementar uma extensão de namespace de Shell, incluindo o comportamento do menu de contexto e tarefas personalizadas no navegador.</span><span class="sxs-lookup"><span data-stu-id="51d9f-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="51d9f-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="51d9f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="51d9f-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51d9f-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="51d9f-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="51d9f-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="51d9f-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="51d9f-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="51d9f-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="51d9f-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="51d9f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51d9f-110">Requirements</span></span>



| <span data-ttu-id="51d9f-111">Produto</span><span class="sxs-lookup"><span data-stu-id="51d9f-111">Product</span></span>                                | <span data-ttu-id="51d9f-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="51d9f-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="51d9f-113">Windows</span><span class="sxs-lookup"><span data-stu-id="51d9f-113">Windows</span></span>                                | <span data-ttu-id="51d9f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51d9f-114">Windows Vista</span></span>           |
| <span data-ttu-id="51d9f-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="51d9f-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="51d9f-116">6.1</span><span class="sxs-lookup"><span data-stu-id="51d9f-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="51d9f-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="51d9f-117">Downloading the Sample</span></span>

| <span data-ttu-id="51d9f-118">Localização</span><span class="sxs-lookup"><span data-stu-id="51d9f-118">Location</span></span>      | <span data-ttu-id="51d9f-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="51d9f-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d9f-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="51d9f-120">GitHub</span></span>  | [<span data-ttu-id="51d9f-121">Exemplo de ExplorerDataProvider</span><span class="sxs-lookup"><span data-stu-id="51d9f-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="51d9f-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="51d9f-122">Building the Sample</span></span>

<span data-ttu-id="51d9f-123">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="51d9f-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="51d9f-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="51d9f-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="51d9f-125">Digite `msbuild ExplorerDataProvider.sln`.</span><span class="sxs-lookup"><span data-stu-id="51d9f-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="51d9f-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="51d9f-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="51d9f-127">Abra o Windows Explorer e navegue até o diretório do projeto **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="51d9f-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="51d9f-128">Clique duas vezes no ícone do arquivo ExplorerDataProvider. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="51d9f-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="51d9f-129">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="51d9f-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="51d9f-130">A DLL será criada no diretório padrão de \\ depuração ou de \\ liberação.</span><span class="sxs-lookup"><span data-stu-id="51d9f-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="51d9f-131">Na versão deste exemplo incluída no SDK do Windows, a configuração para a compilação de versão de 64 bits não inclui o arquivo ExplorerDataProvider. def na opção de **arquivo de definição de módulo** do vinculador.</span><span class="sxs-lookup"><span data-stu-id="51d9f-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="51d9f-132">Você deve especificar esse arquivo antes de Compilar em um ambiente de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="51d9f-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="51d9f-133">Adicione a linha `ModuleDefinitionFile="ExplorerDataProvider.def"` à seção VCLinkerTool (começa na linha 329) do arquivo ExplorerDataProvider. vcproj, como mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="51d9f-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="51d9f-134">A versão deste exemplo baixável da Galeria de códigos foi corrigida para esse problema e nenhuma ação extra é necessária em sua parte.</span><span class="sxs-lookup"><span data-stu-id="51d9f-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="51d9f-135">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="51d9f-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="51d9f-136">Navegue até o diretório que contém o novo arquivo. dll e. propDesc, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="51d9f-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="51d9f-137">Na linha de comando, digite `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="51d9f-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="51d9f-138">Se você executar esse comando em um prompt de comando elevado, o registro automático também registrará o arquivo. propDesc automaticamente.</span><span class="sxs-lookup"><span data-stu-id="51d9f-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="51d9f-139">Se ele for executado de um prompt de comando sem privilégios elevados, a extensão do namespace funcionará, mas sem a funcionalidade de propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="51d9f-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="51d9f-140">Abra a pasta **meu computador** e procure a nova extensão de namespace presente nela.</span><span class="sxs-lookup"><span data-stu-id="51d9f-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>


