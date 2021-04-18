---
description: Cada recurso de Windows Installer usa um ou mais componentes do Windows Installer, e os recursos podem compartilhar componentes.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Especificando relações de Feature-Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770177"
---
# <a name="specifying-feature-component-relationships"></a><span data-ttu-id="639d5-103">Especificando relações de Feature-Component</span><span class="sxs-lookup"><span data-stu-id="639d5-103">Specifying Feature-Component Relationships</span></span>

<span data-ttu-id="639d5-104">Cada [recurso de Windows Installer](windows-installer-features.md) usa um ou mais [componentes do Windows Installer](windows-installer-components.md), e os recursos podem compartilhar componentes.</span><span class="sxs-lookup"><span data-stu-id="639d5-104">Each [Windows Installer Feature](windows-installer-features.md) uses one or more [Windows Installer Components](windows-installer-components.md), and features may share components.</span></span> <span data-ttu-id="639d5-105">A [tabela FeatureComponents](featurecomponents-table.md) define a relação entre recursos e componentes.</span><span class="sxs-lookup"><span data-stu-id="639d5-105">The [FeatureComponents table](featurecomponents-table.md) defines the relationship between features and components.</span></span> <span data-ttu-id="639d5-106">Consulte o [grupo de tabelas principais](core-tables-group.md) e os [componentes e recursos](components-and-features.md) no Windows Installer visão geral.</span><span class="sxs-lookup"><span data-stu-id="639d5-106">See the [Core Tables Group](core-tables-group.md) and [Components and Features](components-and-features.md) in the Windows Installer overview.</span></span> <span data-ttu-id="639d5-107">Nesta seção, você adiciona informações à tabela FeatureComponents do exemplo do bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="639d5-107">In this section you add information to the FeatureComponents table of the Notepad sample.</span></span>

<span data-ttu-id="639d5-108">Use o editor de banco de dados para abrir MNP2000.msi e insira os dados a seguir na tabela FeatureComponents vazia.</span><span class="sxs-lookup"><span data-stu-id="639d5-108">Use your database editor to open MNP2000.msi and enter the following data into the empty FeatureComponents table.</span></span>

[<span data-ttu-id="639d5-109">Tabela FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="639d5-109">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="639d5-110">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="639d5-110">Feature\_</span></span> | <span data-ttu-id="639d5-111">Componente\_</span><span class="sxs-lookup"><span data-stu-id="639d5-111">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="639d5-112">Beisebol</span><span class="sxs-lookup"><span data-stu-id="639d5-112">Baseball</span></span>  | <span data-ttu-id="639d5-113">Beisebol</span><span class="sxs-lookup"><span data-stu-id="639d5-113">Baseball</span></span>    |
| <span data-ttu-id="639d5-114">Concerto</span><span class="sxs-lookup"><span data-stu-id="639d5-114">Concert</span></span>   | <span data-ttu-id="639d5-115">Concerto</span><span class="sxs-lookup"><span data-stu-id="639d5-115">Concert</span></span>     |
| <span data-ttu-id="639d5-116">Dance</span><span class="sxs-lookup"><span data-stu-id="639d5-116">Dance</span></span>     | <span data-ttu-id="639d5-117">Dance</span><span class="sxs-lookup"><span data-stu-id="639d5-117">Dance</span></span>       |
| <span data-ttu-id="639d5-118">Comemorar</span><span class="sxs-lookup"><span data-stu-id="639d5-118">Football</span></span>  | <span data-ttu-id="639d5-119">Comemorar</span><span class="sxs-lookup"><span data-stu-id="639d5-119">Football</span></span>    |
| <span data-ttu-id="639d5-120">Ajuda</span><span class="sxs-lookup"><span data-stu-id="639d5-120">Help</span></span>      | <span data-ttu-id="639d5-121">Ajuda</span><span class="sxs-lookup"><span data-stu-id="639d5-121">Help</span></span>        |
| <span data-ttu-id="639d5-122">Janeiro</span><span class="sxs-lookup"><span data-stu-id="639d5-122">January</span></span>   | <span data-ttu-id="639d5-123">Janeiro</span><span class="sxs-lookup"><span data-stu-id="639d5-123">January</span></span>     |
| <span data-ttu-id="639d5-124">NewYears</span><span class="sxs-lookup"><span data-stu-id="639d5-124">NewYears</span></span>  | <span data-ttu-id="639d5-125">NewYears</span><span class="sxs-lookup"><span data-stu-id="639d5-125">NewYears</span></span>    |
| <span data-ttu-id="639d5-126">Bloco de notas</span><span class="sxs-lookup"><span data-stu-id="639d5-126">Notepad</span></span>   | <span data-ttu-id="639d5-127">Bloco de notas</span><span class="sxs-lookup"><span data-stu-id="639d5-127">Notepad</span></span>     |
| <span data-ttu-id="639d5-128">Leiame</span><span class="sxs-lookup"><span data-stu-id="639d5-128">Readme</span></span>    | <span data-ttu-id="639d5-129">Bloco de notas</span><span class="sxs-lookup"><span data-stu-id="639d5-129">Notepad</span></span>     |



 

[<span data-ttu-id="639d5-130">Continuar</span><span class="sxs-lookup"><span data-stu-id="639d5-130">Continue</span></span>](adding-registry-information.md)

 

 



