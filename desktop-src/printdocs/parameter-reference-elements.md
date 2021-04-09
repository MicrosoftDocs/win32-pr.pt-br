---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 78df6acf-eb4e-46c1-bf1d-c0a99cf49bff
title: Elementos ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c0e145e99b1ee705d63449cf693c6fc87f6463
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104011972"
---
# <a name="parameterref-elements"></a><span data-ttu-id="76168-104">Elementos ParameterRef</span><span class="sxs-lookup"><span data-stu-id="76168-104">ParameterRef Elements</span></span>

<span data-ttu-id="76168-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="76168-105">This topic is not current.</span></span> <span data-ttu-id="76168-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="76168-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="76168-107">Os elementos ParameterRef se aplicam especificamente a elementos Option, permitindo que a capacidade desse elemento Option se refira a um determinado elemento ParameterDef.</span><span class="sxs-lookup"><span data-stu-id="76168-107">ParameterRef elements specifically apply to Option elements, allowing the ability for that Option element to refer to a particular ParameterDef element.</span></span> <span data-ttu-id="76168-108">Para esses elementos de opção, um elemento ScoredProperty que caracteriza a opção não é embutido no código no documento PrintCapabilities como um valor, mas em vez disso é variável.</span><span class="sxs-lookup"><span data-stu-id="76168-108">For these Option elements, a ScoredProperty element that characterizes the Option is not hard-coded in the PrintCapabilities document as a Value, but instead is variable.</span></span> <span data-ttu-id="76168-109">Para habilitar essa variabilidade, esses elementos ScoredProperty contêm um elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="76168-109">To enable this variability, these ScoredProperty elements contain a ParameterRef element.</span></span> <span data-ttu-id="76168-110">Um elemento ScoredProperty não pode conter um elemento Value e um elemento ParameterRef.</span><span class="sxs-lookup"><span data-stu-id="76168-110">A ScoredProperty element may not contain both a Value element and a ParameterRef element.</span></span> <span data-ttu-id="76168-111">Elementos de opção contendo um ou mais elementos ParameterRef são chamados de elementos de opção com parâmetros.</span><span class="sxs-lookup"><span data-stu-id="76168-111">Option elements containing one or more ParameterRef elements are called parameterized Option elements.</span></span>

<span data-ttu-id="76168-112">A estrutura de esquema de impressão permite que um elemento de opção contenha qualquer número de elementos ScoredProperty que se referem a elementos de parâmetro, juntamente com qualquer número de elementos ScoredProperty que contêm elementos de valor.</span><span class="sxs-lookup"><span data-stu-id="76168-112">The Print Schema Framework allows an Option element to contain any number of ScoredProperty elements that refer to Parameter elements, together with any number of ScoredProperty elements that contain Value elements.</span></span> <span data-ttu-id="76168-113">A estrutura também permite que qualquer número de elementos de recurso contenha elementos de opção com parâmetros e qualquer número de elementos de opção com parâmetros seja permitido para cada elemento de recurso.</span><span class="sxs-lookup"><span data-stu-id="76168-113">The Framework also allows any number of Feature elements to contain parameterized Option elements, and any number of parameterized Option elements are permitted for each Feature element.</span></span> <span data-ttu-id="76168-114">Além disso, a mesma construção de parâmetro pode ser referenciada por vários elementos de opção diferentes, elementos de opção que podem pertencer a elementos de recurso iguais ou diferentes.</span><span class="sxs-lookup"><span data-stu-id="76168-114">Also, the same parameter construct can be referred to by several different Option elements, Option elements that can belong to the same or different Feature elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76168-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="76168-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76168-116">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="76168-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



