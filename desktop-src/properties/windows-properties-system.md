---
description: Sistema de propriedades do Windows
ms.assetid: c2094bbe-a4ca-4f30-b16e-14dced2912bc
title: Sistema de propriedades do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49e44c988d3a91572be1b42d5fbaf75e664d7f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089874"
---
# <a name="windows-property-system"></a><span data-ttu-id="631e2-103">Sistema de propriedades do Windows</span><span class="sxs-lookup"><span data-stu-id="631e2-103">Windows Property System</span></span>

## <a name="purpose"></a><span data-ttu-id="631e2-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="631e2-104">Purpose</span></span>

<span data-ttu-id="631e2-105">O sistema de propriedades do Windows é um sistema de leitura/gravação extensível de definições de dados que fornece uma maneira uniforme de expressar os metadados sobre itens de Shell.</span><span class="sxs-lookup"><span data-stu-id="631e2-105">The Windows Property System is an extensible read/write system of data definitions that provides a uniform way of expressing metadata about Shell items.</span></span> <span data-ttu-id="631e2-106">O sistema de propriedades do Windows no Windows Vista e posterior permite que você armazene e recupere metadados para itens de Shell.</span><span class="sxs-lookup"><span data-stu-id="631e2-106">The Windows Property system in Windows Vista and later enables you to store and retrieve metadata for Shell items.</span></span> <span data-ttu-id="631e2-107">Um item de Shell é qualquer conteúdo único, como um arquivo, uma pasta, um email ou um contato.</span><span class="sxs-lookup"><span data-stu-id="631e2-107">A Shell item is any single piece of content, such as a file, folder, email, or contact.</span></span> <span data-ttu-id="631e2-108">Uma propriedade é uma parte individual dos metadados associados a um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="631e2-108">A property is an individual piece of metadata associated with a Shell item.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="631e2-109">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="631e2-109">Developer audience</span></span>

<span data-ttu-id="631e2-110">Antes de começar a ler a documentação do SDK do sistema de propriedades do Windows, você deve ter uma compreensão fundamental do seguinte:</span><span class="sxs-lookup"><span data-stu-id="631e2-110">Before you start reading the Windows Property System SDK documentation, you should have a fundamental understanding of the following:</span></span>

-   <span data-ttu-id="631e2-111">COM (Component Object Model)</span><span class="sxs-lookup"><span data-stu-id="631e2-111">Component Object Model (COM)</span></span>
-   <span data-ttu-id="631e2-112">Programação de namespace de Shell</span><span class="sxs-lookup"><span data-stu-id="631e2-112">Shell Namespace programming</span></span>

<span data-ttu-id="631e2-113">Para obter uma introdução ao COM, consulte [conceitos básicos de com](../com/com-fundamentals.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-113">For an introduction to COM, see [COM Fundamentals](../com/com-fundamentals.md).</span></span> <span data-ttu-id="631e2-114">Para obter uma introdução à programação de namespace do Shell, consulte [introdução com o namespace do Shell](../shell/namespace-intro.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-114">For an introduction to Shell Namespace programming, see [Getting Started with the Shell Namespace](../shell/namespace-intro.md).</span></span>

<span data-ttu-id="631e2-115">Para usos do sistema de propriedades do Windows, consulte [visão geral do sistema de propriedades: cenários de desenvolvimento](property-system-overview.md).</span><span class="sxs-lookup"><span data-stu-id="631e2-115">For uses of the Windows Property System, see [Property System Overview: Development Scenarios](property-system-overview.md).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="631e2-116">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="631e2-116">Run-time requirements</span></span>

<span data-ttu-id="631e2-117">O ambiente de tempo de execução com suporte para usar o sistema de propriedades do Windows é o Windows Vista ou posterior e o SDK (Software Development Kit) do Windows.</span><span class="sxs-lookup"><span data-stu-id="631e2-117">The supported run-time environment for using the Windows Property System is Windows Vista or later and the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="631e2-118">O Windows XP e o Microsoft Windows Desktop Search (WDS) 3,0 ou posterior também incluem um subconjunto do sistema de propriedades do Windows.</span><span class="sxs-lookup"><span data-stu-id="631e2-118">Windows XP and Microsoft Windows Desktop Search (WDS) 3.0 or later also include a subset of the Windows Property System.</span></span> <span data-ttu-id="631e2-119">Para obter o download do SDK do Windows Vista ou atualizado, consulte a [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="631e2-119">For the Windows 7 or updated Windows Vista SDK download, see the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="631e2-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="631e2-120">In this section</span></span>

-   [<span data-ttu-id="631e2-121">Visão geral do sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="631e2-121">Property System Overview</span></span>](property-system-overview.md)
-   [<span data-ttu-id="631e2-122">Guia do desenvolvedor do sistema de propriedades do Windows</span><span class="sxs-lookup"><span data-stu-id="631e2-122">Windows Property System Developer's Guide</span></span>](property-system-developer-s-guide.md)
-   [<span data-ttu-id="631e2-123">Referência do sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="631e2-123">Property System Reference</span></span>](property-system-reference.md)
-   [<span data-ttu-id="631e2-124">Exemplos de código do sistema de propriedades</span><span class="sxs-lookup"><span data-stu-id="631e2-124">Property System Code Samples</span></span>](property-system-code-samples.md)

 

 
