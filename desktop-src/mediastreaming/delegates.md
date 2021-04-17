---
title: Delegados
description: A API de streaming de mídia fornece as seguintes funções de manipulador de eventos.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499029"
---
# <a name="delegates"></a>Delegados

A [API de streaming de mídia](media-streaming-api-portal.md) fornece as seguintes funções de manipulador de eventos.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                   | Descrição                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))<br/>                   | Representa a função que manipulará o evento [**ConnectionStatusChanged**](connectionstatuschanged.md) , que notifica o cliente sobre as alterações no status de conexão de rede do dispositivo.<br/>               |
| [**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))<br/>       | Representa a função que manipulará os eventos [**DeviceArrival**](devicearrival.md) e [**DeviceDeparture**](devicedeparture.md) que notificam o cliente sobre as alterações na lista de dispositivos armazenados em cache.<br/> |
| [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))<br/> | Representa a função que manipulará o evento [**RenderingParametersUpdate**](renderingparametersupdate.md) , que notifica o cliente sobre uma atualização para qualquer um dos parâmetros de controle de RENDERIZAÇÃO de DMR s.<br/>  |
| [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))<br/> | Representa a função que manipulará o evento [**TransportParametersUpdate**](transportparametersupdate.md) , que notifica o cliente sobre uma atualização para qualquer um dos parâmetros de transporte de DMR.<br/>          |



 

 

