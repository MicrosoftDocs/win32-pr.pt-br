---
description: Interfaces de conexão Bluetooth MTP
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: Interfaces de conexão Bluetooth MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0f32717afe14be05cae6e43d097e67fc9790729e5be4ce9c2dfa6f901a126a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843363"
---
# <a name="mtpbluetooth-connection-interfaces"></a>Interfaces de conexão Bluetooth MTP

As interfaces a seguir permitem que os aplicativos enumerem e conectem-se somente a dispositivos que suportam o protocolo MTP por Bluetooth (MTP/Bluetooth). As interfaces de cliente, coleção e driver WPD não estão restritas ao protocolo MTP/Bluetooth.



| Interface                                                              | Descrição                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**IConnectionRequestCallback**](iconnectionrequestcallback.md)       | Define um único método de retorno de chamada que os aplicativos usam para receber notificação de solicitações concluídas e canceladas. |
| [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) | Enumera interfaces **IPortableDeviceConnector.**                                                                 |
| [**IPortableDeviceConnector**](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | Dá suporte a métodos que os aplicativos chamam para estabelecer conexões com dispositivos Bluetooth MTP.                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 



