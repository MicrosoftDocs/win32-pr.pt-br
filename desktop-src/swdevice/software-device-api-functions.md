---
title: Funções de API de dispositivo de software
description: Esta seção descreve as funções de API de dispositivo de software que um aplicativo cliente chama e uma função de retorno de chamada implementada por um aplicativo cliente.
ms.assetid: 68F142A9-08AD-4F74-A0C3-3DCC8F7449B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f5d525eb9a4d4bc9af4807a2b3ad069b109b17874040e84cb3a9059d31bb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937086"
---
# <a name="software-device-api-functions"></a>Funções de API de dispositivo de software

Esta seção descreve as funções de API de dispositivo de software que um aplicativo cliente chama e uma função de retorno de chamada implementada por um aplicativo cliente.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                           | Descrição                                                                                                                                                      |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SwDeviceClose**](/windows/win32/api/swdevice/nf-swdevice-swdeviceclose)<br/>                               | Fecha o identificador de dispositivo de software. Quando o identificador for fechado, o PnP iniciará o processo de remoção do dispositivo.<br/>                                   |
| [**\_retorno de \_ \_ chamada do dispositivo SW**](/windows/win32/api/swdevice/nc-swdevice-sw_device_create_callback)<br/>    | Fornece um dispositivo com suporte no registro e permite que o chamador faça chamadas para funções de API de dispositivo de software com o identificador *hSwDevice* .<br/> |
| [**SwDeviceCreate**](/windows/win32/api/swdevice/nf-swdevice-swdevicecreate)<br/>                             | Inicia a enumeração de um dispositivo de software.<br/>                                                                                                       |
| [**SwDeviceGetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicegetlifetime)<br/>                   | Obtém o tempo de vida de um dispositivo de software. <br/>                                                                                                              |
| [**SwDeviceInterfacePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacepropertyset)<br/> | Define propriedades em uma interface de dispositivo de software. <br/>                                                                                                      |
| [**SwDeviceInterfaceRegister**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfaceregister)<br/>       | Registra uma interface de dispositivo para um dispositivo de software e, opcionalmente, define propriedades nessa interface. <br/>                                                 |
| [**SwDeviceInterfaceSetState**](/windows/win32/api/swdevice/nf-swdevice-swdeviceinterfacesetstate)<br/>       | Habilita ou desabilita uma interface de dispositivo para um dispositivo de software. <br/>                                                                                        |
| [**SwDevicePropertySet**](/windows/win32/api/swdevice/nf-swdevice-swdevicepropertyset)<br/>                   | Define propriedades em um dispositivo de software. <br/>                                                                                                                |
| [**SwDeviceSetLifetime**](/windows/win32/api/swdevice/nf-swdevice-swdevicesetlifetime)<br/>                   | Gerencia o tempo de vida de um dispositivo de software. <br/>                                                                                                           |
| [**SwMemFree**](/windows/win32/api/swdevice/nf-swdevice-swmemfree)<br/>                                       | Libera a memória que outras funções de API de dispositivo de software alocadas.<br/>                                                                                      |



 

 

 

[Enviar comentários sobre este tópico para a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20Functions%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Enviar comentários sobre este tópico para a Microsoft")