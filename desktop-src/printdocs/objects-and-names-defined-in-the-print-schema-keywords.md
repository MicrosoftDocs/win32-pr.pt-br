---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 5a07ec21-dc7c-46d5-b1c2-de06f53fe6bf
title: Objetos e nomes definidos nas palavras-chave do esquema de impressão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2347c73dd647f90a88821658cdcf9e2ed846e83
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172541"
---
# <a name="objects-and-names-defined-in-the-print-schema-keywords"></a><span data-ttu-id="71423-104">Objetos e nomes definidos nas palavras-chave do esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="71423-104">Objects and Names Defined in the Print Schema Keywords</span></span>

<span data-ttu-id="71423-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="71423-105">This topic is not current.</span></span> <span data-ttu-id="71423-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="71423-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="71423-107">A estrutura de esquema de impressão define um namespace que inclui os elementos e atributos XML definidos nas palavras-chave do esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="71423-107">The Print Schema Framework defines a namespace that includes the elements and XML attributes defined in the Print Schema Keywords.</span></span> <span data-ttu-id="71423-108">Isso inclui elementos como recurso, opção e ScoredProperty; nomes de atributos como Name e propagar; e valores para atributos XML, como restritos.</span><span class="sxs-lookup"><span data-stu-id="71423-108">This includes elements such as Feature, Option, and ScoredProperty; attribute names such as name and propagate; and values for XML attributes such as constrained.</span></span> <span data-ttu-id="71423-109">Em outras palavras, cada uso de um nome definido nas palavras-chave do esquema de impressão deve ser explicitamente qualificado com esse namespace ou deve ser implicitamente associado a esse namespace pelo uso de um atributo xmlns padrão.</span><span class="sxs-lookup"><span data-stu-id="71423-109">In other words, every use of a name that is defined in the Print Schema Keywords should be explicitly qualified with this namespace, or should be implicitly associated with this namespace by the use of a default xmlns attribute.</span></span> <span data-ttu-id="71423-110">O documento de palavras-chave do esquema de impressão define as instâncias do elemento público que podem aparecer em qualquer contexto ou local específico.</span><span class="sxs-lookup"><span data-stu-id="71423-110">The Print Schema Keywords document defines the public element instances that may appear in any given context or location.</span></span> <span data-ttu-id="71423-111">As instâncias de elemento devem aparecer somente dentro do contexto ou local designado na estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="71423-111">Element instances must appear only within the context or location designated in the Print Schema Framework.</span></span> <span data-ttu-id="71423-112">Por exemplo, a <PSF: Option Name = "PSK: letter" > instância definida nas palavras-chave do esquema de impressão deve aparecer dentro da instância do <PSF: Feature Name = "PSK: PageMediaSize >" (também definida nas palavras-chave do esquema de impressão).</span><span class="sxs-lookup"><span data-stu-id="71423-112">For example, the <psf:Option name= "psk:Letter"> instance that is defined in the Print Schema Keywords must appear within the <psf:Feature name = "psk:PageMediaSize"> instance (also defined in the Print Schema Keywords).</span></span> <span data-ttu-id="71423-113">Você não tem a liberdade de usar uma determinada instância de opção fora de seu contexto especificado.</span><span class="sxs-lookup"><span data-stu-id="71423-113">You do not have the freedom to use a given Option instance outside of its specified context.</span></span>

<span data-ttu-id="71423-114">As instâncias de elemento definidas de modo privado podem aparecer em qualquer lugar, desde que o tipo de elemento apareça em um contexto permitido pela estrutura de esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="71423-114">Privately-defined element instances may appear anywhere as long as the element type appears in a context allowed by the Print Schema Framework.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71423-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71423-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71423-116">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="71423-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



