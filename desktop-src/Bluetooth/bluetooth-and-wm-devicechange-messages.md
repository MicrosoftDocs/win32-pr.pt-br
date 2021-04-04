---
title: Mensagens de WM_DEVICECHANGE e Bluetooth
description: O Bluetooth inclui mensagens específicas do DEVICECHANGE do WM \_ que permitem aos desenvolvedores obter mensagens quando os dispositivos Bluetooth sofrerem alterações de status.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917391"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Mensagens DEVICECHANGE do Bluetooth e do WM \_

O Bluetooth inclui mensagens específicas do [**\_ DEVICECHANGE do WM**](/windows/desktop/DevIO/wm-devicechange) que permitem aos desenvolvedores obter mensagens quando os dispositivos Bluetooth sofrerem alterações de status. Este tópico descreve como receber mensagens **\_ DEVICECHANGE do WM** específicas do Bluetooth e lista mensagens específicas do Bluetooth.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Recebendo mensagens DEVICECHANGE do WM específicas do Bluetooth \_

Para receber mensagens do [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , primeiro é necessário abrir um identificador para o rádio local. Para tal, use um dos seguintes métodos:

-   Use a função [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) com os seguintes parâmetros: (GUID \_ BTHPORT \_ Device \_ interface,..., DIGCF \_ presente \| DIGCF \_ DEVICEINTERFACE) e, em seguida, use as funções [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)e [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .
-   Use as funções [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)e [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .

Quando o identificador de rádio Bluetooth for aberto, chame a função [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) e registre-se para obter notificações sobre o identificador usando **DBT \_ DEVTYP \_ Handle** como o DeviceType. Quando registrado, os GUIDs a seguir são enviados e o membro de [**transmissão do dev \_ \_**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_ Data** member é o buffer associado.

## <a name="bluetooth-specific-messages"></a>Mensagens específicas do Bluetooth

A tabela a seguir lista as mensagens [**\_ DEVICECHANGE do WM**](/windows/desktop/DevIO/wm-devicechange) específicas do Bluetooth.

| GUID                                   | BUFFER                                                  | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_evento de \_ HCI do Bluetooth do GUID \_            | [**\_informações do \_ evento BTH HCI \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Essa mensagem é enviada quando um dispositivo Bluetooth remoto se conecta ou se desconecta no nível de ACL.                                                                                                                                                                                                                                                                    |
| \_ \_ Evento L2CAP de Bluetooth de GUID \_          | [**\_Informações do \_ evento BTH L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Essa mensagem é enviada quando um canal L2CAP entre o rádio local e um dispositivo Bluetooth remoto foi estabelecido ou encerrado. Para canais L2CAP que são multiplexadores, como RFCOMM, essa mensagem é enviada somente quando o canal subjacente é estabelecido, não quando cada canal multiplexado, como um canal de RFCOMM, é estabelecido ou encerrado. |
| \_solicitação de \_ PIN de Bluetooth de GUID \_          | Não aplicável.                                         | Essa mensagem deve ser ignorada pelo aplicativo. Se o aplicativo precisar receber solicitações de PIN, a função [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) deverá ser usada.                                                                                                                                                   |
| \_rádio Bluetooth \_ \_ de GUID no \_ intervalo      | [**\_rádio BTH \_ no \_ intervalo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Essa mensagem é enviada quando qualquer um dos seguintes atributos de um dispositivo Bluetooth remoto foi alterado: o dispositivo foi descoberto, a classe de dispositivo, o nome, o estado conectado ou o estado memorizado do dispositivo. Essa mensagem também é enviada quando esses atributos são definidos ou apagados.                                                                                  |
| \_rádio Bluetooth \_ \_ de GUID fora \_ do \_ intervalo | [**\_endereço Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Essa mensagem é enviada quando um dispositivo descoberto anteriormente não foi encontrado após a conclusão da última consulta. Esta mensagem não será enviada para dispositivos lembrados. A estrutura de **\_ endereço BTH** é o endereço do dispositivo que não foi encontrado.                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[**\_endereço Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**\_informações do \_ evento BTH HCI \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**\_Informações do \_ evento BTH L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**\_rádio BTH \_ no \_ intervalo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**\_identificador de difusão de dev \_**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**DEVICECHANGE do WM \_**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 