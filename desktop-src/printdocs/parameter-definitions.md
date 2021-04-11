---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 82ba4658-f0e1-47a7-bb0c-1b527fabde4a
title: Definições de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5a71bfc5a5111a826b5d221ff1436ecf921dd2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172555"
---
# <a name="parameter-definitions"></a><span data-ttu-id="aa8dd-104">Definições de parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa8dd-104">Parameter Definitions</span></span>

<span data-ttu-id="aa8dd-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-105">This topic is not current.</span></span> <span data-ttu-id="aa8dd-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="aa8dd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="aa8dd-107">Esta seção descreve as definições de parâmetros públicos que podem aparecer em um documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-107">This section outlines the public parameter definitions which may appear in either a PrintCapabilities document.</span></span>

<span data-ttu-id="aa8dd-108">Os parâmetros são usados para descrever um intervalo aceitável de valores, em vez de uma enumeração discreta de valores.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-108">Parameters are used to describe an acceptable range of values, rather than a discrete enumeration of values.</span></span>

## <a name="parameterdef"></a><span data-ttu-id="aa8dd-109">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="aa8dd-109">ParameterDef</span></span>

<span data-ttu-id="aa8dd-110">Para obter um resumo do tipo de elemento ParameterDef, consulte a seção [ParameterDef](parameterdef.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8dd-110">For a summary of the ParameterDef element type, please refer to [ParameterDef](parameterdef.md) section.</span></span>

<span data-ttu-id="aa8dd-111">Para obter mais informações sobre a interação entre elementos ParameterDef e elementos ParameterInit, consulte a seção de [elementos ParameterDef e ParameterInit](./parameterdef-and-parameterinit-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8dd-111">For more information on the interaction between ParameterDef elements and ParameterInit elements, refer to [ParameterDef and ParameterInit Elements](./parameterdef-and-parameterinit-elements.md) section.</span></span>

<span data-ttu-id="aa8dd-112">Os elementos ParameterDef definidos nas palavras-chave do esquema de impressão devem ser totalmente definidos em um documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-112">ParameterDef elements that are defined in the Print Schema Keywords must be fully defined in a PrintCapabilities document.</span></span>

## <a name="parameterref"></a><span data-ttu-id="aa8dd-113">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="aa8dd-113">ParameterRef</span></span>

<span data-ttu-id="aa8dd-114">Para obter um resumo do tipo de elemento ParameterRef, consulte a seção [ParameterRef](parameterref.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8dd-114">For a summary of the ParameterRef element type, please refer to [ParameterRef](parameterref.md) section.</span></span>

<span data-ttu-id="aa8dd-115">Uma palavra-chave de elemento configurável pelo usuário pode conter uma referência a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="aa8dd-115">A user configurable element keyword may contain a reference to a Parameter.</span></span> <span data-ttu-id="aa8dd-116">Os elementos ParameterRef são especificados como um filho de um elemento ScoredProperty para obter mais informações, consulte a seção [elementos de referência de parâmetro](parameter-reference-elements.md) .</span><span class="sxs-lookup"><span data-stu-id="aa8dd-116">ParameterRef elements are specified as a child of a ScoredProperty element For more information, please refer to [Parameter Reference Elements](parameter-reference-elements.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa8dd-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa8dd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa8dd-118">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="aa8dd-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 
