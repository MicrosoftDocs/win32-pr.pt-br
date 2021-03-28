---
description: Demonstra como usar os métodos de interface IFileOperationProgressSink para monitorar os detalhes das ações da interface IFileOperation.
title: Coletor do andamento da operação de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011185"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="8be6a-103">Coletor do andamento da operação de arquivo</span><span class="sxs-lookup"><span data-stu-id="8be6a-103">File Operation Progress Sink</span></span>

<span data-ttu-id="8be6a-104">Demonstra como usar os métodos de interface [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) para monitorar os detalhes das ações da interface [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .</span><span class="sxs-lookup"><span data-stu-id="8be6a-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="8be6a-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8be6a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8be6a-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be6a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8be6a-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="8be6a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="8be6a-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="8be6a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="8be6a-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="8be6a-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="8be6a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8be6a-110">Requirements</span></span>



| <span data-ttu-id="8be6a-111">Produto</span><span class="sxs-lookup"><span data-stu-id="8be6a-111">Product</span></span>                                | <span data-ttu-id="8be6a-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="8be6a-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="8be6a-113">Windows</span><span class="sxs-lookup"><span data-stu-id="8be6a-113">Windows</span></span>                                | <span data-ttu-id="8be6a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8be6a-114">Windows Vista</span></span>           |
| <span data-ttu-id="8be6a-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="8be6a-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="8be6a-116">6.1</span><span class="sxs-lookup"><span data-stu-id="8be6a-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="8be6a-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="8be6a-117">Downloading the Sample</span></span>

| <span data-ttu-id="8be6a-118">Localização</span><span class="sxs-lookup"><span data-stu-id="8be6a-118">Location</span></span>      | <span data-ttu-id="8be6a-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="8be6a-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8be6a-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="8be6a-120">GitHub</span></span>  | [<span data-ttu-id="8be6a-121">Exemplo de FileOperationProgressSink</span><span class="sxs-lookup"><span data-stu-id="8be6a-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="8be6a-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="8be6a-122">Building the Sample</span></span>

<span data-ttu-id="8be6a-123">Para criar o exemplo na janela de prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="8be6a-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="8be6a-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **FileOperationProgressSink** .</span><span class="sxs-lookup"><span data-stu-id="8be6a-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="8be6a-125">Digite `msbuild FileOperationProgressSinkSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="8be6a-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="8be6a-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="8be6a-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="8be6a-127">Abra o Windows Explorer e navegue até o diretório do projeto **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="8be6a-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="8be6a-128">Por exemplo, o caminho de instalação padrão completo é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .</span><span class="sxs-lookup"><span data-stu-id="8be6a-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="8be6a-129">Clique duas vezes no ícone do arquivo FileOperationProgressSinkSample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8be6a-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="8be6a-130">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="8be6a-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="8be6a-131">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="8be6a-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="8be6a-132">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="8be6a-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="8be6a-133">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="8be6a-133">Running the Sample</span></span>

1.  <span data-ttu-id="8be6a-134">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="8be6a-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="8be6a-135">No prompt de comando, digite `FileOperationProgressSinkSample.exe` ou, no Windows Explorer, clique duas vezes no ícone para FileOperationProgressSinkSample.exe.</span><span class="sxs-lookup"><span data-stu-id="8be6a-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 



