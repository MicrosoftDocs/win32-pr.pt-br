---
title: Obtendo SDOs de serviço e usuário
description: Para obter o SDOs para NPS (IAS) ou um usuário específico, chame os métodos ISdoMachine GetServiceSDO ou ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294252"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="a666e-103">Obtendo SDOs de serviço e usuário</span><span class="sxs-lookup"><span data-stu-id="a666e-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="a666e-104">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a666e-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="a666e-105">Para obter o SDOs para NPS (IAS) ou um usuário específico, chame os métodos [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) .</span><span class="sxs-lookup"><span data-stu-id="a666e-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="a666e-106">Esses métodos retornam ponteiros para interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="a666e-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="a666e-107">Para o usuário SDO, use o método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter uma interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a666e-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="a666e-108">Para o SDO de serviço, use **IUnknown:: QueryInterface** para obter uma interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) ou uma interface [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .</span><span class="sxs-lookup"><span data-stu-id="a666e-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="a666e-109">Antes de chamar [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), chame [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) para associar o objeto de computador ao computador local.</span><span class="sxs-lookup"><span data-stu-id="a666e-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="a666e-110">Consulte [recuperando um serviço de SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) e [recuperando um SDO de usuário](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) para código de exemplo que demonstra como obter esses SDOs.</span><span class="sxs-lookup"><span data-stu-id="a666e-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 