---
title: Como registrar um dispositivo no host do dispositivo
description: Você pode registrar um dispositivo em execução ou um dispositivo que não esteja em execução.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005557"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Como registrar um dispositivo no host do dispositivo

Você pode registrar um dispositivo em execução ou um dispositivo que não esteja em execução.

## <a name="registering-a-running-device"></a>Registrando um dispositivo em execução

Os dispositivos são registrados usando a interface [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Somente administradores têm permissão para registrar dispositivos em execução. Para registrar um dispositivo que tem um objeto de controle de dispositivo em execução, um aplicativo deve invocar [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), passando o seguinte:

-   O texto da descrição do dispositivo.
-   Um ponteiro **IUnknown** para o objeto de controle de dispositivo.
-   Uma cadeia de inicialização que é passada para o método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle de dispositivo.
-   O local do diretório de recursos.
-   O tempo de vida do dispositivo.
-   O parâmetro de ID do dispositivo (um parâmetro OUT), que é o valor de retorno dessa chamada; um ponteiro para a ID do dispositivo é retornado em C++.

## <a name="registering-a-non-running-device"></a>Registrando um dispositivo que não está em execução

Por padrão, somente administradores e usuários interativos têm permissão para registrar dispositivos que não estão em execução. Para registrar um dispositivo com um objeto de controle de dispositivo que não está em execução, o aplicativo usa o método [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .

Para registrar um dispositivo de forma programática com um objeto de controle de dispositivo que não está em execução, o aplicativo deve invocar [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) e passá-lo para os seguintes parâmetros:

-   O texto da descrição do dispositivo.
-   O ProgID do objeto de controle de dispositivo.
-   Uma cadeia de inicialização que é passada para o método [**IUPnPDeviceControl:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle de dispositivo.
-   Uma ID de contêiner.
-   O local do diretório de recursos.
-   O tempo de vida do dispositivo.
-   O parâmetro de ID do dispositivo (um parâmetro OUT), que é o valor de retorno dessa chamada; um ponteiro para a ID do dispositivo é retornado em C++.

Os registros de dispositivos que não estão em execução podem ser configurados para persistir nas inicializações do sistema (os dispositivos não são publicados durante a fase de desligamento). Portanto, se eles estiverem configurados dessa forma, os dispositivos serão publicados e anunciados toda vez que o computador for inicializado.

 

 




