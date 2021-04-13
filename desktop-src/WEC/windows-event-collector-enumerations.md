---
title: Enumerações do coletor de eventos do Windows
description: A tabela a seguir lista as enumerações do SDK do coletor de eventos do Windows.
ms.assetid: 3775aa7c-ef35-4534-b709-15624fd7a90d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d2617c6eb0052ec1ac41d5f197d9216c253054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364090"
---
# <a name="windows-event-collector-enumerations"></a><span data-ttu-id="73108-103">Enumerações do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="73108-103">Windows Event Collector Enumerations</span></span>

<span data-ttu-id="73108-104">A tabela a seguir lista as enumerações do SDK do coletor de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="73108-104">The following table lists the enumerations of the Windows Event Collector SDK.</span></span>



| <span data-ttu-id="73108-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="73108-105">Enumeration</span></span>                                                                                               | <span data-ttu-id="73108-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="73108-106">Description</span></span>                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73108-107">**\_modo de \_ configuração de assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-107">**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)                       | <span data-ttu-id="73108-108">Especifica modos de configuração diferentes que alteram as configurações padrão de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="73108-108">Specifies different configuration modes that change the default settings for a subscription.</span></span>                                            |
| [<span data-ttu-id="73108-109">**\_formato de \_ conteúdo de assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-109">**EC\_SUBSCRIPTION\_CONTENT\_FORMAT**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_content_format)                               | <span data-ttu-id="73108-110">Especifica como os eventos serão processados no computador que envia os eventos antes que os eventos sejam enviados para o computador do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="73108-110">Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.</span></span> |
| [<span data-ttu-id="73108-111">**\_tipo de \_ credenciais de assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-111">**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)                           | <span data-ttu-id="73108-112">Especifica o tipo de credenciais a ser usado ao se comunicar com origens de evento.</span><span class="sxs-lookup"><span data-stu-id="73108-112">Specifies the type of credentials to use when communicating with event sources.</span></span>                                                         |
| [<span data-ttu-id="73108-113">**\_modo de \_ entrega de assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-113">**EC\_SUBSCRIPTION\_DELIVERY\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_delivery_mode)                                 | <span data-ttu-id="73108-114">Especifica como os eventos são entregues por meio de uma assinatura de evento (usando um modelo de Push ou pull).</span><span class="sxs-lookup"><span data-stu-id="73108-114">Specifies how events are delivered through an event subscription (using a push or pull model).</span></span>                                          |
| [<span data-ttu-id="73108-115">**\_ID da \_ propriedade da assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-115">**EC\_SUBSCRIPTION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)                                     | <span data-ttu-id="73108-116">Define valores para identificar as propriedades de assinatura de evento usadas para configuração de assinatura.</span><span class="sxs-lookup"><span data-stu-id="73108-116">Defines values to identify event subscription properties used for subscription configuration.</span></span>                                           |
| [<span data-ttu-id="73108-117">**\_ \_ \_ status ativo do status de tempo de execução da \_ assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-117">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_ACTIVE\_STATUS**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_active_status) | <span data-ttu-id="73108-118">Especifica o status de uma assinatura ou uma origem do evento em relação a uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="73108-118">Specifies the status of a subscription or an event source with respect to a subscription.</span></span>                                               |
| [<span data-ttu-id="73108-119">**\_ID das \_ informações de status do tempo de execução da assinatura do \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="73108-119">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id)             | <span data-ttu-id="73108-120">Especifica um valor que identifica uma propriedade do status de tempo de execução de uma origem de evento ou uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="73108-120">Specifies a value that identifies a property of the runtime status of an event source or a subscription.</span></span>                                |
| [<span data-ttu-id="73108-121">**\_tipo de assinatura do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-121">**EC\_SUBSCRIPTION\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_type)                                                    | <span data-ttu-id="73108-122">Especifica o tipo de assinatura a ser usado (uma assinatura iniciada por uma fonte ou iniciada pelo coletor).</span><span class="sxs-lookup"><span data-stu-id="73108-122">Specifies the type of subscription to use (a source initiated or collector initiated subscription).</span></span>                                     |
| [<span data-ttu-id="73108-123">**\_tipo de variante do EC \_**</span><span class="sxs-lookup"><span data-stu-id="73108-123">**EC\_VARIANT\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_variant_type)                                                              | <span data-ttu-id="73108-124">Define os valores que especificam os tipos de dados que são usados nas funções do coletor de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="73108-124">Defines the values that specify the data types that are used in the Windows Event Collector functions.</span></span>                                  |



 

 

 




