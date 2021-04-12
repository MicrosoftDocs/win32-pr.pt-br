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
# <a name="obtaining-service-and-user-sdos"></a>Obtendo SDOs de serviço e usuário

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.

 

Para obter o SDOs para NPS (IAS) ou um usuário específico, chame os métodos [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) . Esses métodos retornam ponteiros para interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para esses objetos. Para o usuário SDO, use o método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter uma interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para o objeto. Para o SDO de serviço, use **IUnknown:: QueryInterface** para obter uma interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) ou uma interface [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .

Antes de chamar [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) ou [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), chame [**ISdoMachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) para associar o objeto de computador ao computador local.

Consulte [recuperando um serviço de SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) e [recuperando um SDO de usuário](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) para código de exemplo que demonstra como obter esses SDOs.

 

 