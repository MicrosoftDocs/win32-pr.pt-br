---
title: Amostra de rebar
ms.assetid: f26c0819-523d-42a5-be2f-3cd75748b4a6
description: 'Saiba mais sobre: exemplo de rebar'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72b58a66c22b0ef8cc60d97c0965a8ae29a20fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920176"
---
# <a name="rebar-sample"></a><span data-ttu-id="202b0-103">Amostra de rebar</span><span class="sxs-lookup"><span data-stu-id="202b0-103">Rebar Sample</span></span>

<span data-ttu-id="202b0-104">Este tópico descreve o exemplo de código de exemplo do rebar.</span><span class="sxs-lookup"><span data-stu-id="202b0-104">This topic describes the Rebar Sample code sample.</span></span> <span data-ttu-id="202b0-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="202b0-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="202b0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="202b0-106">Description</span></span>](#description)
-   [<span data-ttu-id="202b0-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="202b0-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="202b0-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="202b0-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="202b0-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="202b0-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="202b0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="202b0-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="202b0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="202b0-111">Description</span></span>

<span data-ttu-id="202b0-112">O exemplo de rebar mostra como implementar um controle comum de rebar simples em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="202b0-112">The Rebar Sample shows how to implement a simple rebar common control in an application.</span></span> <span data-ttu-id="202b0-113">Este exemplo cria um controle rebar que tem duas faixas.</span><span class="sxs-lookup"><span data-stu-id="202b0-113">This example creates a rebar control that has two bands.</span></span> <span data-ttu-id="202b0-114">Uma delas contém uma caixa de combinação e a outra contém um botão de ação.</span><span class="sxs-lookup"><span data-stu-id="202b0-114">One contains a combo box and the other contains a push button.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="202b0-115">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="202b0-115">Minimum Requirements</span></span>



| <span data-ttu-id="202b0-116">Produto</span><span class="sxs-lookup"><span data-stu-id="202b0-116">Product</span></span>          | <span data-ttu-id="202b0-117">Versão</span><span class="sxs-lookup"><span data-stu-id="202b0-117">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="202b0-118">DLL</span><span class="sxs-lookup"><span data-stu-id="202b0-118">DLL</span></span>              | <span data-ttu-id="202b0-119">comctl32.dll versão 4,71</span><span class="sxs-lookup"><span data-stu-id="202b0-119">comctl32.dll version 4.71</span></span>             |
| <span data-ttu-id="202b0-120">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="202b0-120">Operating System</span></span> | <span data-ttu-id="202b0-121">Windows 95 com Internet Explorer 4,0</span><span class="sxs-lookup"><span data-stu-id="202b0-121">Windows 95 with Internet Explorer 4.0</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="202b0-122">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="202b0-122">Downloading the Sample</span></span>

<span data-ttu-id="202b0-123">O exemplo de rebar é instalado como parte do [SDK (Software Development Kit) do Windows](https://msdn.microsoft.com/windows/bb980924.aspx) e está disponível no local a seguir.</span><span class="sxs-lookup"><span data-stu-id="202b0-123">The Rebar Sample is installed as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and is available in the following location.</span></span>



| <span data-ttu-id="202b0-124">Local</span><span class="sxs-lookup"><span data-stu-id="202b0-124">Location</span></span>    | <span data-ttu-id="202b0-125">Caminho/URL</span><span class="sxs-lookup"><span data-stu-id="202b0-125">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="202b0-126">SDK do Windows</span><span class="sxs-lookup"><span data-stu-id="202b0-126">Windows SDK</span></span> | <span data-ttu-id="202b0-127">% Arquivos de programas% \\ Microsoft SDKs \\ Windows número de \\ \[ versão \] \\ amostras \\ WinUI \\ controles \\ \\ rebar comuns</span><span class="sxs-lookup"><span data-stu-id="202b0-127">%Program Files%\\Microsoft SDKs\\Windows\\\[version number\]\\Samples\\winui\\controls\\common\\rebar</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="202b0-128">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="202b0-128">Building the Sample</span></span>

<span data-ttu-id="202b0-129">Para criar o exemplo usando o prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="202b0-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="202b0-130">Abra a janela do prompt de comando e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="202b0-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="202b0-131">Digite `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="202b0-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="202b0-132">Para criar o exemplo usando o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="202b0-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="202b0-133">Abra o Windows Explorer e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="202b0-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="202b0-134">Clique duas vezes no ícone do arquivo. vcproj para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="202b0-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="202b0-135">No menu **Compilar** , selecione **Compilar solução** para compilar a solução.</span><span class="sxs-lookup"><span data-stu-id="202b0-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="202b0-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="202b0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="202b0-137">Controles Rebar</span><span class="sxs-lookup"><span data-stu-id="202b0-137">Rebar Controls</span></span>](rebar-controls.md)
</dt> </dl>

 

 




