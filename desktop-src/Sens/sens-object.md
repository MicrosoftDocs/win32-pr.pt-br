---
description: O serviço de notificação de eventos do sistema (SENS) define a coclasse SENS como parte da biblioteca de tipos do SENS.
ms.assetid: b494808c-1116-47ac-8713-0d515b312368
title: Objeto SENS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d0d5cd857063d6ac224de66610d2604db619d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754946"
---
# <a name="sens-object"></a><span data-ttu-id="5eb0a-103">Objeto SENS</span><span class="sxs-lookup"><span data-stu-id="5eb0a-103">SENS Object</span></span>

<span data-ttu-id="5eb0a-104">O serviço de notificação de eventos do sistema (SENS) define a coclasse SENS como parte da biblioteca de tipos do SENS.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-104">The System Event Notification Service (SENS) defines the SENS coclass as part of the SENS type library.</span></span>

## <a name="implementation"></a><span data-ttu-id="5eb0a-105">Implementação</span><span class="sxs-lookup"><span data-stu-id="5eb0a-105">Implementation</span></span>

<span data-ttu-id="5eb0a-106">A implementação do objeto SENS é fornecida pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-106">The SENS object implementation is provided by the operating system.</span></span>

## <a name="creationaccess-functions"></a><span data-ttu-id="5eb0a-107">Funções de criação/acesso</span><span class="sxs-lookup"><span data-stu-id="5eb0a-107">Creation/Access Functions</span></span>



| <span data-ttu-id="5eb0a-108">Função</span><span class="sxs-lookup"><span data-stu-id="5eb0a-108">Function</span></span>                                      | <span data-ttu-id="5eb0a-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eb0a-109">Description</span></span>                                             |
|-----------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="5eb0a-110">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-110">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) | <span data-ttu-id="5eb0a-111">Cria uma instância do objeto SENS usando seu CLSID.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-111">Creates an instance of the SENS object using its CLSID.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="5eb0a-112">Interfaces</span><span class="sxs-lookup"><span data-stu-id="5eb0a-112">Interfaces</span></span>



| <span data-ttu-id="5eb0a-113">Interface</span><span class="sxs-lookup"><span data-stu-id="5eb0a-113">Interface</span></span>                            | <span data-ttu-id="5eb0a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5eb0a-114">Description</span></span>                                                                                         |
|--------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5eb0a-115">**IsensNetwork**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-115">**IsensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork) | <span data-ttu-id="5eb0a-116">Padrão.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-116">Default.</span></span> <span data-ttu-id="5eb0a-117">Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-117">Outgoing interface implemented by sink object in subscriber application.</span></span>                   |
| [<span data-ttu-id="5eb0a-118">**IsensOnNow**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-118">**IsensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)     | <span data-ttu-id="5eb0a-119">Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-119">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="5eb0a-120">**IsensLogon**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-120">**IsensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)     | <span data-ttu-id="5eb0a-121">Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-121">Outgoing interface implemented by sink object in subscriber application.</span></span>                            |
| [<span data-ttu-id="5eb0a-122">**IsensLogon2**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-122">**IsensLogon2**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon2)   | <span data-ttu-id="5eb0a-123">Interface de saída implementada pelo objeto de coletor no aplicativo de assinante.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-123">Outgoing interface implemented by sink object in subscriber application.</span></span> <span data-ttu-id="5eb0a-124">Disponível com o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5eb0a-124">Available with Windows XP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5eb0a-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5eb0a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5eb0a-126">**ISensLogon**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-126">**ISensLogon**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)
</dt> <dt>

[<span data-ttu-id="5eb0a-127">**ISensNetwork**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-127">**ISensNetwork**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)
</dt> <dt>

[<span data-ttu-id="5eb0a-128">**ISensOnNow**</span><span class="sxs-lookup"><span data-stu-id="5eb0a-128">**ISensOnNow**</span></span>](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow)
</dt> <dt>

[<span data-ttu-id="5eb0a-129">Sobre o serviço de notificação de eventos do sistema</span><span class="sxs-lookup"><span data-stu-id="5eb0a-129">About System Event Notification Service</span></span>](about-system-event-notification-service.md)
</dt> </dl>

 

 
