---
description: A tabela ComPlus contém as informações necessárias para instalar aplicativos COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Tabela ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751862"
---
# <a name="complus-table"></a><span data-ttu-id="c3a67-103">Tabela ComPlus</span><span class="sxs-lookup"><span data-stu-id="c3a67-103">Complus Table</span></span>

<span data-ttu-id="c3a67-104">A tabela ComPlus contém as informações necessárias para instalar aplicativos COM+.</span><span class="sxs-lookup"><span data-stu-id="c3a67-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="c3a67-105">A tabela ComPlus tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3a67-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="c3a67-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="c3a67-106">Column</span></span>      | <span data-ttu-id="c3a67-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3a67-107">Type</span></span>                         | <span data-ttu-id="c3a67-108">Chave</span><span class="sxs-lookup"><span data-stu-id="c3a67-108">Key</span></span> | <span data-ttu-id="c3a67-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="c3a67-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="c3a67-110">Componente\_</span><span class="sxs-lookup"><span data-stu-id="c3a67-110">Component\_</span></span> | [<span data-ttu-id="c3a67-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="c3a67-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="c3a67-112">S</span><span class="sxs-lookup"><span data-stu-id="c3a67-112">Y</span></span>   | <span data-ttu-id="c3a67-113">N</span><span class="sxs-lookup"><span data-stu-id="c3a67-113">N</span></span>        |
| <span data-ttu-id="c3a67-114">ExpType</span><span class="sxs-lookup"><span data-stu-id="c3a67-114">ExpType</span></span>     | [<span data-ttu-id="c3a67-115">Inteiro</span><span class="sxs-lookup"><span data-stu-id="c3a67-115">Integer</span></span>](integer.md)       | <span data-ttu-id="c3a67-116">N</span><span class="sxs-lookup"><span data-stu-id="c3a67-116">N</span></span>   | <span data-ttu-id="c3a67-117">S</span><span class="sxs-lookup"><span data-stu-id="c3a67-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c3a67-118">Colunas</span><span class="sxs-lookup"><span data-stu-id="c3a67-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c3a67-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="c3a67-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="c3a67-120">Uma chave externa na primeira coluna da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3a67-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="c3a67-121">Esse é o componente que contém o aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="c3a67-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="c3a67-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span><span class="sxs-lookup"><span data-stu-id="c3a67-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="c3a67-123">Sinalizadores de exportação usados durante a geração do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="c3a67-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="c3a67-124">Para obter mais informações, consulte a documentação COM+ no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c3a67-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a67-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a67-125">Remarks</span></span>

<span data-ttu-id="c3a67-126">Consulte a ação [RegisterComPlus](registercomplus-action.md) e a [ação UnregisterComPlus](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="c3a67-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="c3a67-127">Consulte [instalando um aplicativo com+ com o Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="c3a67-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="c3a67-128">Validação</span><span class="sxs-lookup"><span data-stu-id="c3a67-128">Validation</span></span>

<dl>

[<span data-ttu-id="c3a67-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="c3a67-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="c3a67-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="c3a67-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="c3a67-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="c3a67-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="c3a67-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="c3a67-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



