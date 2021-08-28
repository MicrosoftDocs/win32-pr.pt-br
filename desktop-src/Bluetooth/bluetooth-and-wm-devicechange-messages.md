---
title: Bluetooth e WM_DEVICECHANGE mensagens
description: Bluetooth inclui mensagens específicas do WM DEVICECHANGE que permitem que os desenvolvedores obtenham mensagens quando Bluetooth \_ dispositivos passam por alterações de status.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b22c08c4243ce33f7d3146e96a3fcdd5c937b4781fd783918c148939ca0e22e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588406"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a>Bluetooth e MENSAGENS \_ WM DEVICECHANGE

Bluetooth inclui mensagens [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) específicas que permitem que os desenvolvedores obtenham mensagens quando Bluetooth dispositivos passam por alterações de status. Este tópico descreve como receber mensagens Bluetooth **WM \_ DEVICECHANGE** específicas e listas Bluetooth mensagens específicas.

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a>Recebendo Bluetooth mensagens WM \_ DEVICECHANGE específicas

Para receber [**mensagens WM \_ DEVICECHANGE,**](/windows/desktop/DevIO/wm-devicechange) um handle para a rádio local deve ser aberto primeiro. Para tal, use um dos seguintes métodos:

-   Use a função [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) com os seguintes parâmetros: \_ (GUID BTHPORT DEVICE INTERFACE, ..., DIGCF PRESENT DIGCF DEVICEINTERFACE) e, em seguida, use as funções \_ \_ \_ \| \_ [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)e [SetupDiDmineyDeviceInfoList.](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
-   Use as [**funções BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)e [**BluetoothFindRadioClose.**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)

Quando o Bluetooth de rádio for aberto, chame a função [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) e registre-se para notificações no handle usando **dBT \_ DEVTYP \_ HANDLE** como o tipo de dispositivo. Quando registrado, os GUIDs a seguir são enviados e o membro de dados [**DEV \_ BROADCAST \_ HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch \_** é o buffer associado.

## <a name="bluetooth-specific-messages"></a>Bluetooth mensagens específicas do Bluetooth

A tabela a seguir lista Bluetooth mensagens [**WM \_ DEVICECHANGE específicas.**](/windows/desktop/DevIO/wm-devicechange)

| GUID                                   | BUFFER                                                  | Descrição                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EVENTO GUID \_ BLUETOOTH \_ HCI \_            | [**INFORMAÇÕES DE \_ EVENTO DO BTH HCI \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | Essa mensagem é enviada quando um dispositivo Bluetooth remoto se conecta ou se desconecta no nível da ACL.                                                                                                                                                                                                                                                                    |
| EVENTO \_ GUID BLUETOOTH \_ \_ L2CAP          | [**INFORMAÇÕES DE \_ EVENTO BTH L2CAP \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | Essa mensagem é enviada quando um canal L2CAP entre a rádio local e um dispositivo Bluetooth remoto foi estabelecido ou encerrado. Para canais L2CAP que são multiplexadores, como RFCOMM, essa mensagem só é enviada quando o canal subjacente é estabelecido, não quando cada canal multiplexado, como um canal RFCOMM, é estabelecido ou encerrado. |
| SOLICITAÇÃO \_ DE PIN DE BLUETOOTH \_ \_ GUID          | Não aplicável.                                         | Essa mensagem deve ser ignorada pelo aplicativo. Se o aplicativo deve receber solicitações de PIN, [**a função BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) deve ser usada.                                                                                                                                                   |
| GUID \_ BLUETOOTH \_ RADIO \_ IN \_ RANGE      | [**RÁDIO \_ BTH \_ NO \_ INTERVALO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | Essa mensagem é enviada quando qualquer um dos seguintes atributos de um dispositivo Bluetooth remoto foi alterado: o dispositivo foi descoberto, a classe de dispositivo, o nome, o estado conectado ou o estado lembrado do dispositivo. Essa mensagem também é enviada quando esses atributos são definidos ou limpos.                                                                                  |
| GUID \_ BLUETOOTH \_ RADIO \_ OUT \_ OF \_ RANGE | [**ENDEREÇO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | Essa mensagem é enviada quando um dispositivo descoberto anteriormente não foi encontrado após a conclusão da última consulta. Essa mensagem não será enviada para dispositivos lembrados. A **estrutura \_ ENDEREÇO BTH** é o endereço do dispositivo que não foi encontrado.                                                                                                      |



 

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

[**ENDEREÇO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[**INFORMAÇÕES DE \_ EVENTO DO BTH HCI \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[**INFORMAÇÕES DE \_ EVENTO BTH L2CAP \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[**RÁDIO \_ BTH \_ NO \_ INTERVALO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[**DEV \_ BROADCAST \_ HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 