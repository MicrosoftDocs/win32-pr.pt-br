---
description: Demonstra como criar uma lista de atalhos personalizada para um aplicativo, incluindo adicionar uma categoria e tarefas personalizadas.
title: Exemplo de lista de atalhos personalizada
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 60DEDB01-8F8F-4c25-8FCC-8EAC461A99B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c20592e508a24985e0f8283993482c7bd61af232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170694"
---
# <a name="custom-jump-list-sample"></a><span data-ttu-id="52b1d-103">Exemplo de lista de atalhos personalizada</span><span class="sxs-lookup"><span data-stu-id="52b1d-103">Custom Jump List Sample</span></span>

<span data-ttu-id="52b1d-104">Demonstra como criar uma lista de atalhos personalizada para um aplicativo, incluindo adicionar uma categoria e tarefas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="52b1d-104">Demonstrates how to create a custom Jump List for an application, including adding a custom category and tasks.</span></span>

<span data-ttu-id="52b1d-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="52b1d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="52b1d-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52b1d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="52b1d-107">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="52b1d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="52b1d-108">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="52b1d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="52b1d-109">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="52b1d-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="52b1d-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52b1d-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="52b1d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52b1d-111">Requirements</span></span>



| <span data-ttu-id="52b1d-112">Produto</span><span class="sxs-lookup"><span data-stu-id="52b1d-112">Product</span></span>                                | <span data-ttu-id="52b1d-113">Versão mínima do produto</span><span class="sxs-lookup"><span data-stu-id="52b1d-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="52b1d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="52b1d-114">Windows</span></span>                                | <span data-ttu-id="52b1d-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="52b1d-115">Windows 7</span></span>               |
| <span data-ttu-id="52b1d-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="52b1d-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="52b1d-117">7.0</span><span class="sxs-lookup"><span data-stu-id="52b1d-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="52b1d-118">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="52b1d-118">Downloading the Sample</span></span>

| <span data-ttu-id="52b1d-119">Localização</span><span class="sxs-lookup"><span data-stu-id="52b1d-119">Location</span></span>      | <span data-ttu-id="52b1d-120">URL do caminho</span><span class="sxs-lookup"><span data-stu-id="52b1d-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52b1d-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="52b1d-121">GitHub</span></span>  | [<span data-ttu-id="52b1d-122">Exemplo de CustomJumpList</span><span class="sxs-lookup"><span data-stu-id="52b1d-122">CustomJumpList sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CustomJumpList) |

## <a name="building-the-sample"></a><span data-ttu-id="52b1d-123">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="52b1d-123">Building the Sample</span></span>

<span data-ttu-id="52b1d-124">Para criar o exemplo do prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="52b1d-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="52b1d-125">Abra a janela do prompt de comando e navegue até o diretório do projeto **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="52b1d-125">Open the command prompt window and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="52b1d-126">Digite `msbuild CustomJumpListSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="52b1d-126">Enter `msbuild CustomJumpListSample.sln`.</span></span>

<span data-ttu-id="52b1d-127">Para criar o exemplo usando Microsoft Visual Studio (preferencial):</span><span class="sxs-lookup"><span data-stu-id="52b1d-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="52b1d-128">Abra o Windows Explorer e navegue até o diretório do projeto **CustomJumpList** .</span><span class="sxs-lookup"><span data-stu-id="52b1d-128">Open Windows Explorer and navigate to the **CustomJumpList** project directory.</span></span>
2.  <span data-ttu-id="52b1d-129">Clique duas vezes no ícone do arquivo CustomJumpListSample. sln para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="52b1d-129">Double-click the icon for the CustomJumpListSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="52b1d-130">No menu **Compilar** , selecione **Compilar solução**.</span><span class="sxs-lookup"><span data-stu-id="52b1d-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="52b1d-131">Executando o exemplo</span><span class="sxs-lookup"><span data-stu-id="52b1d-131">Running the Sample</span></span>

1.  <span data-ttu-id="52b1d-132">Navegue até o diretório que contém o novo executável, usando o prompt de comando ou o Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="52b1d-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="52b1d-133">Na linha de comando, digite `CustomJumpListSample.exe` .</span><span class="sxs-lookup"><span data-stu-id="52b1d-133">At the command line, enter `CustomJumpListSample.exe`.</span></span> <span data-ttu-id="52b1d-134">Como alternativa, no Windows Explorer, clique duas vezes no ícone para CustomJumpListSample.exe.</span><span class="sxs-lookup"><span data-stu-id="52b1d-134">Alternatively, from Windows Explorer double-click the icon for CustomJumpListSample.exe.</span></span>
3.  <span data-ttu-id="52b1d-135">Este exemplo deve ser executado como administrador na primeira vez em que for executado para que ele possa instalar os registros de tipo de arquivo necessários.</span><span class="sxs-lookup"><span data-stu-id="52b1d-135">This sample must be run as an administrator the first time it is run so that it can install the necessary file type registrations.</span></span> <span data-ttu-id="52b1d-136">Depois que os tipos de arquivo tiverem sido registrados, o exemplo poderá ser executado como um usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="52b1d-136">After the file types have been registered, the sample can run as a standard user.</span></span>
4.  <span data-ttu-id="52b1d-137">Selecione opções no menu do aplicativo de exemplo para ver como elas afetam a lista de atalhos do aplicativo na barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="52b1d-137">Select options from the menu in the sample application to see how they affect the application's Jump List in the taskbar.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52b1d-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="52b1d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52b1d-139">IDs de modelo de usuário de aplicativo (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="52b1d-139">Application User Model IDs (AppUserModelIDs)</span></span>](appids.md)
</dt> </dl>

 

 



