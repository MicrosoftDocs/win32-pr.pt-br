---
description: Demonstra como escutar notificações de alteração do Shell em uma pasta ou item no namespace do Windows Explorer.
title: Exemplo de observador de notificação de alteração
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170696"
---
# <a name="change-notify-watcher-sample"></a><span data-ttu-id="38a1f-103">Exemplo de observador de notificação de alteração</span><span class="sxs-lookup"><span data-stu-id="38a1f-103">Change Notify Watcher Sample</span></span>

<span data-ttu-id="38a1f-104">Demonstra como escutar notificações de alteração do Shell em uma pasta ou item no namespace do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="38a1f-104">Demonstrates how to listen to Shell change notifications on a folder or item in the Windows Explorer namespace.</span></span>

<span data-ttu-id="38a1f-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="38a1f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="38a1f-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38a1f-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="38a1f-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38a1f-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="38a1f-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38a1f-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="38a1f-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38a1f-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="38a1f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38a1f-110">Requirements</span></span>



| <span data-ttu-id="38a1f-111">Produto</span><span class="sxs-lookup"><span data-stu-id="38a1f-111">Product</span></span>                                | <span data-ttu-id="38a1f-112">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="38a1f-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="38a1f-113">Windows</span><span class="sxs-lookup"><span data-stu-id="38a1f-113">Windows</span></span>                                | <span data-ttu-id="38a1f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38a1f-114">Windows Vista</span></span>           |
| <span data-ttu-id="38a1f-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="38a1f-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="38a1f-116">7.0</span><span class="sxs-lookup"><span data-stu-id="38a1f-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="38a1f-117">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38a1f-117">Downloading the Sample</span></span>

| <span data-ttu-id="38a1f-118">Localização</span><span class="sxs-lookup"><span data-stu-id="38a1f-118">Location</span></span>      | <span data-ttu-id="38a1f-119">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="38a1f-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38a1f-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="38a1f-120">GitHub</span></span>  | [<span data-ttu-id="38a1f-121">Exemplo de ChangeNotifyWatcher</span><span class="sxs-lookup"><span data-stu-id="38a1f-121">ChangeNotifyWatcher sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a><span data-ttu-id="38a1f-122">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38a1f-122">Building the Sample</span></span>

<span data-ttu-id="38a1f-123">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="38a1f-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="38a1f-124">Abra a janela do prompt de comando e navegue até o diretório do projeto **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="38a1f-124">Open the command prompt window and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="38a1f-125">Digite `msbuild ChangeNotifyWatcher.sln`.</span><span class="sxs-lookup"><span data-stu-id="38a1f-125">Enter `msbuild ChangeNotifyWatcher.sln`.</span></span>

<span data-ttu-id="38a1f-126">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="38a1f-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="38a1f-127">Abra o Windows Explorer e navegue até o diretório do projeto **ChangeNotifyWatcher** .</span><span class="sxs-lookup"><span data-stu-id="38a1f-127">Open Windows Explorer and navigate to the **ChangeNotifyWatcher** project directory.</span></span>
2.  <span data-ttu-id="38a1f-128">Clique duas vezes no ícone do arquivo ChangeNotifyWatcher. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38a1f-128">Double-click the icon for the ChangeNotifyWatcher.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="38a1f-129">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="38a1f-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="38a1f-130">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="38a1f-130">Running the Sample</span></span>

1.  <span data-ttu-id="38a1f-131">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="38a1f-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="38a1f-132">No prompt de comando, digite `ChangeNotifyWatcher.exe`.</span><span class="sxs-lookup"><span data-stu-id="38a1f-132">At the command prompt, enter `ChangeNotifyWatcher.exe`.</span></span> <span data-ttu-id="38a1f-133">Como alternativa, no Windows Explorer, clique duas vezes no ícone para ChangeNotifyWatcher.exe.</span><span class="sxs-lookup"><span data-stu-id="38a1f-133">Alternatively, from Windows Explorer double-click the icon for ChangeNotifyWatcher.exe.</span></span>
3.  <span data-ttu-id="38a1f-134">Para demonstrar o efeito, AppUserModelIDs (IDs de modelo de usuário do aplicativo) Selecione uma pasta para assistir clicando em **"escolher..."** ou usando arrastar e soltar em uma pasta de uma janela do Windows Explorer na exibição de lista do exemplo.</span><span class="sxs-lookup"><span data-stu-id="38a1f-134">To demonstrate the effect, Application User Model IDs (AppUserModelIDs) select a folder to watch by either clicking **"Pick..."** or by using drag-and-drop on a folder from a Windows Explorer window into the sample's list view.</span></span>

 

 



