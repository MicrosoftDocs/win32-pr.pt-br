---
description: Fornece informações (x, y) para os pontos inicial e final da linha de base de um parágrafo no documento do diário. O espaço de coordenadas usado para esses valores é HIMETRIC.
ms.assetid: ff6a97ad-0e48-4128-8f94-24802b6ddc05
title: Elemento de linha de base
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b64986707eaa1b382d2f88851367b9147c59c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164257"
---
# <a name="baseline-element"></a><span data-ttu-id="0cca5-104">Elemento de linha de base</span><span class="sxs-lookup"><span data-stu-id="0cca5-104">Baseline Element</span></span>

<span data-ttu-id="0cca5-105">Fornece informações (x, y) para os pontos inicial e final da linha de base de um parágrafo no documento do diário.</span><span class="sxs-lookup"><span data-stu-id="0cca5-105">Provides (x, y) information for the starting and ending points of the baseline of a paragraph in the Journal document.</span></span> <span data-ttu-id="0cca5-106">O espaço de coordenadas usado para esses valores é **HIMETRIC**.</span><span class="sxs-lookup"><span data-stu-id="0cca5-106">The coordinate space used for these values is **HIMETRIC**.</span></span>

## <a name="definition"></a><span data-ttu-id="0cca5-107">Definição</span><span class="sxs-lookup"><span data-stu-id="0cca5-107">Definition</span></span>

``` syntax
<xs:element name="Baseline" type="BaseLineType" />
```

## <a name="parent-elements"></a><span data-ttu-id="0cca5-108">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="0cca5-108">Parent Elements</span></span>

[<span data-ttu-id="0cca5-109">**ParagraphLineMetrics**</span><span class="sxs-lookup"><span data-stu-id="0cca5-109">**ParagraphLineMetrics**</span></span>](paragraphlinemetrics-element.md)

## <a name="child-elements"></a><span data-ttu-id="0cca5-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0cca5-110">Child Elements</span></span>

<span data-ttu-id="0cca5-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0cca5-111">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="0cca5-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cca5-112">Attributes</span></span>



| <span data-ttu-id="0cca5-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="0cca5-113">Attribute</span></span>  | <span data-ttu-id="0cca5-114">Type</span><span class="sxs-lookup"><span data-stu-id="0cca5-114">Type</span></span>                      | <span data-ttu-id="0cca5-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0cca5-115">Required</span></span> | <span data-ttu-id="0cca5-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cca5-116">Description</span></span>                                                      | <span data-ttu-id="0cca5-117">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="0cca5-117">Possible Values</span></span>           |
|------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="0cca5-118">**StartX**</span><span class="sxs-lookup"><span data-stu-id="0cca5-118">**StartX**</span></span> | <span data-ttu-id="0cca5-119">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0cca5-119">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0cca5-120">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0cca5-120">Required</span></span> | <span data-ttu-id="0cca5-121">O valor X do ponto que marca o início da linha de base.</span><span class="sxs-lookup"><span data-stu-id="0cca5-121">The X value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="0cca5-122">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="0cca5-122">Any non-negative integer.</span></span> |
| <span data-ttu-id="0cca5-123">**Inicialização**</span><span class="sxs-lookup"><span data-stu-id="0cca5-123">**StartY**</span></span> | <span data-ttu-id="0cca5-124">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0cca5-124">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0cca5-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0cca5-125">Required</span></span> | <span data-ttu-id="0cca5-126">O valor Y do ponto que marca o início da linha de base.</span><span class="sxs-lookup"><span data-stu-id="0cca5-126">The Y value for the point marking the beginning of the baseline.</span></span> | <span data-ttu-id="0cca5-127">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="0cca5-127">Any non-negative integer.</span></span> |
| <span data-ttu-id="0cca5-128">**EndX**</span><span class="sxs-lookup"><span data-stu-id="0cca5-128">**EndX**</span></span>   | <span data-ttu-id="0cca5-129">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="0cca5-129">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="0cca5-130">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="0cca5-130">Required</span></span> | <span data-ttu-id="0cca5-131">O valor X do ponto que marca o final da linha de base.</span><span class="sxs-lookup"><span data-stu-id="0cca5-131">The X value for the point marking the end of the baseline.</span></span>       | <span data-ttu-id="0cca5-132">Qualquer inteiro não negativo.</span><span class="sxs-lookup"><span data-stu-id="0cca5-132">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="0cca5-133">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="0cca5-133">Element Information</span></span>



|              |                                                               |
|--------------|---------------------------------------------------------------|
| <span data-ttu-id="0cca5-134">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="0cca5-134">Element type</span></span> | <span data-ttu-id="0cca5-135">ComplexType de [**baselinetype**](baselinetype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="0cca5-135">[**BaselineType**](baselinetype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="0cca5-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cca5-136">Namespace</span></span>    | <span data-ttu-id="0cca5-137">urn: esquemas-Microsoft-com: Tablet: RichInk</span><span class="sxs-lookup"><span data-stu-id="0cca5-137">urn:schemas-microsoft-com:tabletpc:richink</span></span>                    |
| <span data-ttu-id="0cca5-138">Nome do esquema</span><span class="sxs-lookup"><span data-stu-id="0cca5-138">Schema name</span></span>  | <span data-ttu-id="0cca5-139">Leitor de diário</span><span class="sxs-lookup"><span data-stu-id="0cca5-139">Journal Reader</span></span>                                                |



 

 

 



