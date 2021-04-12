---
description: Usado pelo serviço de notificação de eventos do sistema do Microsoft Internet Explorer (SENS) para acessar o armazenamento de dados de eventos. Essa interface estende a interface IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interface IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457094"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="cf117-104">Interface IEventSystem2</span><span class="sxs-lookup"><span data-stu-id="cf117-104">IEventSystem2 interface</span></span>

<span data-ttu-id="cf117-105">Usado pelo serviço de notificação de eventos do sistema do Microsoft Internet Explorer (SENS) para acessar o armazenamento de dados de eventos.</span><span class="sxs-lookup"><span data-stu-id="cf117-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="cf117-106">Essa interface estende a interface [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .</span><span class="sxs-lookup"><span data-stu-id="cf117-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="cf117-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="cf117-107">When to implement</span></span>

<span data-ttu-id="cf117-108">Você não precisa implementar a interface **IEventSystem2** .</span><span class="sxs-lookup"><span data-stu-id="cf117-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="cf117-109">Um objeto de sistema de eventos fornecido pelo sistema (CLSID \_ CEventSystem) implementa **IEventSystem2**.</span><span class="sxs-lookup"><span data-stu-id="cf117-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="cf117-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="cf117-110">When to use</span></span>

<span data-ttu-id="cf117-111">Se você usar o SENS, poderá chamar os métodos de **IEventSystem2** para adicionar e remover objetos de e para o repositório de eventos e para obter objetos do repositório de eventos.</span><span class="sxs-lookup"><span data-stu-id="cf117-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="cf117-112">Como [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) e o objeto Publicador não têm mais suporte, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) não é chamado no método [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .</span><span class="sxs-lookup"><span data-stu-id="cf117-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="cf117-113">Membros</span><span class="sxs-lookup"><span data-stu-id="cf117-113">Members</span></span>

<span data-ttu-id="cf117-114">A interface **IEventSystem2** herda de **IEventSystem**.</span><span class="sxs-lookup"><span data-stu-id="cf117-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="cf117-115">**IEventSystem2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cf117-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="cf117-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf117-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cf117-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="cf117-117">Methods</span></span>

<span data-ttu-id="cf117-118">A interface **IEventSystem2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cf117-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="cf117-119">Método</span><span class="sxs-lookup"><span data-stu-id="cf117-119">Method</span></span>                                                                         | <span data-ttu-id="cf117-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf117-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="cf117-121">**Obter versão**</span><span class="sxs-lookup"><span data-stu-id="cf117-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="cf117-122">Recupera o número de versão do sistema de eventos.</span><span class="sxs-lookup"><span data-stu-id="cf117-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="cf117-123">**VerifyTransientSubscribers**</span><span class="sxs-lookup"><span data-stu-id="cf117-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="cf117-124">Verifica a existência de todos os assinantes transitórios no repositório de dados.</span><span class="sxs-lookup"><span data-stu-id="cf117-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cf117-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf117-125">Requirements</span></span>



| <span data-ttu-id="cf117-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf117-126">Requirement</span></span> | <span data-ttu-id="cf117-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cf117-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="cf117-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf117-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf117-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf117-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cf117-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf117-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf117-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf117-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="cf117-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf117-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf117-133">**IEventSystem**</span><span class="sxs-lookup"><span data-stu-id="cf117-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

