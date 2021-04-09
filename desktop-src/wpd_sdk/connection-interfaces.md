---
description: Interfaces de conexão MTP/Bluetooth
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de conexão MTP/Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011675"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfaces de conexão MTP/Bluetooth

As interfaces a seguir permitem que os aplicativos enumerem e se conectem somente a dispositivos que dão suporte ao MTP (protocolo de transferência de mídia) via Bluetooth (MTP/Bluetooth). As interfaces de driver, coleção e cliente WPD não são restritas ao protocolo MTP/Bluetooth.



| Interface                                                              | Descrição                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Define um único método de retorno de chamada que os aplicativos usam para receber notificação de solicitações concluídas e canceladas. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera as interfaces **IPortableDeviceConnector** .                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Dá suporte a métodos que os aplicativos chamam para estabelecer conexões com dispositivos Bluetooth MTP.                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



