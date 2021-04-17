---
title: Exemplo de VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'Saiba mais sobre: exemplo de VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753562"
---
# <a name="vlistvw-sample"></a><span data-ttu-id="94db0-103">Exemplo de VListVW</span><span class="sxs-lookup"><span data-stu-id="94db0-103">VListVW Sample</span></span>

<span data-ttu-id="94db0-104">Este tópico descreve o exemplo de código de exemplo VListVW.</span><span class="sxs-lookup"><span data-stu-id="94db0-104">This topic describes the VListVW Sample code sample.</span></span> <span data-ttu-id="94db0-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="94db0-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="94db0-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="94db0-106">Description</span></span>](#description)
-   [<span data-ttu-id="94db0-107">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="94db0-107">Minimum Requirements</span></span>](#minimum-requirements)
-   [<span data-ttu-id="94db0-108">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="94db0-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="94db0-109">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="94db0-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="94db0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94db0-110">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="94db0-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="94db0-111">Description</span></span>

<span data-ttu-id="94db0-112">O exemplo de VListVW mostra como implementar um controle de exibição de lista virtual simples em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="94db0-112">The VListVW Sample shows how to implement a simple virtual list-view control in an application.</span></span> <span data-ttu-id="94db0-113">Um controle de exibição de lista virtual é um controle de exibição de lista padrão com o estilo **LVS \_ OWNERDATA** .</span><span class="sxs-lookup"><span data-stu-id="94db0-113">A virtual list-view control is a standard list-view control with the **LVS\_OWNERDATA** style.</span></span> <span data-ttu-id="94db0-114">Este exemplo cria um controle de exibição de lista que "virtualmente" contém 100.000 itens.</span><span class="sxs-lookup"><span data-stu-id="94db0-114">This example creates a list-view control that "virtually" holds 100,000 items.</span></span> <span data-ttu-id="94db0-115">Os itens nunca são adicionados de fato.</span><span class="sxs-lookup"><span data-stu-id="94db0-115">The items are never actually added.</span></span> <span data-ttu-id="94db0-116">Em vez disso, o controle de exibição de lista virtual é "informado" quantos itens ele contém com a mensagem do [**LVM \_ setitemcount**](lvm-setitemcount.md) .</span><span class="sxs-lookup"><span data-stu-id="94db0-116">Instead, the virtual list-view control is "told" how many items it contains with the [**LVM\_SETITEMCOUNT**](lvm-setitemcount.md) message.</span></span> <span data-ttu-id="94db0-117">Quando um item precisa ser desenhado, o controle List-View consulta a janela pai para exibir informações com a notificação [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="94db0-117">When an item needs to be drawn, the list-view control queries the parent window for display information with the [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification.</span></span>

## <a name="minimum-requirements"></a><span data-ttu-id="94db0-118">Requisitos mínimos</span><span class="sxs-lookup"><span data-stu-id="94db0-118">Minimum Requirements</span></span>



| <span data-ttu-id="94db0-119">Produto</span><span class="sxs-lookup"><span data-stu-id="94db0-119">Product</span></span>          | <span data-ttu-id="94db0-120">Versão</span><span class="sxs-lookup"><span data-stu-id="94db0-120">Version</span></span>                               |
|------------------|---------------------------------------|
| <span data-ttu-id="94db0-121">DLL</span><span class="sxs-lookup"><span data-stu-id="94db0-121">DLL</span></span>              | <span data-ttu-id="94db0-122">comctl32.dll versão 4,70</span><span class="sxs-lookup"><span data-stu-id="94db0-122">comctl32.dll version 4.70</span></span>             |
| <span data-ttu-id="94db0-123">Sistema operacional</span><span class="sxs-lookup"><span data-stu-id="94db0-123">Operating System</span></span> | <span data-ttu-id="94db0-124">Windows 95, Microsoft Windows NT 3,51</span><span class="sxs-lookup"><span data-stu-id="94db0-124">Windows 95, Microsoft Windows NT 3.51</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="94db0-125">Baixando o exemplo</span><span class="sxs-lookup"><span data-stu-id="94db0-125">Downloading the Sample</span></span>

<span data-ttu-id="94db0-126">O exemplo VListVW está disponível no GitHub no repositório de [exemplos clássico do Windows](https://github.com/microsoft/Windows-classic-samples).</span><span class="sxs-lookup"><span data-stu-id="94db0-126">The VListVW Sample is available on on github in the [Windows Classic Samples repository](https://github.com/microsoft/Windows-classic-samples).</span></span> <span data-ttu-id="94db0-127">Os exemplos de itens de controle de exibição de lista podem ser encontrados [aqui](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span><span class="sxs-lookup"><span data-stu-id="94db0-127">The list view control items examples can be found at [here](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="94db0-128">Compilando o exemplo</span><span class="sxs-lookup"><span data-stu-id="94db0-128">Building the Sample</span></span>

<span data-ttu-id="94db0-129">Para criar o exemplo usando o prompt de comando:</span><span class="sxs-lookup"><span data-stu-id="94db0-129">To build the sample using the command prompt:</span></span>

1.  <span data-ttu-id="94db0-130">Abra a janela do prompt de comando e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="94db0-130">Open the Command Prompt window and navigate to the project directory.</span></span>
2.  <span data-ttu-id="94db0-131">Digite `msbuild [project file]`.</span><span class="sxs-lookup"><span data-stu-id="94db0-131">Enter `msbuild [project file]`.</span></span>

<span data-ttu-id="94db0-132">Para criar o exemplo usando o Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="94db0-132">To build the sample using Visual Studio:</span></span>

1.  <span data-ttu-id="94db0-133">Abra o Windows Explorer e navegue até o diretório do projeto.</span><span class="sxs-lookup"><span data-stu-id="94db0-133">Open Windows Explorer and navigate to the project directory.</span></span>
2.  <span data-ttu-id="94db0-134">Clique duas vezes no ícone do arquivo. vcproj para abrir o projeto no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="94db0-134">Double-click the icon for the .vcproj file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="94db0-135">No menu **Compilar** , selecione **Compilar solução** para compilar a solução.</span><span class="sxs-lookup"><span data-stu-id="94db0-135">From the **Build** menu, select **Build Solution** to build the solution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94db0-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94db0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94db0-137">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="94db0-137">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> </dl>

 

 




