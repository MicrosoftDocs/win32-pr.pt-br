---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Suporte a deltas do PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105765784"
---
# <a name="supporting-printticket-deltas"></a><span data-ttu-id="707b0-104">Suporte a deltas do PrintTicket</span><span class="sxs-lookup"><span data-stu-id="707b0-104">Supporting PrintTicket Deltas</span></span>

<span data-ttu-id="707b0-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="707b0-105">This topic is not current.</span></span> <span data-ttu-id="707b0-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="707b0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="707b0-107">A interface do provedor PrintTicket tem métodos que podem ser usados para fazer alterações incrementais em um PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="707b0-107">The PrintTicket Provider Interface has methods that can be used to make incremental changes to an existing PrintTicket.</span></span> <span data-ttu-id="707b0-108">As alterações incrementais do PrintTicket podem ser especificadas em um PrintTicket parcial conhecido como um Delta PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="707b0-108">The incremental PrintTicket changes can be specified in a partial PrintTicket that is known as a PrintTicket delta.</span></span> <span data-ttu-id="707b0-109">Um PrintTicket revisado é criado pela mesclagem de um Delta PrintTicket com um PrintTicket existente.</span><span class="sxs-lookup"><span data-stu-id="707b0-109">A revised PrintTicket is created by merging a PrintTicket delta with an existing PrintTicket.</span></span> <span data-ttu-id="707b0-110">Consulte o documento da interface do provedor do PrintTicket em breve para obter mais informações sobre métodos envolvendo deltas PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="707b0-110">See the forthcoming PrintTicket Provider Interface document for more information about methods involving PrintTicket deltas.</span></span>

<span data-ttu-id="707b0-111">Quando um Delta PrintTicket é processado, as etapas a seguir devem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="707b0-111">When a PrintTicket delta is processed, the following steps must be performed.</span></span>

1.  <span data-ttu-id="707b0-112">Identifique as instâncias de recurso ou ParameterInit que são comuns ao PrintTicket existente (o PrintTicket de destino) e ao Delta do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="707b0-112">Identify Feature or ParameterInit instances that are common to both the existing PrintTicket (the target PrintTicket) and the PrintTicket delta.</span></span>

    -   <span data-ttu-id="707b0-113">Para cada recurso comum ao PrintTicket de destino e ao Delta do PrintTicket, substitua o recurso no PrintTicket de destino pelo recurso correspondente no Delta do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="707b0-113">For each Feature common to both the target PrintTicket and the PrintTicket delta, replace the Feature in the target PrintTicket by the corresponding Feature in the PrintTicket delta.</span></span>

    -   <span data-ttu-id="707b0-114">Para cada ParameterInit comum ao PrintTicket de destino e ao Delta do PrintTicket, substitua o ParameterInit no PrintTicket de destino pelo ParameterInit correspondente no Delta do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="707b0-114">For each ParameterInit common to both the target PrintTicket and the PrintTicket delta, replace the ParameterInit in the target PrintTicket by the corresponding ParameterInit in the PrintTicket delta.</span></span>

2.  <span data-ttu-id="707b0-115">Copie todas as instâncias restantes do recurso e do ParameterInit no Delta do PrintTicket para o PrintTicket de destino.</span><span class="sxs-lookup"><span data-stu-id="707b0-115">Copy all remaining Feature and ParameterInit instances in the PrintTicket delta to the target PrintTicket.</span></span>

3.  <span data-ttu-id="707b0-116">Se o algoritmo de resolução de conflitos permitir que as prioridades sejam especificadas no próprio PrintTicket, você poderá optar por elevar as prioridades do recurso e das instâncias ParameterInit nomeadas no Delta do PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="707b0-116">If your conflict resolution algorithm allows priorities to be specified in the PrintTicket itself, you may choose to elevate the priorities of the Feature and ParameterInit instances named in the PrintTicket delta.</span></span>

4.  <span data-ttu-id="707b0-117">Execute a validação de PrintTicket conforme descrito na [lista de verificação de validação do PrintTicket](printticket-validation-checklist.md).</span><span class="sxs-lookup"><span data-stu-id="707b0-117">Perform PrintTicket validation as described in [PrintTicket Validation Checklist](printticket-validation-checklist.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="707b0-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="707b0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="707b0-119">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="707b0-119">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



