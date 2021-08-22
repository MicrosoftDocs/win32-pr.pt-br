---
title: Bluetooth Estruturas
description: Esta seção fornece definições para estruturas usadas para gerenciar Bluetooth dispositivos e serviços.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, referência, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a2208902360b4f1161f9586e41f59f062972efbbba7eeb0cfb8ffbbc3c6b3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588276"
---
# <a name="bluetooth-structures"></a>Bluetooth Estruturas

Esta seção fornece definições para estruturas usadas para gerenciar Bluetooth dispositivos e serviços.

Bluetooth também tem suporte usando a interface de programação Windows Sockets. Para obter mais informações sobre Bluetooth usando a interface Windows Sockets, consulte [Suporte Windows soquetes para Bluetooth](windows-sockets-support-for-bluetooth.md).



| Seção                                                                                       | Conteúdo                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**ENDEREÇO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Contém o endereço de um Bluetooth dispositivo.                                                                                      |
| [**PARAMS DE RETORNO DE CHAMADA BLUETOOTH \_ \_ \_ AUTHENTICATE**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Contém informações de configuração específicas sobre o dispositivo Bluetooth respondendo a uma solicitação de autenticação.                  |
| [**RESPOSTA \_ BLUETOOTH \_ AUTHENTICATE**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contém informações passadas em resposta a um evento BTH \_ REMOTE \_ AUTHENTICATE \_ REQUEST.                                           |
| [**PARES DE CÓDIGO BLUETOOTH \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Fornece especificação e recuperação de informações Bluetooth COD (Classe de Dispositivo).                                         |
| [**INFORMAÇÕES \_ DO DISPOSITIVO \_ BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Fornece informações sobre um Bluetooth dispositivo.                                                                                   |
| [**\_PARAMS DE PESQUISA DE \_ \_ DISPOSITIVO BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Especifica critérios de pesquisa para Bluetooth pesquisa de dispositivo.                                                                         |
| [**BLUETOOTH \_ FIND \_ RADIO \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Facilita a enumeração de rádios Bluetooth instalados.                                                                       |
| [**INFORMAÇÕES \_ DE SERVIÇO LOCAL \_ \_ DO BLUETOOTH**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Contém informações de serviço local para uma Bluetooth rádio.                                                                        |
| [**INFORMAÇÕES \_ DE COMPARAÇÃO NUMÉRICA \_ \_ DE BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contém o valor numérico usado para autenticação por meio de comparação numérica.                                                       |
| [**INFORMAÇÕES \_ DE DADOS OOB \_ \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contém dados usados para autenticar antes de estabelecer um emparelhamento de dispositivo fora de banda.                                          |
| [**INFORMAÇÕES \_ DE SENHA \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contém a chave de acesso usada para autenticação por meio da chave de acesso.                                                                        |
| [**INFORMAÇÕES \_ DE PIN DO BLUETOOTH \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contém informações usadas para autenticação por meio do PIN.                                                                            |
| [**INFORMAÇÕES \_ DE RÁDIO \_ BLUETOOTH**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Contém informações sobre uma Bluetooth rádio.                                                                                    |
| [**BLUETOOTH \_ SELECT \_ DEVICE \_ PARAMS**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Facilita e gerencia a visibilidade, a autenticação e a seleção de Bluetooth e serviços.                         |
| [**INFORMAÇÕES DO \_ DISPOSITIVO \_ BTH**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Armazena informações sobre um Bluetooth dispositivo.                                                                                     |
| [**INFORMAÇÕES DE \_ EVENTO DO BTH HCI \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Usado em conexão com a obtenção de mensagens WM \_ DEVICECHANGE para Bluetooth.                                                       |
| [**INFORMAÇÕES DE \_ EVENTO BTH L2CAP \_ \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contém dados sobre os eventos associados a um canal L2CAP.                                                        |
| [**DISPOSITIVO DE \_ CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Usado ao consultar a presença de um Bluetooth dispositivo.                                                                       |
| [**SERVIÇO \_ DE CONSULTA \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Usado para consultar um Bluetooth serviço.                                                                                               |
| [**RÁDIO \_ BTH \_ NO \_ INTERVALO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Armazena dados sobre os dispositivos Bluetooth que estão dentro do intervalo de comunicação.                                                     |
| [**BTH \_ SET \_ SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Fornece informações de serviço para o serviço Bluetooth especificado.                                                                |
| [**DADOS DO ELEMENTO SDP \_ \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Armazena dados de elemento SDP.                                                                                                         |
| [**DADOS DE TIPO \_ DE CADEIA \_ DE \_ CARACTERES SDP**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Armazena informações sobre tipos de cadeia de caracteres SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Usado em uma Bluetooth consulta para restringir o conjunto de atributos a retornar na consulta.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Facilita a pesquisa de UUIDs.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contém o UUID no qual executar uma consulta SDP. Usado em conjunto com a [**estrutura SdpQueryUuid.**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Usado em conjunto com Bluetooth soquete conforme definido pela família de \_ endereços AF BTH.                                   |



 

 

 




