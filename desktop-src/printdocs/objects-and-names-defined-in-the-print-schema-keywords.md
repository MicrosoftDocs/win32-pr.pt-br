---
description: A Estrutura de Esquema de Impressão define um namespace que inclui os elementos e atributos XML definidos nas Palavras-chave de esquema de impressão.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos e nomes definidos nas palavras-chave de esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aabdac90de6743388ca1f4d44e1ad52c020dbd
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408549"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="bf96a-103">Objetos e nomes definidos nas palavras-chave de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="bf96a-103">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="bf96a-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="bf96a-104">This topic is not current.</span></span> <span data-ttu-id="bf96a-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bf96a-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bf96a-106">A Estrutura de Esquema de Impressão define um namespace que inclui os elementos e atributos XML definidos nas Palavras-chave de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="bf96a-106">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="bf96a-107">Isso inclui elementos como Feature, Option e ScoredProperty; nomes de atributo, como nome e propagação; e valores para atributos XML, como restritos.</span><span class="sxs-lookup"><span data-stu-id="bf96a-107">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="bf96a-108">Em outras palavras, cada uso de um nome definido nas Palavras-chave de Esquema de Impressão deve ser explicitamente qualificado com esse namespace ou deve ser implicitamente associado a esse namespace pelo uso de um atributo xmlns padrão.</span><span class="sxs-lookup"><span data-stu-id="bf96a-108">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="bf96a-109">O documento Palavras-chave de esquema de impressão define as instâncias de elemento público que podem aparecer em qualquer contexto ou local específico.</span><span class="sxs-lookup"><span data-stu-id="bf96a-109">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="bf96a-110">As instâncias de elemento devem aparecer somente dentro do contexto ou local designado na Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="bf96a-110">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="bf96a-111">Por exemplo, a instância <psf:Option name= "psk:Letter"> que é definida nas Palavras-chave de esquema de impressão deve aparecer dentro da instância do <psf:Feature name = "psk:PageMediaSize"> (também definida nas Palavras-chave de esquema de impressão).</span><span class="sxs-lookup"><span data-stu-id="bf96a-111">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="bf96a-112">Você não tem a liberdade de usar uma determinada instância option fora do contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="bf96a-112">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="bf96a-113">Instâncias de elemento definidas de forma privada podem aparecer em qualquer lugar, desde que o tipo de elemento apareça em um contexto permitido pela Estrutura de Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="bf96a-113">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf96a-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf96a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf96a-115">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="bf96a-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



