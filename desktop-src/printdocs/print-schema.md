---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referência de esquema de impressão herdado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 881e986501950108c06e1e92303d13dc06265aae
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105755910"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="192be-104">Referência de esquema de impressão herdado</span><span class="sxs-lookup"><span data-stu-id="192be-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="192be-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="192be-105">This topic is not current.</span></span> <span data-ttu-id="192be-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="192be-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="192be-107">O esquema de impressão e as tecnologias relacionadas estão disponíveis no Microsoft .NET Framework 3,0, no Microsoft Windows Vista e em versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="192be-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="192be-108">O esquema de impressão fornece um formato baseado em XML para expressar e organizar um grande conjunto de propriedades que descrevem um formato de trabalho ou PrintCapabilities de uma maneira hierarquicamente estruturada.</span><span class="sxs-lookup"><span data-stu-id="192be-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="192be-109">O esquema de impressão é um termo abrangente que inclui dois componentes, as palavras-chave do esquema de impressão e a estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="192be-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="192be-110">O documento de palavras-chave do esquema de impressão é um esquema público que define um conjunto de instâncias de elemento que pode ser usado para descrever os atributos do dispositivo e a formatação do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="192be-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="192be-111">A estrutura de esquema de impressão é um esquema público que define uma coleção hierarquicamente estruturada de tipos de elemento XML e especifica como os tipos de elemento podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="192be-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="192be-112">As palavras-chave do esquema de impressão e a estrutura de esquema de impressão formam a base para duas tecnologias de impressão relacionadas ao esquema, o esquema de PrintCapabilities e o esquema PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="192be-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="192be-113">É importante ter em mente que uma das metas do esquema de impressão é dar suporte a extensões de esquema por provedores.</span><span class="sxs-lookup"><span data-stu-id="192be-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="192be-114">Ou seja, os provedores não estão restritos a usar somente as instâncias de propriedade, recurso, opção ou ParameterInit definidas nas palavras-chave do esquema de impressão nas tecnologias criadas na estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="192be-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="192be-115">As instâncias de elemento específicas do provedor podem estar livremente intercaladas dentro das instâncias de elemento definidas nas palavras-chave do esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="192be-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="192be-116">O único requisito é que as instâncias de propriedade específicas do provedor (ou seja, privadas) devem pertencer a um namespace que esteja claramente associado ao provedor.</span><span class="sxs-lookup"><span data-stu-id="192be-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="192be-117">Plano de fundo do esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="192be-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="192be-118">Schema-Related tecnologias de impressão</span><span class="sxs-lookup"><span data-stu-id="192be-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="192be-119">Termos usados no esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="192be-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="192be-120">Sintaxe do esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="192be-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="192be-121">Resumo dos tipos de elementos</span><span class="sxs-lookup"><span data-stu-id="192be-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="192be-122">Estrutura de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="192be-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="192be-123">Imprimir palavras-chave públicas do esquema</span><span class="sxs-lookup"><span data-stu-id="192be-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="192be-124">Construção de esquema e documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="192be-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="192be-125">Construção de esquema e documento do PrintTicket</span><span class="sxs-lookup"><span data-stu-id="192be-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="192be-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="192be-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="192be-127">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="192be-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



