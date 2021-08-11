---
title: Delegados
description: A API de Streaming de Mídia fornece as seguintes funções de manipulador de eventos.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb7dc8f0896c23e7b7cacc42070b454e4dbffc7e016ff978382bd48e837ac11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236400"
---
# <a name="delegates"></a>Delegados

A [API de Streaming de Mídia](media-streaming-api-portal.md) fornece as seguintes funções de manipulador de eventos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))<br/>                   | Representa a função que manipulará o [**evento ConnectionStatusChanged**](connectionstatuschanged.md) que notifica o cliente de alterações no status de conexão de rede do dispositivo.<br/>               |
| [**DeviceControllerHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))<br/>       | Representa a função que manipulará os eventos [**DeviceArrival**](devicearrival.md) e [**DeviceDeparture**](devicedeparture.md) que notificam o cliente sobre alterações na lista de dispositivos armazenados em cache.<br/> |
| [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))<br/> | Representa a função que manipulará o evento [**RenderingParametersUpdate,**](renderingparametersupdate.md) que notifica o cliente de uma atualização para qualquer um dos parâmetros de controle de renderização da DMR.<br/>  |
| [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))<br/> | Representa a função que manipulará o evento [**TransportParametersUpdate,**](transportparametersupdate.md) que notifica o cliente de uma atualização para qualquer um dos parâmetros de transporte da DMR.<br/>          |



 

 

