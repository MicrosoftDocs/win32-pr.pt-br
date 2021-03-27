---
description: Demonstra como personalizar o arquivo na caixa de diálogo usar para exibir informações e opções adicionais para arquivos que estão abertos no momento no aplicativo.
title: Exemplo do arquivo em uso
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 22EFE7CC-D223-46b3-BD6B-293E3FA0BA01
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223e0addf201f3526654a17346963b4639e0d215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296834"
---
# <a name="file-is-in-use-sample"></a><span data-ttu-id="542a9-103">Exemplo do arquivo em uso</span><span class="sxs-lookup"><span data-stu-id="542a9-103">File Is In Use Sample</span></span>

<span data-ttu-id="542a9-104">Demonstra como personalizar o **arquivo na caixa de diálogo usar** para exibir informações e opções adicionais para arquivos que estão abertos no momento no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="542a9-104">Demonstrates how to customize the **File In Use** dialog to display additional information and options for files that are currently opened in the application.</span></span>

<span data-ttu-id="542a9-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="542a9-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="542a9-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="542a9-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="542a9-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="542a9-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="542a9-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="542a9-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="542a9-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="542a9-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="542a9-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="542a9-110">Requirements</span></span>



| <span data-ttu-id="542a9-111">Produto</span><span class="sxs-lookup"><span data-stu-id="542a9-111">Product</span></span>                                | <span data-ttu-id="542a9-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="542a9-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="542a9-113">Windows</span><span class="sxs-lookup"><span data-stu-id="542a9-113">Windows</span></span>                                | <span data-ttu-id="542a9-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="542a9-114">Windows Vista</span></span>           |
| <span data-ttu-id="542a9-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="542a9-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="542a9-116">6.1</span><span class="sxs-lookup"><span data-stu-id="542a9-116">6.1</span></span>                     |



 

<span data-ttu-id="542a9-117">Para obter requisitos adicionais, consulte o \_ arquivo IFileIsInUsesample.docx incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="542a9-117">For additional requirements, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="542a9-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="542a9-118">Downloading the Sample</span></span>

| <span data-ttu-id="542a9-119">Localização</span><span class="sxs-lookup"><span data-stu-id="542a9-119">Location</span></span>      | <span data-ttu-id="542a9-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="542a9-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542a9-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="542a9-121">GitHub</span></span>  | [<span data-ttu-id="542a9-122">Exemplo de FileIsInUse</span><span class="sxs-lookup"><span data-stu-id="542a9-122">FileIsInUse sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse) |

## <a name="building-the-sample"></a><span data-ttu-id="542a9-123">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="542a9-123">Building the Sample</span></span>

<span data-ttu-id="542a9-124">Para criar o exemplo na janela de prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="542a9-124">To build the sample from the Command Prompt window:</span></span>

1.  <span data-ttu-id="542a9-125">Abra a janela do prompt de comando e navegue até o diretório do projeto **FileIsInUse** .</span><span class="sxs-lookup"><span data-stu-id="542a9-125">Open the Command Prompt window and navigate to the **FileIsInUse** project directory.</span></span>
2.  <span data-ttu-id="542a9-126">Digite `msbuild FileIsInUse.sln`.</span><span class="sxs-lookup"><span data-stu-id="542a9-126">Enter `msbuild FileIsInUse.sln`.</span></span>

<span data-ttu-id="542a9-127">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="542a9-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="542a9-128">Abra o Windows Explorer e navegue até o diretório do projeto **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="542a9-128">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="542a9-129">Por exemplo, o caminho de instalação padrão completo é `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse` .</span><span class="sxs-lookup"><span data-stu-id="542a9-129">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileIsInUse`.</span></span>
2.  <span data-ttu-id="542a9-130">Clique duas vezes no ícone do arquivo FileIsInUseSample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="542a9-130">Double-click the icon for the FileIsInUseSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="542a9-131">A extensão de nome de arquivo. sln não é mostrada em configurações de pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="542a9-131">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="542a9-132">Nessa situação, ela pode ser identificada por seu ícone exclusivo ou por sua descrição de tipo, "solução de Microsoft Visual Studio".</span><span class="sxs-lookup"><span data-stu-id="542a9-132">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="542a9-133">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="542a9-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="542a9-134">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="542a9-134">Running the Sample</span></span>

1.  <span data-ttu-id="542a9-135">Navegue até o diretório que contém o novo executável, usando a janela de prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="542a9-135">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="542a9-136">No prompt de comando, digite `FileIsInUseSample.exe` ou, no Windows Explorer, clique duas vezes no ícone para FileIsInUseSample.exe.</span><span class="sxs-lookup"><span data-stu-id="542a9-136">At the command prompt, enter `FileIsInUseSample.exe`, or from Windows Explorer, double-click the icon for FileIsInUseSample.exe.</span></span>

<span data-ttu-id="542a9-137">Para obter informações detalhadas sobre este exemplo de código, consulte o \_ arquivo IFileIsInUsesample.docx incluído com o exemplo.</span><span class="sxs-lookup"><span data-stu-id="542a9-137">For detailed information about this code sample, see the IFileIsInUse\_sample.docx file included with the sample.</span></span>

 

 



