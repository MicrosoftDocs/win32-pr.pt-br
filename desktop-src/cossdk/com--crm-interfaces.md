---
description: As interfaces de CRM são necessárias para fornecer suporte para trabalhadores de CRM e compensadores de CRM desenvolvidos usando Visual Basic e Visual C++.
ms.assetid: 68a75da7-1f35-41a4-8872-e3f4ad1fc30d
title: Interfaces do CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ba3235b1cd2a82fc913dd676bbb78324f340cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646526"
---
# <a name="com-crm-interfaces"></a><span data-ttu-id="099aa-103">Interfaces do CRM COM+</span><span class="sxs-lookup"><span data-stu-id="099aa-103">COM+ CRM Interfaces</span></span>

<span data-ttu-id="099aa-104">As interfaces de CRM são necessárias para fornecer suporte para trabalhadores de CRM e compensadores de CRM desenvolvidos usando Visual Basic e Visual C++.</span><span class="sxs-lookup"><span data-stu-id="099aa-104">The CRM interfaces are required to provide support for CRM Workers and CRM Compensators developed using Visual Basic and Visual C++.</span></span>

<span data-ttu-id="099aa-105">Você pode usar o CRM (Gerenciador de recursos de compensação COM+) para integrar com rapidez e facilidade recursos de aplicativos com transações do Microsoft Coordenador de Transações Distribuídas (DTC).</span><span class="sxs-lookup"><span data-stu-id="099aa-105">You can use the COM+ Compensating Resource Manager (CRM) to quickly and easily integrate application resources with Microsoft Distributed Transaction Coordinator (DTC) transactions.</span></span>

<span data-ttu-id="099aa-106">É mais fácil para os componentes escritos com Visual Basic criar um registro de log como uma coleção de variantes.</span><span class="sxs-lookup"><span data-stu-id="099aa-106">It is easier for components written with Visual Basic to build up a log record as a collection of Variants.</span></span> <span data-ttu-id="099aa-107">Além disso, Visual Basic componentes são segmentados em apartamento, o que implica que deve ser possível realizar marshaling das interfaces do apartamento multithread para um apartamento de thread único.</span><span class="sxs-lookup"><span data-stu-id="099aa-107">Also, Visual Basic components are apartment threaded, which implies that it must be possible to marshal the interfaces from the multithreaded apartment to a single-threaded apartment.</span></span> <span data-ttu-id="099aa-108">Os componentes do CRM desenvolvidos com o Visual C++ também podem usar o modelo de Threading Apartment, embora seja recomendável que eles usem o modelo de Threading em vez disso.</span><span class="sxs-lookup"><span data-stu-id="099aa-108">CRM components developed with Visual C++ could also use the Apartment threading model, although it is recommended that these use the Both threading model instead.</span></span>

<span data-ttu-id="099aa-109">As interfaces descritas na tabela a seguir fornecem informações de referência detalhadas para desenvolvedores de COM+ CRMs.</span><span class="sxs-lookup"><span data-stu-id="099aa-109">The interfaces described in the following table provide detailed reference information for developers of COM+ CRMs.</span></span>



| <span data-ttu-id="099aa-110">Interfaces do CRM</span><span class="sxs-lookup"><span data-stu-id="099aa-110">CRM interfaces</span></span>                                             | <span data-ttu-id="099aa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="099aa-111">Description</span></span>                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="099aa-112">**ICrmCompensator**</span><span class="sxs-lookup"><span data-stu-id="099aa-112">**ICrmCompensator**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator)                 | <span data-ttu-id="099aa-113">Essa interface fornece registros de log não estruturados em Visual C++.</span><span class="sxs-lookup"><span data-stu-id="099aa-113">This interface delivers unstructured log records in Visual C++.</span></span>                                                           |
| [<span data-ttu-id="099aa-114">**ICrmCompensatorVariants**</span><span class="sxs-lookup"><span data-stu-id="099aa-114">**ICrmCompensatorVariants**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensatorvariants) | <span data-ttu-id="099aa-115">Essa interface fornece registros de log estruturados para o compensador de CRM ao usar o Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="099aa-115">This interface delivers structured log records to the CRM Compensator when using Visual Basic.</span></span>                            |
| [<span data-ttu-id="099aa-116">**ICrmFormatLogRecords**</span><span class="sxs-lookup"><span data-stu-id="099aa-116">**ICrmFormatLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmformatlogrecords)       | <span data-ttu-id="099aa-117">Essa interface converte os registros de log no formato exibível para que eles possam ser apresentados usando uma ferramenta de monitoramento genérica.</span><span class="sxs-lookup"><span data-stu-id="099aa-117">This interface converts the log records to viewable format so that they can be presented using a generic monitoring tool.</span></span> |
| [<span data-ttu-id="099aa-118">**ICrmLogControl**</span><span class="sxs-lookup"><span data-stu-id="099aa-118">**ICrmLogControl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmlogcontrol)                   | <span data-ttu-id="099aa-119">Essa interface é usada pelo compensador CRM e CRM para gravar registros no log e torná-los duráveis.</span><span class="sxs-lookup"><span data-stu-id="099aa-119">This interface is used by the CRM Worker and CRM Compensator to write records to the log and make them durable.</span></span>           |
| [<span data-ttu-id="099aa-120">**ICrmMonitor**</span><span class="sxs-lookup"><span data-stu-id="099aa-120">**ICrmMonitor**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitor)                         | <span data-ttu-id="099aa-121">Essa interface captura um instantâneo do estado atual de um CRM e mantém um funcionário específico do CRM.</span><span class="sxs-lookup"><span data-stu-id="099aa-121">This interface captures a snapshot of the current state of a CRM and holds a specific CRM clerk.</span></span>                          |
| [<span data-ttu-id="099aa-122">**ICrmMonitorClerks**</span><span class="sxs-lookup"><span data-stu-id="099aa-122">**ICrmMonitorClerks**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorclerks)             | <span data-ttu-id="099aa-123">Essa interface obtém informações sobre o estado dos auxiliares.</span><span class="sxs-lookup"><span data-stu-id="099aa-123">This interface obtains information about the state of clerks.</span></span>                                                             |
| [<span data-ttu-id="099aa-124">**ICrmMonitorLogRecords**</span><span class="sxs-lookup"><span data-stu-id="099aa-124">**ICrmMonitorLogRecords**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmmonitorlogrecords)     | <span data-ttu-id="099aa-125">Essa interface monitora os registros de log individuais mantidos por um vendedor de CRM específico para uma determinada transação.</span><span class="sxs-lookup"><span data-stu-id="099aa-125">This interface monitors the individual log records maintained by a specific CRM clerk for a given transaction.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="099aa-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="099aa-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="099aa-127">Conceitos do Gerenciador de recursos de compensação COM+</span><span class="sxs-lookup"><span data-stu-id="099aa-127">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



