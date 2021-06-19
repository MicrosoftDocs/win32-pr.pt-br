---
description: Esta visão geral descreve os tópicos Esquema de Impressão e links para Referência de Esquema de Impressão. O esquema de impressão inclui as Palavras-chave de esquema de impressão e a Estrutura.
ms.assetid: d746bdd1-96c2-41f5-ad99-0b51c8ee8731
title: Referência de esquema de impressão herdado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a8f417d20913563cfd4a52ba51d21b516e73f0
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407129"
---
# <a name="legacy-print-schema-reference"></a><span data-ttu-id="a726c-104">Referência de esquema de impressão herdado</span><span class="sxs-lookup"><span data-stu-id="a726c-104">Legacy Print Schema Reference</span></span>

<span data-ttu-id="a726c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="a726c-105">This topic is not current.</span></span> <span data-ttu-id="a726c-106">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a726c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a726c-107">O Esquema de Impressão e as tecnologias relacionadas estão disponíveis no Microsoft .NET Framework 3.0, Microsoft Windows Vista e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a726c-107">The Print Schema and related technologies are available in the Microsoft .NET Framework 3.0, Microsoft Windows Vista, and later releases.</span></span>

<span data-ttu-id="a726c-108">O Esquema de Impressão fornece um formato baseado em XML para expressar e organizar um grande conjunto de propriedades que descrevem um formato de trabalho ou PrintCapabilities de maneira hierárquica.</span><span class="sxs-lookup"><span data-stu-id="a726c-108">The Print Schema provides an XML-based format for expressing and organizing a large set of properties that describe either a job format or PrintCapabilities in a hierarchically structured manner.</span></span>

<span data-ttu-id="a726c-109">O Esquema de Impressão é um termo que inclui dois componentes, As Palavras-chave de esquema de impressão e a Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="a726c-109">The Print Schema is an umbrella term that includes two components, the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="a726c-110">O documento Palavras-chave de esquema de impressão é um esquema público que define um conjunto de instâncias de elemento que podem ser usadas para descrever atributos de dispositivo e formatação de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="a726c-110">The Print Schema Keywords document is a public schema that defines a set of element instances that can be used to describe device attributes and print job formatting.</span></span> <span data-ttu-id="a726c-111">A Estrutura de Esquema de Impressão é um esquema público que define uma coleção hierarquicamente estruturada de tipos de elemento XML e especifica como os tipos de elemento podem ser usados juntos.</span><span class="sxs-lookup"><span data-stu-id="a726c-111">The Print Schema Framework is a public schema that defines a hierarchically structured collection of XML element types, and specifies how the element types can be used together.</span></span>

<span data-ttu-id="a726c-112">As palavras-chave de esquema de impressão e a Estrutura de Esquema de Impressão formam a base para duas tecnologias relacionadas ao esquema de impressão, o esquema PrintCapabilities e o esquema PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="a726c-112">The Print Schema Keywords and the Print Schema Framework form the foundation for two Print Schema-related technologies, the PrintCapabilities Schema, and the PrintTicket Schema.</span></span>

<span data-ttu-id="a726c-113">É importante ter em mente que uma das metas do Esquema de Impressão é dar suporte a extensões de esquema por provedores.</span><span class="sxs-lookup"><span data-stu-id="a726c-113">It is important to keep in mind that one of the goals of the Print Schema is to support schema extensions by providers.</span></span> <span data-ttu-id="a726c-114">Ou seja, os provedores não estão restritos a usar apenas as instâncias Property, Feature, Option ou ParameterInit definidas nas Palavras-chave de esquema de impressão nas tecnologias criadas na Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="a726c-114">That is, providers are not restricted to using only those Property, Feature, Option, or ParameterInit instances defined in the Print Schema Keywords in the technologies built on the Print Schema Framework.</span></span> <span data-ttu-id="a726c-115">Instâncias de elemento específicas do provedor podem ser intercaladas livremente em instâncias de elemento definidas nas Palavras-chave de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="a726c-115">Provider-specific element instances may be freely interspersed within element instances defined in the Print Schema Keywords.</span></span> <span data-ttu-id="a726c-116">O único requisito é que as instâncias de propriedade específicas do provedor (ou seja, privadas) devem pertencer a um namespace claramente associado ao provedor.</span><span class="sxs-lookup"><span data-stu-id="a726c-116">The only requirement is that provider-specific (that is, private) Property instances must belong to a namespace that is clearly associated with the provider.</span></span>

-   [<span data-ttu-id="a726c-117">Tela de fundo do esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a726c-117">Print Schema Background</span></span>](print-schema-background.md)

-   [<span data-ttu-id="a726c-118">Tecnologias de Schema-Related impressão</span><span class="sxs-lookup"><span data-stu-id="a726c-118">Print Schema-Related Technologies</span></span>](print-schema-related-technologies.md)

-   [<span data-ttu-id="a726c-119">Termos usados no esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a726c-119">Terms Used in the Print Schema</span></span>](terms-used-in-the-print-schema.md)

-   [<span data-ttu-id="a726c-120">Sintaxe do esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a726c-120">Syntax of the Print Schema</span></span>](syntax-of-the-print-schema.md)

-   [<span data-ttu-id="a726c-121">Resumo dos tipos de elemento</span><span class="sxs-lookup"><span data-stu-id="a726c-121">Summary of Element Types</span></span>](summary-of-element-types.md)

-   [<span data-ttu-id="a726c-122">Estrutura de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a726c-122">Print Schema Framework</span></span>](print-schema-framework.md)

-   [<span data-ttu-id="a726c-123">Imprimir palavras-chave públicas do esquema</span><span class="sxs-lookup"><span data-stu-id="a726c-123">Print Schema Public Keywords</span></span>](print-schema-public-keywords.md)

-   [<span data-ttu-id="a726c-124">Esquema PrintCapabilities e construção de documentos</span><span class="sxs-lookup"><span data-stu-id="a726c-124">PrintCapabilities Schema and Document Construction</span></span>](printcapabilities-schema-and-document-construction.md)

-   [<span data-ttu-id="a726c-125">Esquema PrintTicket e construção de documento</span><span class="sxs-lookup"><span data-stu-id="a726c-125">PrintTicket Schema and Document Construction</span></span>](printticket-schema-and-document-construction.md)

## <a name="related-topics"></a><span data-ttu-id="a726c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a726c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a726c-127">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="a726c-127">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



