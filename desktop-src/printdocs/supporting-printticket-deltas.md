---
description: Saiba mais sobre como dar suporte a deltas printTicket. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Suporte a deltas PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548774"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="bf975-105">Suporte a deltas PrintTicket</span><span class="sxs-lookup"><span data-stu-id="bf975-105">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="bf975-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="bf975-106">This topic is not current.</span></span> <span data-ttu-id="bf975-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="bf975-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bf975-108">A Interface do Provedor PrintTicket tem métodos que podem ser usados para fazer alterações incrementais em um PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="bf975-108">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="bf975-109">As alterações incrementais de PrintTicket podem ser especificadas em um PrintTicket parcial que é conhecido como um delta printTicket.</span><span class="sxs-lookup"><span data-stu-id="bf975-109">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="bf975-110">Um PrintTicket revisado é criado mesclando um delta printTicket com um PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="bf975-110">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="bf975-111">Consulte o próximo documento da Interface do Provedor PrintTicket para obter mais informações sobre métodos que envolvem deltas printTicket.</span><span class="sxs-lookup"><span data-stu-id="bf975-111">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="bf975-112">Quando um delta printTicket é processado, as etapas a seguir devem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="bf975-112">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="bf975-113">Identifique instâncias de Recurso ou ParameterInit que são comuns ao PrintTicket existente (o PrintTicket de destino) e ao delta printTicket.</span><span class="sxs-lookup"><span data-stu-id="bf975-113">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="bf975-114">Para cada Recurso comum ao PrintTicket de destino e ao delta PrintTicket, substitua o Recurso no PrintTicket de destino pelo Recurso correspondente no delta printTicket.</span><span class="sxs-lookup"><span data-stu-id="bf975-114">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="bf975-115">Para cada ParameterInit comum ao PrintTicket de destino e ao delta PrintTicket, substitua ParameterInit no PrintTicket de destino pelo ParameterInit correspondente no delta printTicket.</span><span class="sxs-lookup"><span data-stu-id="bf975-115">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="bf975-116">Copie todas as instâncias restantes de Recurso e ParameterInit no delta PrintTicket para o PrintTicket de destino.</span><span class="sxs-lookup"><span data-stu-id="bf975-116">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="bf975-117">Se o algoritmo de resolução de conflitos permitir que as prioridades sejam especificadas no próprio PrintTicket, você poderá optar por elevar as prioridades das instâncias Feature e ParameterInit nomeadas no delta printTicket.</span><span class="sxs-lookup"><span data-stu-id="bf975-117">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="bf975-118">Execute a validação printTicket, conforme descrito em [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="bf975-118">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf975-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf975-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf975-120">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="bf975-120">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



