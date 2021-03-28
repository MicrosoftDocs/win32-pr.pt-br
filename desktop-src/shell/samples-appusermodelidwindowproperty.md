---
description: Demonstra como controlar o comportamento de agrupamento da barra de tarefas de janelas de um aplicativo por meio da propriedade System.AppUserModel.ID.
title: Exemplo da propriedade janela de ID do modelo do usuário do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D4B22B3F-C849-4b5f-BDA0-FB42D7E0E4C9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 42544992248143c95ae905db39fe854b27751862
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968098"
---
# <a name="application-user-model-id-appid-window-property-sample"></a><span data-ttu-id="c5fdc-103">Exemplo da propriedade da janela de ID do modelo de usuário do aplicativo (AppID)</span><span class="sxs-lookup"><span data-stu-id="c5fdc-103">Application User Model ID (AppID) Window Property Sample</span></span>

<span data-ttu-id="c5fdc-104">Demonstra como controlar o comportamento de agrupamento da barra de tarefas de janelas de um aplicativo por meio da propriedade [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="c5fdc-104">Demonstrates how to control the taskbar grouping behavior of an application's windows through the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property.</span></span>

<span data-ttu-id="c5fdc-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c5fdc-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5fdc-106">Description</span></span>](#description)
-   [<span data-ttu-id="c5fdc-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5fdc-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="c5fdc-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c5fdc-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="c5fdc-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c5fdc-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="c5fdc-110">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c5fdc-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="c5fdc-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5fdc-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="c5fdc-112">Description</span><span class="sxs-lookup"><span data-stu-id="c5fdc-112">Description</span></span>

<span data-ttu-id="c5fdc-113">Este exemplo mostra como definir a propriedade [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) por meio do uso da implementação de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) da janela, que é obtida por meio de [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span><span class="sxs-lookup"><span data-stu-id="c5fdc-113">This sample shows how to set the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property through the use of the window's [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) implementation, which is obtained through [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5fdc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5fdc-114">Requirements</span></span>



| <span data-ttu-id="c5fdc-115">Produto</span><span class="sxs-lookup"><span data-stu-id="c5fdc-115">Product</span></span>                                | <span data-ttu-id="c5fdc-116">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="c5fdc-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="c5fdc-117">Windows</span><span class="sxs-lookup"><span data-stu-id="c5fdc-117">Windows</span></span>                                | <span data-ttu-id="c5fdc-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5fdc-118">Windows 7</span></span>               |
| <span data-ttu-id="c5fdc-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c5fdc-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="c5fdc-120">7.0</span><span class="sxs-lookup"><span data-stu-id="c5fdc-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="c5fdc-121">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c5fdc-121">Downloading the Sample</span></span>

| <span data-ttu-id="c5fdc-122">Localização</span><span class="sxs-lookup"><span data-stu-id="c5fdc-122">Location</span></span>      | <span data-ttu-id="c5fdc-123">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="c5fdc-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5fdc-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="c5fdc-124">GitHub</span></span>  | [<span data-ttu-id="c5fdc-125">Exemplo de AppUserModelIDWindowProperty</span><span class="sxs-lookup"><span data-stu-id="c5fdc-125">AppUserModelIDWindowProperty sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/AppUserModelIDWindowProperty) |


## <a name="building-the-sample"></a><span data-ttu-id="c5fdc-126">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c5fdc-126">Building the Sample</span></span>

<span data-ttu-id="c5fdc-127">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="c5fdc-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="c5fdc-128">Abra a janela do prompt de comando e navegue até o diretório do projeto **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="c5fdc-128">Open the command prompt window and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="c5fdc-129">Digite `msbuild AppUserModelIDWindowProperty.sln`.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-129">Enter `msbuild AppUserModelIDWindowProperty.sln`.</span></span>

<span data-ttu-id="c5fdc-130">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="c5fdc-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="c5fdc-131">Abra o Windows Explorer e navegue até o diretório do projeto **AppUserModelIDWindowProperty** .</span><span class="sxs-lookup"><span data-stu-id="c5fdc-131">Open Windows Explorer and navigate to the **AppUserModelIDWindowProperty** project directory.</span></span>
2.  <span data-ttu-id="c5fdc-132">Clique duas vezes no ícone do arquivo AppUserModelIDWindowProperty. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-132">Double-click the icon for the AppUserModelIDWindowProperty.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="c5fdc-133">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c5fdc-134">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="c5fdc-134">Running the Sample</span></span>

1.  <span data-ttu-id="c5fdc-135">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="c5fdc-136">Na linha de comando, digite `AppUserModelIDWindowProperty.exe` .</span><span class="sxs-lookup"><span data-stu-id="c5fdc-136">At the command line, enter `AppUserModelIDWindowProperty.exe`.</span></span> <span data-ttu-id="c5fdc-137">Como alternativa, no Windows Explorer, clique duas vezes no ícone para AppUserModelIDWindowProperty.exe.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-137">Alternatively, from Windows Explorer double-click the icon for AppUserModelIDWindowProperty.exe.</span></span>
3.  <span data-ttu-id="c5fdc-138">Para demonstrar o efeito que as IDs de modelo de usuário do aplicativo (AppUserModelIDs) têm no agrupamento da barra de tarefas, inicie pelo menos três instâncias do aplicativo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-138">To demonstrate the effect Application User Model IDs (AppUserModelIDs) have on taskbar grouping, launch at least three instances of the application at the same time.</span></span>
4.  <span data-ttu-id="c5fdc-139">Use o menu para definir um AppUserModelID diferente em cada uma das três janelas.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-139">Use the menu to set a different AppUserModelID on each of the three windows.</span></span> <span data-ttu-id="c5fdc-140">Observe que cada AppUserModelID separado resulta em um botão de barra de tarefas separado e que o Windows pode alterar sua identidade em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-140">Notice that each separate AppUserModelID results in a separate taskbar button and that windows can change their identity at runtime.</span></span>
5.  <span data-ttu-id="c5fdc-141">Defina pelo menos duas janelas para o segundo AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-141">Set at least two windows to the second AppUserModelID.</span></span> <span data-ttu-id="c5fdc-142">Observe que ambos se movem para o mesmo grupo da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-142">Notice that they both move into the same taskbar group.</span></span>
6.  <span data-ttu-id="c5fdc-143">Abra a **barra de tarefas e a janela Propriedades do menu iniciar** clicando com o botão direito do mouse na barra de tarefas e selecionando **Propriedades** no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-143">Open the **Taskbar and Start Menu Properties** window by right-clicking the taskbar and selecting **Properties** in the context menu.</span></span> <span data-ttu-id="c5fdc-144">Altere os **botões da barra de tarefas:** lista suspensa entre **combinar quando a barra de tarefas estiver cheia** e **nunca combinar** valores.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-144">Change the **Taskbar buttons:** drop-down between the **Combine when taskbar is full** and **Never combine** values.</span></span> <span data-ttu-id="c5fdc-145">Observe que cada janela pode obter um botão separado, mas que os botões são agrupados por AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="c5fdc-145">Notice that each window can get a separate button, but that the buttons are grouped by AppUserModelID.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5fdc-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5fdc-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5fdc-147">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="c5fdc-147">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 
