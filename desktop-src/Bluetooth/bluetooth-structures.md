---
title: Estruturas Bluetooth
description: Esta seção fornece definições para estruturas usadas para gerenciar dispositivos e serviços Bluetooth.
ms.assetid: bab27f5c-04c1-4fdc-91ff-249d1bfaef24
keywords:
- Bluetooth, referência, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7df10989e41814f6f750bdcc719f01b14ccae315
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822321"
---
# <a name="bluetooth-structures"></a>Estruturas Bluetooth

Esta seção fornece definições para estruturas usadas para gerenciar dispositivos e serviços Bluetooth.

O Bluetooth também tem suporte usando a interface de programação do Windows Sockets. Para obter mais informações sobre como programar o Bluetooth usando a interface do Windows Sockets, consulte [suporte do Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).



| Seção                                                                                       | Conteúdo                                                                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**\_endereço Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)                                               | Contém o endereço de um dispositivo Bluetooth.                                                                                      |
| [**\_parâmetros de \_ retorno de chamada de AUTENTICAr Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authentication_callback_params) | Contém informações de configuração específicas sobre o dispositivo Bluetooth respondendo a uma solicitação de autenticação.                  |
| [**\_resposta de autenticar Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_authenticate_response)                  | Contém informações passadas em resposta a um \_ evento de solicitação de autenticação remota BTH \_ \_ .                                           |
| [**\_pares Bluetooth c.o.d. \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_cod_pairs)                                          | Fornece a especificação e a recuperação da classe Bluetooth de informações do dispositivo (COD).                                         |
| [**\_informações do dispositivo Bluetooth \_**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_device_info_struct)                                      | Fornece informações sobre um dispositivo Bluetooth.                                                                                   |
| [**\_parâmetros de \_ pesquisa de dispositivo Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_device_search_params)                   | Especifica critérios de pesquisa para pesquisas de dispositivo Bluetooth.                                                                         |
| [**\_parâmetros de \_ rádio de localização de Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_find_radio_params)                         | Facilita a enumeração de rádios Bluetooth instalados.                                                                       |
| [**\_informações do \_ serviço \_ local Bluetooth**](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_local_service_info_struct)                       | Contém informações de serviço local para um rádio Bluetooth.                                                                        |
| [**\_informações de \_ comparação \_ numérica do Bluetooth**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_numeric_comparison_info)             | Contém o valor numérico usado para autenticação por meio de comparação numérica.                                                       |
| [**\_informações de \_ dados de OOB do Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_oob_data_info)                                 | Contém os dados usados para autenticação antes de estabelecer um emparelhamento de dispositivo fora de banda.                                          |
| [**\_informações de chave de acesso Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_passkey_info)                                    | Contém a chave de acesso usada para autenticação via chave de acesso.                                                                        |
| [**\_informações de PIN do Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_pin_info)                                            | Contém informações usadas para autenticação via PIN.                                                                            |
| [**\_informações de rádio Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_radio_info)                                        | Contém informações sobre um rádio Bluetooth.                                                                                    |
| [**\_parâmetros de seleção de \_ dispositivos Bluetooth \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-bluetooth_select_device_params)                   | Facilita e gerencia a visibilidade, a autenticação e a seleção de dispositivos e serviços Bluetooth.                         |
| [**\_informações do dispositivo BTH \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info)                                                  | Armazena informações sobre um dispositivo Bluetooth.                                                                                     |
| [**\_informações do \_ evento BTH HCI \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)                                           | Usado em conexão com a obtenção \_ de mensagens do WM DEVICECHANGE para Bluetooth.                                                       |
| [**\_Informações do \_ evento BTH L2CAP \_**](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)                                       | Contém dados sobre os eventos associados a um canal do L2CAP.                                                        |
| [**\_dispositivo de consulta BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)                                                | Usado ao consultar a presença de um dispositivo Bluetooth.                                                                       |
| [**\_serviço de consulta do BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)                                              | Usado para consultar um serviço Bluetooth.                                                                                               |
| [**\_rádio BTH \_ no \_ intervalo**](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)                                           | Armazena dados sobre os dispositivos Bluetooth que estão no intervalo de comunicação.                                                     |
| [**BTH \_ definir \_ serviço**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)                                                  | Fornece informações de serviço para o serviço Bluetooth especificado.                                                                |
| [**\_dados do elemento SDP \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_element_data)                                                | Armazena dados do elemento SDP.                                                                                                         |
| [**\_dados do \_ tipo cadeia de caracteres SDP \_**](/windows/desktop/api/BluetoothAPIs/ns-bluetoothapis-sdp_string_type_data)                                       | Armazena informações sobre tipos de cadeia de caracteres SDP.                                                                                       |
| [**SdpAttributeRange**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpattributerange)                                                | Usado em uma consulta de Bluetooth para restringir o conjunto de atributos a serem retornados na consulta.                                             |
| [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid)                                                          | Facilita a pesquisa de UUIDs.                                                                                                 |
| [**SdpQueryUuidUnion**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuidunion)                                                | Contém o UUID no qual executar uma consulta SDP. Usado em conjunto com a estrutura [**SdpQueryUuid**](/windows/desktop/api/Bthsdpdef/ns-bthsdpdef-sdpqueryuuid) . |
| [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)                                                         | Usado em conjunto com operações de soquete Bluetooth, conforme definido pela \_ família de endereços BTH de AF.                                   |



 

 

 




