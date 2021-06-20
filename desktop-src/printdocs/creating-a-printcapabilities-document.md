---
description: Depois que um PrintTicket é validado, ele pode ser usado para criar um instantâneo de PrintCapabilities.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Criando um documento PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409509"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="8ab16-103">Criando um documento PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="8ab16-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="8ab16-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="8ab16-104">This topic is not current.</span></span> <span data-ttu-id="8ab16-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="8ab16-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="8ab16-106">Depois que um PrintTicket é validado, ele pode ser usado para criar um instantâneo de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8ab16-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="8ab16-107">O provedor deve ter uma representação interna para qualquer Propriedade cujo Valor depende da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ab16-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="8ab16-108">Por exemplo, se SpotDiameter for uma Propriedade que depende dos recursos Resolution e MediaType, uma representação interna do SpotDiameter relacionada aos vários valores de Resolution e MediaType poderá aparecer como na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="8ab16-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="8ab16-109">Resolução</span><span class="sxs-lookup"><span data-stu-id="8ab16-109">Resolution</span></span>      | <span data-ttu-id="8ab16-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="8ab16-110">MediaType</span></span>         | <span data-ttu-id="8ab16-111">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="8ab16-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="8ab16-112">300</span><span class="sxs-lookup"><span data-stu-id="8ab16-112">300</span></span><br/>  | <span data-ttu-id="8ab16-113">Bond</span><span class="sxs-lookup"><span data-stu-id="8ab16-113">Bond</span></span><br/>   | <span data-ttu-id="8ab16-114">520</span><span class="sxs-lookup"><span data-stu-id="8ab16-114">520</span></span><br/> |
| <span data-ttu-id="8ab16-115">300</span><span class="sxs-lookup"><span data-stu-id="8ab16-115">300</span></span><br/>  | <span data-ttu-id="8ab16-116">Brilhante</span><span class="sxs-lookup"><span data-stu-id="8ab16-116">Glossy</span></span><br/> | <span data-ttu-id="8ab16-117">350</span><span class="sxs-lookup"><span data-stu-id="8ab16-117">350</span></span><br/> |
| <span data-ttu-id="8ab16-118">600</span><span class="sxs-lookup"><span data-stu-id="8ab16-118">600</span></span><br/>  | <span data-ttu-id="8ab16-119">Bond</span><span class="sxs-lookup"><span data-stu-id="8ab16-119">Bond</span></span><br/>   | <span data-ttu-id="8ab16-120">330</span><span class="sxs-lookup"><span data-stu-id="8ab16-120">330</span></span><br/> |
| <span data-ttu-id="8ab16-121">600</span><span class="sxs-lookup"><span data-stu-id="8ab16-121">600</span></span><br/>  | <span data-ttu-id="8ab16-122">Brilhante</span><span class="sxs-lookup"><span data-stu-id="8ab16-122">Glossy</span></span><br/> | <span data-ttu-id="8ab16-123">180</span><span class="sxs-lookup"><span data-stu-id="8ab16-123">180</span></span><br/> |
| <span data-ttu-id="8ab16-124">1200</span><span class="sxs-lookup"><span data-stu-id="8ab16-124">1200</span></span><br/> | <span data-ttu-id="8ab16-125">Bond</span><span class="sxs-lookup"><span data-stu-id="8ab16-125">Bond</span></span><br/>   | <span data-ttu-id="8ab16-126">250</span><span class="sxs-lookup"><span data-stu-id="8ab16-126">250</span></span><br/> |
| <span data-ttu-id="8ab16-127">1200</span><span class="sxs-lookup"><span data-stu-id="8ab16-127">1200</span></span><br/> | <span data-ttu-id="8ab16-128">Brilhante</span><span class="sxs-lookup"><span data-stu-id="8ab16-128">Glossy</span></span><br/> | <span data-ttu-id="8ab16-129">100</span><span class="sxs-lookup"><span data-stu-id="8ab16-129">100</span></span><br/> |



 

<span data-ttu-id="8ab16-130">Para este exemplo, o provedor PrintCapabilities deve usar o PrintTicket fornecido para selecionar a entrada adequada na tabela interna e relatar isso como o Valor para a propriedade SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="8ab16-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="8ab16-131">Esse processo é repetido para cada Propriedade com valores múltiplos (para cada Propriedade cujo Valor depende da configuração).</span><span class="sxs-lookup"><span data-stu-id="8ab16-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="8ab16-132">A [seção Esquema de PrintCapabilities e](printcapabilities-schema-and-document-construction.md) Construção de Documentos descreve as outras etapas envolvidas na criação de um instantâneo do PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8ab16-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="8ab16-133">Para criar um instantâneo do documento PrintCapabilities padrão, forneça um PrintTicket padrão (em vez de um PrintTicket arbitrário) para o método que cria documentos PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="8ab16-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ab16-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ab16-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ab16-135">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="8ab16-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




