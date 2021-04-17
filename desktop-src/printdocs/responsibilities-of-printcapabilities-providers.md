---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 92e9bce1-d58e-40a4-9721-832d7c3bc2b2
title: Responsabilidades de provedores de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bbf355f7b62f8f9c8b3f3b0c59714cdd6ade5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105763769"
---
# <a name="responsibilities-of-printcapabilities-providers"></a><span data-ttu-id="b1d84-104">Responsabilidades de provedores de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="b1d84-104">Responsibilities of PrintCapabilities Providers</span></span>

<span data-ttu-id="b1d84-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="b1d84-105">This topic is not current.</span></span> <span data-ttu-id="b1d84-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="b1d84-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="b1d84-107">Os provedores de PrintCapabilities devem dar suporte a um conjunto mínimo de recursos, que são implícitos pela interface do provedor PrintTicket/PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="b1d84-107">PrintCapabilities providers must support a minimum set of capabilities, which are implied by the PrintTicket/PrintCapabilities Provider Interface.</span></span> <span data-ttu-id="b1d84-108">Esses recursos estão listados aqui.</span><span class="sxs-lookup"><span data-stu-id="b1d84-108">These capabilities are listed here.</span></span>

-   <span data-ttu-id="b1d84-109">Eles devem seguir a direção da propagação?? O atributo XML, quando aparece no contexto apropriado, e contém um valor válido para esse contexto.</span><span class="sxs-lookup"><span data-stu-id="b1d84-109">They must follow the direction of the propagate??XML attribute, when it appears in the appropriate context and contains a valid value for that context.</span></span>

-   <span data-ttu-id="b1d84-110">Eles devem gerar um documento de PrintCapabilities que esteja de acordo com o esquema de PrintCapabilities e atenda aos requisitos especificados no esquema de impressão.</span><span class="sxs-lookup"><span data-stu-id="b1d84-110">They must generate a PrintCapabilities document that conforms to the PrintCapabilities Schema and satisfies the requirements specified in the Print Schema.</span></span>

-   <span data-ttu-id="b1d84-111">Eles devem ser capazes de reconhecer um PrintTicket válido.</span><span class="sxs-lookup"><span data-stu-id="b1d84-111">They must be able to recognize a valid PrintTicket.</span></span>

-   <span data-ttu-id="b1d84-112">Eles devem ser capazes de interpretar um PrintTicket e compreender a configuração específica que ele representa.</span><span class="sxs-lookup"><span data-stu-id="b1d84-112">They must be able to interpret a PrintTicket and understand the specific configuration it represents.</span></span>

-   <span data-ttu-id="b1d84-113">Eles devem ser capazes de determinar se essa configuração contém conflitos de restrição.</span><span class="sxs-lookup"><span data-stu-id="b1d84-113">They must be able to determine whether that configuration contains constraint conflicts.</span></span>

-   <span data-ttu-id="b1d84-114">Eles devem ser capazes de modificar um PrintTicket inválido ou conflitante, tornando a alteração menos significativa necessária para torná-lo válido e sem conflitos.</span><span class="sxs-lookup"><span data-stu-id="b1d84-114">They must be able to modify an invalid or conflicting PrintTicket by making the least significant change necessary to make it both valid and without conflicts.</span></span>

-   <span data-ttu-id="b1d84-115">Eles devem ser capazes de gerar um documento de PrintCapabilities para uma configuração de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="b1d84-115">They must be able to generate a PrintCapabilities document for a particular device configuration.</span></span>

-   <span data-ttu-id="b1d84-116">Eles devem ser capazes de gerar uma configuração padrão ou PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b1d84-116">They must be able to generate a default configuration or PrintTicket.</span></span>

-   <span data-ttu-id="b1d84-117">Eles devem ser capazes de gerar um documento de PrintCapabilities que corresponda à configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="b1d84-117">They must be able to generate a PrintCapabilities document that corresponds to the default configuration.</span></span>

-   <span data-ttu-id="b1d84-118">Eles devem implementar um processo de Pontuação de opção definido pelo driver de dispositivo capaz de determinar a proximidade de correspondência entre duas instâncias de opção que pertencem ao mesmo recurso.</span><span class="sxs-lookup"><span data-stu-id="b1d84-118">They must implement an Option-scoring process defined by the device driver capable of determining the closeness of match between two Option instances that belong to the same Feature.</span></span> <span data-ttu-id="b1d84-119">Esse algoritmo é usado no processo de validação do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="b1d84-119">This algorithm is used in the PrintTicket validation process.</span></span>

<span data-ttu-id="b1d84-120">Além dos requisitos acima, o documento PrintCapabilities deve conter valores válidos e corretos para cada atributo XML (por exemplo, restrito) de cada opção.</span><span class="sxs-lookup"><span data-stu-id="b1d84-120">In addition to the foregoing requirements, the PrintCapabilities document must contain valid and correct values for each XML attribute (for example, constrained) of each Option.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1d84-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1d84-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1d84-122">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b1d84-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



