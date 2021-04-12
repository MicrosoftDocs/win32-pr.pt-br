---
title: Funções do coletor de eventos do Windows
description: A lista a seguir descreve brevemente as funções que são usadas no coletor de eventos do Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291764"
---
# <a name="windows-event-collector-functions"></a><span data-ttu-id="f41fb-103">Funções do coletor de eventos do Windows</span><span class="sxs-lookup"><span data-stu-id="f41fb-103">Windows Event Collector Functions</span></span>

<span data-ttu-id="f41fb-104">A lista a seguir descreve brevemente as funções que são usadas no coletor de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="f41fb-104">The following list briefly describes the functions that are used in Windows Event Collector.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f41fb-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f41fb-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f41fb-106">**EcClose**</span><span class="sxs-lookup"><span data-stu-id="f41fb-106">**EcClose**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

<span data-ttu-id="f41fb-107">Fecha um identificador recebido de outras funções do coletor de eventos.</span><span class="sxs-lookup"><span data-stu-id="f41fb-107">Closes a handle received from other Event Collector functions.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-108">**EcDeleteSubscription**</span><span class="sxs-lookup"><span data-stu-id="f41fb-108">**EcDeleteSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

<span data-ttu-id="f41fb-109">Exclui uma assinatura existente.</span><span class="sxs-lookup"><span data-stu-id="f41fb-109">Deletes an existing subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-110">**EcEnumNextSubscription**</span><span class="sxs-lookup"><span data-stu-id="f41fb-110">**EcEnumNextSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

<span data-ttu-id="f41fb-111">Continua a enumeração das assinaturas registradas no computador local.</span><span class="sxs-lookup"><span data-stu-id="f41fb-111">Continues the enumeration of the subscriptions registered on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-112">**EcGetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="f41fb-112">**EcGetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="f41fb-113">Recupera valores de propriedade para as origens de evento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-113">Retrieves property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-114">**EcGetObjectArraySize**</span><span class="sxs-lookup"><span data-stu-id="f41fb-114">**EcGetObjectArraySize**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

<span data-ttu-id="f41fb-115">Recupera o número de índices da matriz de valores de propriedade para as origens de evento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-115">Retrieves the number of indexes of the array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-116">**EcGetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="f41fb-116">**EcGetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="f41fb-117">Recupera um valor de propriedade de um objeto de assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-117">Retrieves a property value from a subscription object.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-118">**EcGetSubscriptionRunTimeStatus**</span><span class="sxs-lookup"><span data-stu-id="f41fb-118">**EcGetSubscriptionRunTimeStatus**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

<span data-ttu-id="f41fb-119">Recupera as informações de status de tempo de execução para uma origem de evento de uma assinatura ou a própria assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-119">Retrieves the run time status information for an event source of a subscription or the subscription itself.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-120">**EcInsertObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="f41fb-120">**EcInsertObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

<span data-ttu-id="f41fb-121">Insere um objeto vazio em uma matriz de valores de propriedade para as origens de evento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-121">Inserts an empty object into an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-122">**EcOpenSubscriptionEnum**</span><span class="sxs-lookup"><span data-stu-id="f41fb-122">**EcOpenSubscriptionEnum**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

<span data-ttu-id="f41fb-123">Cria um enumerador de assinatura para enumerar todas as assinaturas registradas no computador local.</span><span class="sxs-lookup"><span data-stu-id="f41fb-123">Creates a subscription enumerator to enumerate all registered subscriptions on the local machine.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-124">**EcOpenSubscription**</span><span class="sxs-lookup"><span data-stu-id="f41fb-124">**EcOpenSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

<span data-ttu-id="f41fb-125">Abre uma assinatura existente ou cria uma nova assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-125">Opens an existing subscription or creates a new subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-126">**EcSaveSubscription**</span><span class="sxs-lookup"><span data-stu-id="f41fb-126">**EcSaveSubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

<span data-ttu-id="f41fb-127">Salva as informações de configuração da assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-127">Saves subscription configuration information.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-128">**EcSetObjectArrayProperty**</span><span class="sxs-lookup"><span data-stu-id="f41fb-128">**EcSetObjectArrayProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

<span data-ttu-id="f41fb-129">Define um valor de propriedade em uma matriz de valores de propriedade para as origens de evento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-129">Sets a property value in an array of property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-130">**EcSetSubscriptionProperty**</span><span class="sxs-lookup"><span data-stu-id="f41fb-130">**EcSetSubscriptionProperty**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

<span data-ttu-id="f41fb-131">Define novos valores ou atualiza os valores existentes de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-131">Sets new values or updates existing values of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-132">**EcRemoveObjectArrayElement**</span><span class="sxs-lookup"><span data-stu-id="f41fb-132">**EcRemoveObjectArrayElement**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

<span data-ttu-id="f41fb-133">Remove um elemento de uma matriz de objetos que contêm valores de propriedade para as origens de evento de uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="f41fb-133">Removes an element from an array of objects that contain property values for the event sources of a subscription.</span></span>

</dd> <dt>

[<span data-ttu-id="f41fb-134">**EcRetrySubscription**</span><span class="sxs-lookup"><span data-stu-id="f41fb-134">**EcRetrySubscription**</span></span>](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

<span data-ttu-id="f41fb-135">Tenta se conectar novamente à origem do evento de uma assinatura que não está conectada.</span><span class="sxs-lookup"><span data-stu-id="f41fb-135">Retries connecting to the event source of a subscription that is not connected.</span></span>

</dd> </dl>

 

 




