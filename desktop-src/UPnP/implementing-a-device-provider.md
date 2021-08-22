---
title: Implementando um provedor de dispositivos
description: Para implementar um provedor de dispositivos, crie um objeto que expõe a interface IUPnPDeviceProvider.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19823357389a513a095081ce6ca79176af79897273274cc1f0e59a56e29b339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999646"
---
# <a name="implementing-a-device-provider"></a>Implementando um provedor de dispositivos

Para implementar um provedor de dispositivos, crie um objeto que expõe a interface [**IUPnPDeviceProvider.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) Esse objeto deve ser registrado com o host do dispositivo usando o [**método IUPnPRegistrar::RegisterDeviceProvider.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) Esse método recebe os seguintes parâmetros:

-   O nome do provedor, que deve ser exclusivo no computador.
-   O ProgID da classe que implementa o provedor de dispositivos.
-   Uma cadeia de caracteres de inicialização que é passada para o provedor de dispositivos quando ela é iniciada.
-   Uma ID de contêiner. Uma ID de contêiner é uma cadeia de caracteres que identifica o grupo ao qual o dispositivo pertence. Todos os dispositivos com o mesmo identificador de contêiner são hospedados no mesmo processo.

 

 




