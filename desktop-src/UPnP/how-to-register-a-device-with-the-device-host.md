---
title: Como registrar um dispositivo com o host do dispositivo
description: Você pode registrar um dispositivo em execução ou um dispositivo não em execução.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8425578dbd5ccc76685c2a142bee8d2167c4058341c32e4b03bcedca15041579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867576"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Como registrar um dispositivo com o host do dispositivo

Você pode registrar um dispositivo em execução ou um dispositivo não em execução.

## <a name="registering-a-running-device"></a>Registrando um dispositivo em execução

Os dispositivos são registrados usando a interface [**IUPnPRegistrar.**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) Somente os administradores têm permissão para registrar dispositivos em execução. Para registrar um dispositivo que tem um objeto de controle de dispositivo em execução, um aplicativo deve invocar [**IUPnPRegistrar::RegisterRunningDevice,**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)passando o seguinte:

-   O texto da descrição do dispositivo.
-   Um **ponteiro IUnknown** para o objeto de controle do dispositivo.
-   Uma cadeia de caracteres de inicialização passada para o método [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle do dispositivo.
-   O local do diretório de recursos.
-   O tempo de vida do dispositivo.
-   O parâmetro ID do dispositivo (um parâmetro OUT), que é o valor de retorno dessa chamada; um ponteiro para a ID do dispositivo é retornado em C++.

## <a name="registering-a-non-running-device"></a>Registrando um dispositivo não em execução

Por padrão, somente administradores e usuários interativos têm permissão para registrar dispositivos não em execução. Para registrar um dispositivo com um objeto de controle de dispositivo que não está em execução, o aplicativo usa o método [**IUPnPRegistrar::RegisterDevice.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)

Para registrar programaticamente um dispositivo com um objeto de controle de dispositivo não em execução, o aplicativo deve invocar [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) e passar os seguintes parâmetros:

-   O texto da descrição do dispositivo.
-   O ProgID do objeto de controle do dispositivo.
-   Uma cadeia de caracteres de inicialização passada para o método [**IUPnPDeviceControl::Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) do objeto de controle do dispositivo.
-   Uma ID de contêiner.
-   O local do diretório de recursos.
-   O tempo de vida do dispositivo.
-   O parâmetro ID do dispositivo (um parâmetro OUT), que é o valor de retorno dessa chamada; um ponteiro para a ID do dispositivo é retornado em C++.

Os registros de dispositivos não em execução podem ser configurados para persistir entre as inicializações do sistema (os dispositivos não são publicados durante a fase de desligamento). Portanto, se eles são configurados dessa forma, os dispositivos são publicados e anunciados sempre que o computador é inicializado.

 

 




