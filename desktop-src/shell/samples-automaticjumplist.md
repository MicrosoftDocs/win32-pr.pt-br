---
description: Demonstra como adicionar itens à lista de atalhos automática para um aplicativo, incluindo a alternância entre a exibição das categorias frequentes e recentes.
title: Exemplo de lista de atalhos automática
ms.topic: article
ms.date: 05/31/2018
ms.assetid: C33152FE-1322-42f8-A656-3D5FAF4B612D
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ce0b6520163fcb07bb990b7a5a9fe742d976a899
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461270"
---
# <a name="automatic-jump-list-sample"></a><span data-ttu-id="daff2-103">Exemplo de lista de atalhos automática</span><span class="sxs-lookup"><span data-stu-id="daff2-103">Automatic Jump List Sample</span></span>

<span data-ttu-id="daff2-104">Demonstra como adicionar itens à lista de atalhos automática para um aplicativo, incluindo a alternância entre a exibição das categorias frequentes e recentes.</span><span class="sxs-lookup"><span data-stu-id="daff2-104">Demonstrates how to add items to the automatic Jump List for an application, including switching between the display of the Frequent and Recent categories.</span></span>

<span data-ttu-id="daff2-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="daff2-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="daff2-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daff2-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="daff2-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="daff2-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="daff2-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="daff2-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="daff2-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="daff2-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="daff2-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="daff2-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="daff2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="daff2-111">Requirements</span></span>



| <span data-ttu-id="daff2-112">Produto</span><span class="sxs-lookup"><span data-stu-id="daff2-112">Product</span></span>                                | <span data-ttu-id="daff2-113">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="daff2-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="daff2-114">Windows</span><span class="sxs-lookup"><span data-stu-id="daff2-114">Windows</span></span>                                | <span data-ttu-id="daff2-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="daff2-115">Windows 7</span></span>               |
| <span data-ttu-id="daff2-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="daff2-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="daff2-117">7.0</span><span class="sxs-lookup"><span data-stu-id="daff2-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="daff2-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="daff2-118">Downloading the Sample</span></span>

| <span data-ttu-id="daff2-119">Localização</span><span class="sxs-lookup"><span data-stu-id="daff2-119">Location</span></span>      | <span data-ttu-id="daff2-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="daff2-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daff2-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="daff2-121">GitHub</span></span>  | [<span data-ttu-id="daff2-122">Exemplo de AutomaticJumpList</span><span class="sxs-lookup"><span data-stu-id="daff2-122">AutomaticJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AutomaticJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="daff2-123">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="daff2-123">Building the Sample</span></span>

<span data-ttu-id="daff2-124">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="daff2-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="daff2-125">Abra a janela do prompt de comando e navegue até o diretório do projeto **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="daff2-125">Open the command prompt window and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="daff2-126">Digite `msbuild AutomaticJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="daff2-126">Enter `msbuild AutomaticJumpListSample.sln`.</span></span>

<span data-ttu-id="daff2-127">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="daff2-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="daff2-128">Abra o Windows Explorer e navegue até o diretório do projeto **AutomaticJumpList** .</span><span class="sxs-lookup"><span data-stu-id="daff2-128">Open Windows Explorer and navigate to the **AutomaticJumpList** project directory.</span></span>
2.  <span data-ttu-id="daff2-129">Clique duas vezes no ícone do arquivo AutomaticJumpListSample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="daff2-129">Double-click the icon for the AutomaticJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="daff2-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="daff2-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="daff2-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="daff2-131">Running the Sample</span></span>

1.  <span data-ttu-id="daff2-132">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="daff2-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="daff2-133">Na linha de comando, digite `AutomaticJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="daff2-133">At the command line, enter `AutomaticJumpListSample.exe`.</span></span> <span data-ttu-id="daff2-134">Como alternativa, no Windows Explorer, clique duas vezes no ícone para AutomaticJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="daff2-134">Alternatively, from Windows Explorer double-click the icon for AutomaticJumpListSample.exe.</span></span>
3.  <span data-ttu-id="daff2-135">Este exemplo deve ser executado como administrador na primeira vez em que for executado para que ele possa instalar os registros de tipo de arquivo necessários.</span><span class="sxs-lookup"><span data-stu-id="daff2-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="daff2-136">Depois que os tipos de arquivo tiverem sido registrados, o exemplo poderá ser executado como um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="daff2-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="daff2-137">Selecione opções no menu do aplicativo de exemplo, incluindo a seleção de documentos. txt ou. doc por meio da caixa de diálogo **abrir** para ver como eles afetam a lista de atalhos do aplicativo na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="daff2-137">Select options from the menu in the sample application, including the selection of .txt or .doc documents through the **Open** dialog to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="daff2-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="daff2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daff2-139">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="daff2-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



