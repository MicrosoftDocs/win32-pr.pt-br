---
title: Implementando um provedor de dispositivo
description: Para implementar um provedor de dispositivo, crie um objeto que expõe a interface IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453717"
---
# <a name="implementing-a-device-provider"></a>Implementando um provedor de dispositivo

Para implementar um provedor de dispositivo, crie um objeto que expõe a interface [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) . Esse objeto deve ser registrado com o host do dispositivo usando o método [**IUPnPRegistrar:: RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) . Esse método usa os seguintes parâmetros:

-   O nome do provedor, que deve ser exclusivo no computador.
-   O ProgID da classe que implementa o provedor do dispositivo.
-   Uma cadeia de inicialização que é passada para o provedor do dispositivo quando ele é iniciado.
-   Uma ID de contêiner. Uma ID de contêiner é uma cadeia de caracteres que identifica o grupo ao qual o dispositivo pertence. Todos os dispositivos com o mesmo identificador de contêiner são hospedados no mesmo processo.

 

 




