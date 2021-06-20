---
description: Os provedores PrintCapabilities devem dar suporte a um conjunto mínimo de recursos, que são implícitos pela Interface do Provedor PrintTicket/PrintCapabilities.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades dos provedores PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc04137eacdd2395205b96233db3c53964bc02
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404909"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="ffba7-103">Responsabilidades dos provedores PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="ffba7-103">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="ffba7-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="ffba7-104">This topic is not current.</span></span> <span data-ttu-id="ffba7-105">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ffba7-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ffba7-106">Os provedores PrintCapabilities devem dar suporte a um conjunto mínimo de recursos, que são implícitos pela Interface do Provedor PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="ffba7-106">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="ffba7-107">Essas funcionalidades estão listadas aqui.</span><span class="sxs-lookup"><span data-stu-id="ffba7-107">These capabilities are listed here.</span></span>

-   <span data-ttu-id="ffba7-108">Eles devem seguir a direção da propagação?? Atributo XML, quando ele aparece no contexto apropriado e contém um valor válido para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="ffba7-108">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="ffba7-109">Eles devem gerar um documento PrintCapabilities que esteja em conformidade com o esquema PrintCapabilities e atenda aos requisitos especificados no Esquema de Impressão.</span><span class="sxs-lookup"><span data-stu-id="ffba7-109">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="ffba7-110">Eles devem ser capazes de reconhecer um PrintTicket válido.</span><span class="sxs-lookup"><span data-stu-id="ffba7-110">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="ffba7-111">Eles devem ser capazes de interpretar um PrintTicket e entender a configuração específica que ele representa.</span><span class="sxs-lookup"><span data-stu-id="ffba7-111">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="ffba7-112">Eles devem ser capazes de determinar se essa configuração contém conflitos de restrição.</span><span class="sxs-lookup"><span data-stu-id="ffba7-112">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="ffba7-113">Eles devem ser capazes de modificar um PrintTicket inválido ou conflitante fazendo a alteração menos significativa necessária para torná-la válida e sem conflitos.</span><span class="sxs-lookup"><span data-stu-id="ffba7-113">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="ffba7-114">Eles devem ser capazes de gerar um documento PrintCapabilities para uma configuração de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="ffba7-114">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="ffba7-115">Eles devem ser capazes de gerar uma configuração padrão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="ffba7-115">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="ffba7-116">Eles devem ser capazes de gerar um documento PrintCapabilities que corresponda à configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="ffba7-116">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="ffba7-117">Eles devem implementar um processo de pontuação de opção definido pelo driver de dispositivo capaz de determinar a proximidade da combinação entre duas instâncias option que pertencem ao mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="ffba7-117">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="ffba7-118">Esse algoritmo é usado no processo de validação printTicket.</span><span class="sxs-lookup"><span data-stu-id="ffba7-118">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="ffba7-119">Além dos requisitos acima, o documento PrintCapabilities deve conter valores válidos e corretos para cada atributo XML (por exemplo, restrito) de cada Opção.</span><span class="sxs-lookup"><span data-stu-id="ffba7-119">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffba7-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffba7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffba7-121">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="ffba7-121">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



