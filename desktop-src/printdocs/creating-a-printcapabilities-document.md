---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Criando um documento de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105807857"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="b3685-104">Criando um documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b3685-104">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="b3685-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b3685-105">This topic is not current.</span></span> <span data-ttu-id="b3685-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b3685-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b3685-107">Depois que um PrintTicket é validado, ele pode ser usado para criar um instantâneo dos PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b3685-107">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="b3685-108">O provedor deve ter uma representação interna para qualquer propriedade cujo valor seja dependente da configuração do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b3685-108">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="b3685-109">Por exemplo, se SpotDiameter for uma propriedade que depende dos recursos de resolução e de MediaType, uma representação interna de SpotDiameter, pois ele se relaciona com os vários valores para resolução e MediaType pode aparecer como na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="b3685-109">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="b3685-110">Resolução</span><span class="sxs-lookup"><span data-stu-id="b3685-110">Resolution</span></span>      | <span data-ttu-id="b3685-111">MediaType</span><span class="sxs-lookup"><span data-stu-id="b3685-111">MediaType</span></span>         | <span data-ttu-id="b3685-112">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="b3685-112">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="b3685-113">300</span><span class="sxs-lookup"><span data-stu-id="b3685-113">300</span></span><br/>  | <span data-ttu-id="b3685-114">Vincular</span><span class="sxs-lookup"><span data-stu-id="b3685-114">Bond</span></span><br/>   | <span data-ttu-id="b3685-115">520</span><span class="sxs-lookup"><span data-stu-id="b3685-115">520</span></span><br/> |
| <span data-ttu-id="b3685-116">300</span><span class="sxs-lookup"><span data-stu-id="b3685-116">300</span></span><br/>  | <span data-ttu-id="b3685-117">Acetinado</span><span class="sxs-lookup"><span data-stu-id="b3685-117">Glossy</span></span><br/> | <span data-ttu-id="b3685-118">350</span><span class="sxs-lookup"><span data-stu-id="b3685-118">350</span></span><br/> |
| <span data-ttu-id="b3685-119">600</span><span class="sxs-lookup"><span data-stu-id="b3685-119">600</span></span><br/>  | <span data-ttu-id="b3685-120">Vincular</span><span class="sxs-lookup"><span data-stu-id="b3685-120">Bond</span></span><br/>   | <span data-ttu-id="b3685-121">330</span><span class="sxs-lookup"><span data-stu-id="b3685-121">330</span></span><br/> |
| <span data-ttu-id="b3685-122">600</span><span class="sxs-lookup"><span data-stu-id="b3685-122">600</span></span><br/>  | <span data-ttu-id="b3685-123">Acetinado</span><span class="sxs-lookup"><span data-stu-id="b3685-123">Glossy</span></span><br/> | <span data-ttu-id="b3685-124">180</span><span class="sxs-lookup"><span data-stu-id="b3685-124">180</span></span><br/> |
| <span data-ttu-id="b3685-125">1200</span><span class="sxs-lookup"><span data-stu-id="b3685-125">1200</span></span><br/> | <span data-ttu-id="b3685-126">Vincular</span><span class="sxs-lookup"><span data-stu-id="b3685-126">Bond</span></span><br/>   | <span data-ttu-id="b3685-127">250</span><span class="sxs-lookup"><span data-stu-id="b3685-127">250</span></span><br/> |
| <span data-ttu-id="b3685-128">1200</span><span class="sxs-lookup"><span data-stu-id="b3685-128">1200</span></span><br/> | <span data-ttu-id="b3685-129">Acetinado</span><span class="sxs-lookup"><span data-stu-id="b3685-129">Glossy</span></span><br/> | <span data-ttu-id="b3685-130">100</span><span class="sxs-lookup"><span data-stu-id="b3685-130">100</span></span><br/> |



 

<span data-ttu-id="b3685-131">Para este exemplo, o provedor de PrintCapabilities deve usar o PrintTicket fornecido para selecionar a entrada apropriada da tabela interna e relatar que como o valor para a propriedade SpotDiameter.</span><span class="sxs-lookup"><span data-stu-id="b3685-131">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="b3685-132">Esse processo é repetido para cada propriedade de valores múltiplos (para cada propriedade cujo valor é dependente da configuração).</span><span class="sxs-lookup"><span data-stu-id="b3685-132">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="b3685-133">A seção [esquema de PrintCapabilities e construção de documentos](printcapabilities-schema-and-document-construction.md) descreve as outras etapas envolvidas na criação de um instantâneo dos PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b3685-133">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="b3685-134">Para criar um instantâneo do documento padrão de PrintCapabilities, forneça um PrintTicket padrão (em vez de um PrintTicket arbitrário) para o método que cria documentos de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b3685-134">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3685-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3685-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3685-136">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b3685-136">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




