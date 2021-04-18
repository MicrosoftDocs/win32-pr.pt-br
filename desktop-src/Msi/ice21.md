---
description: ICE21 valida que cada componente na tabela de componentes pertence a um recurso. Ele usa a tabela FeatureComponents para verificar esse mapeamento.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753448"
---
# <a name="ice21"></a><span data-ttu-id="d9915-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="d9915-104">ICE21</span></span>

<span data-ttu-id="d9915-105">ICE21 valida que cada componente na tabela de [componentes](component-table.md) pertence a um recurso.</span><span class="sxs-lookup"><span data-stu-id="d9915-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="d9915-106">Ele usa a [tabela FeatureComponents](featurecomponents-table.md) para verificar esse mapeamento.</span><span class="sxs-lookup"><span data-stu-id="d9915-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="d9915-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="d9915-107">Result</span></span>

<span data-ttu-id="d9915-108">ICE21 posta uma mensagem de erro se o pacote de instalação contiver um componente que não pertence a um recurso.</span><span class="sxs-lookup"><span data-stu-id="d9915-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="d9915-109">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d9915-109">Example</span></span>

<span data-ttu-id="d9915-110">Para o exemplo a seguir, ICE21 posta uma mensagem de erro informando que o componente comp1 não é mapeado para nenhum recurso.</span><span class="sxs-lookup"><span data-stu-id="d9915-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="d9915-111">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d9915-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="d9915-112">Componente</span><span class="sxs-lookup"><span data-stu-id="d9915-112">Component</span></span> |
|-----------|
| <span data-ttu-id="d9915-113">Comp1</span><span class="sxs-lookup"><span data-stu-id="d9915-113">Comp1</span></span>     |
| <span data-ttu-id="d9915-114">Comp2</span><span class="sxs-lookup"><span data-stu-id="d9915-114">Comp2</span></span>     |



 

<span data-ttu-id="d9915-115">[Tabela FeatureComponents](featurecomponents-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d9915-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="d9915-116">Recurso</span><span class="sxs-lookup"><span data-stu-id="d9915-116">Feature</span></span>  | <span data-ttu-id="d9915-117">Componente</span><span class="sxs-lookup"><span data-stu-id="d9915-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="d9915-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="d9915-118">Feature1</span></span> | <span data-ttu-id="d9915-119">Comp2</span><span class="sxs-lookup"><span data-stu-id="d9915-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="d9915-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d9915-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9915-121">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="d9915-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



