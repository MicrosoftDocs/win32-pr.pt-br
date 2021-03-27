---
description: Demonstra como estender o menu de atalho do tipo "arrastar e soltar" (às vezes chamado de menu de contexto).
title: Exemplo NonDefaultDropMenuVerb
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297235"
---
# <a name="nondefaultdropmenuverb-sample"></a><span data-ttu-id="13ad8-103">Exemplo NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="13ad8-103">NonDefaultDropMenuVerb Sample</span></span>

<span data-ttu-id="13ad8-104">Demonstra como estender o menu de atalho do tipo "arrastar e soltar" (às vezes chamado de menu de contexto).</span><span class="sxs-lookup"><span data-stu-id="13ad8-104">Demonstrates how to extend the drag-and-drop shortcut menu (sometimes referred to as a context menu).</span></span>

<span data-ttu-id="13ad8-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="13ad8-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="13ad8-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ad8-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="13ad8-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13ad8-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="13ad8-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13ad8-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="13ad8-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13ad8-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="13ad8-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13ad8-110">Requirements</span></span>



| <span data-ttu-id="13ad8-111">Produto</span><span class="sxs-lookup"><span data-stu-id="13ad8-111">Product</span></span>                                | <span data-ttu-id="13ad8-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="13ad8-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="13ad8-113">Windows</span><span class="sxs-lookup"><span data-stu-id="13ad8-113">Windows</span></span>                                | <span data-ttu-id="13ad8-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13ad8-114">Windows Vista</span></span>           |
| <span data-ttu-id="13ad8-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="13ad8-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="13ad8-116">7.0</span><span class="sxs-lookup"><span data-stu-id="13ad8-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="13ad8-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13ad8-117">Downloading the Sample</span></span>

| <span data-ttu-id="13ad8-118">Localização</span><span class="sxs-lookup"><span data-stu-id="13ad8-118">Location</span></span>      | <span data-ttu-id="13ad8-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="13ad8-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ad8-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="13ad8-120">GitHub</span></span>  | [<span data-ttu-id="13ad8-121">Exemplo de NonDefaultDropMenuVerb</span><span class="sxs-lookup"><span data-stu-id="13ad8-121">NonDefaultDropMenuVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="13ad8-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13ad8-122">Building the Sample</span></span>

<span data-ttu-id="13ad8-123">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="13ad8-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="13ad8-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="13ad8-124">Open the command prompt window and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="13ad8-125">Digite `msbuild NonDefaultDropMenuVerb.sln`.</span><span class="sxs-lookup"><span data-stu-id="13ad8-125">Enter `msbuild NonDefaultDropMenuVerb.sln`.</span></span>

<span data-ttu-id="13ad8-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="13ad8-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="13ad8-127">Abra o Windows Explorer e navegue até o diretório do projeto **NonDefaultDropMenuVerb** .</span><span class="sxs-lookup"><span data-stu-id="13ad8-127">Open Windows Explorer and navigate to the **NonDefaultDropMenuVerb** project directory.</span></span>
2.  <span data-ttu-id="13ad8-128">Clique duas vezes no ícone do arquivo NonDefaultDropMenuVerb. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="13ad8-128">Double-click the icon for the NonDefaultDropMenuVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="13ad8-129">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="13ad8-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="13ad8-130">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="13ad8-130">Running the Sample</span></span>

1.  <span data-ttu-id="13ad8-131">Navegue até o diretório que contém o novo arquivo DLL, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="13ad8-131">Navigate to the directory that contains the new DLL file, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="13ad8-132">Copie NonDefaultDropMenuVerb.dll para o diretório do sistema (por exemplo, C: \\ Windows \\ System32).</span><span class="sxs-lookup"><span data-stu-id="13ad8-132">Copy NonDefaultDropMenuVerb.dll to the System directory (for example, C:\\Windows\\System32).</span></span>
3.  <span data-ttu-id="13ad8-133">Em um prompt de comando, digite `regedit NonDefaultDropMenuVerb.reg` .</span><span class="sxs-lookup"><span data-stu-id="13ad8-133">At a command prompt, enter `regedit NonDefaultDropMenuVerb.reg`.</span></span>
4.  <span data-ttu-id="13ad8-134">Use o botão direito do mouse para arrastar um arquivo de uma pasta para outra.</span><span class="sxs-lookup"><span data-stu-id="13ad8-134">Use the right mouse button to drag a file from one folder to another.</span></span> <span data-ttu-id="13ad8-135">Você verá itens de menu adicionais para a operação de soltar.</span><span class="sxs-lookup"><span data-stu-id="13ad8-135">You will see additional menu items for the drop operation.</span></span>

 

 



