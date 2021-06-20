---
description: Saiba mais sobre a sintaxe do esquema de impressão, que é expressa na sintaxe XML e é composta por um pequeno número de tipos de elementos.
ms.assetid: d67518e3-c379-4a50-aeda-31afaa7f05dd
title: Sintaxe do esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef52dbdbdfacc2d3cc947b46558319577a75b1b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405289"
---
# <a name="syntax-of-the-print-schema"></a><span data-ttu-id="7b7a3-103">Sintaxe do esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7b7a3-103">Syntax of the Print Schema</span></span>

<span data-ttu-id="7b7a3-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-104">This topic is not current.</span></span> <span data-ttu-id="7b7a3-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7b7a3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b7a3-106">O esquema de impressão é expresso na sintaxe XML.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-106">The Print Schema is expressed in XML syntax.</span></span> <span data-ttu-id="7b7a3-107">Portanto, os leitores devem estar familiarizados com a sintaxe XML e os termos como elemento, marca do elemento, conteúdo do elemento, atributo e namespace.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-107">Readers are therefore expected to be familiar with XML syntax and terms such as element, element tag, element content, attribute, and namespace.</span></span> <span data-ttu-id="7b7a3-108">A estrutura do esquema de impressão é composta por um pequeno número de tipos de elementos; cada tipo de elemento atende a uma finalidade específica nas tecnologias criadas no esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-108">The Print Schema Framework is composed of a small number of element types; each element type serves a specific purpose in the technologies built on the Print Schema.</span></span>

<span data-ttu-id="7b7a3-109">Os tipos de elementos são diferenciados por sua marca de elemento XML.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-109">Element types are distinguished by their XML element tag.</span></span> <span data-ttu-id="7b7a3-110">A estrutura de esquema de impressão define a estrutura geral e a organização das tecnologias dependentes, denotando para cada tipo de elemento quais tipos de elementos são permitidos como elementos filho.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-110">The Print Schema Framework defines the overall structure and organization of the dependent technologies, by denoting for each element type which element types are allowed as child elements.</span></span>

<span data-ttu-id="7b7a3-111">Muitos tipos de elementos são diferenciados de outros do mesmo tipo pelo atributo de nome, que desempenha uma função significativa no esquema.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-111">Many element types are differentiated from others of the same type by the name attribute, which plays a significant role in the schema.</span></span> <span data-ttu-id="7b7a3-112">O atributo Name serve para identificar instâncias de cada tipo de elemento.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-112">The name attribute serves to identify instances of each element type.</span></span> <span data-ttu-id="7b7a3-113">As palavras-chave do esquema de impressão definem um conjunto de valores para o atributo Name para muitos dos tipos de elemento.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-113">The Print Schema Keywords defines a set of values for the name attribute for many of the element types.</span></span> <span data-ttu-id="7b7a3-114">Na maioria dos casos, os provedores podem atribuir seus próprios valores ao atributo Name.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-114">In most cases, providers can assign their own values to the name attribute.</span></span> <span data-ttu-id="7b7a3-115">Eles precisam apenas garantir que os valores sejam QName de XML qualificados com um namespace exclusivo para o provedor.</span><span class="sxs-lookup"><span data-stu-id="7b7a3-115">They need only ensure the values are XML QNames qualified with a namespace that is unique to the provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b7a3-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b7a3-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b7a3-117">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="7b7a3-117">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



