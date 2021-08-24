---
title: Bluetooth Funções
description: as funções nesta seção são usadas para gerenciar Bluetooth dispositivos e serviços.
ms.assetid: 5cd4a050-51f3-40f4-b434-be639e109f0f
keywords:
- Bluetooth, referência, funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e8d945355b0bc25df4d91a96c30a4d20491eb3b0e86c3542e30c0f2b470833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701406"
---
# <a name="bluetooth-functions"></a>Bluetooth Funções

as funções nesta seção são usadas para gerenciar Bluetooth dispositivos e serviços.

também há suporte para Bluetooth usando a interface de programação de soquetes de Windows. para obter mais informações sobre Bluetooth de programação usando a interface Windows sockets, consulte [suporte a Windows sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).



| Seção                                                                                | Conteúdo                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BluetoothAuthenticateDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedevice)                     | envia uma solicitação de autenticação para um dispositivo de Bluetooth remoto.                                                                                                                                 |
| [**BluetoothAuthenticateDeviceEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatedeviceex)                 | envia uma solicitação de autenticação para um dispositivo de Bluetooth remoto. Além disso, essa função permite que dados fora de banda sejam passados para a chamada de função para o dispositivo que está sendo autenticado. |
| [**BluetoothAuthenticateMultipleDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothauthenticatemultipledevices)   | permite que o chamador solicite a autenticação de vários dispositivos durante uma única instância do assistente de conexão de Bluetooth.                                                            |
| [**BluetoothDisplayDeviceProperties**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothdisplaydeviceproperties)           | Invoca a folha de propriedades informações do dispositivo do painel de controle.                                                                                                                                  |
| [**BluetoothEnableDiscovery**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenablediscovery)                           | altera o estado de descoberta de um rádio local Bluetooth ou rádios.                                                                                                                             |
| [**BluetoothEnableIncomingConnections**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenableincomingconnections)       | modifica se um rádio Bluetooth local aceita conexões de entrada.                                                                                                                        |
| [**BluetoothEnumerateInstalledServices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothenumerateinstalledservices)     | enumera os guids (identificadores globalmente exclusivos) dos serviços que estão habilitados em um dispositivo Bluetooth.                                                                                    |
| [**BluetoothFindDeviceClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfinddeviceclose)                           | Fecha um identificador de enumeração associado a uma consulta de dispositivo.                                                                                                                          |
| [**BluetoothFindFirstDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstdevice)                           | inicia a enumeração de dispositivos Bluetooth locais.                                                                                                                                            |
| [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)                             | inicia a enumeração de rádios de Bluetooth local.                                                                                                                                             |
| [**BluetoothFindNextDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextdevice)                             | localiza o próximo dispositivo Bluetooth.                                                                                                                                                              |
| [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)                               | localiza o próximo Bluetooth rádio.                                                                                                                                                               |
| [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)                             | fecha o identificador de enumeração que está associado à localização de Bluetooth rádios.                                                                                                               |
| [**BluetoothGetDeviceInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetdeviceinfo)                               | recupera informações sobre um dispositivo de Bluetooth remoto. o dispositivo Bluetooth deve ter sido identificado anteriormente por meio de uma chamada de função de consulta de dispositivo bem-sucedida.                           |
| [**BluetoothGetRadioInfo**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothgetradioinfo)                                 | obtém informações sobre um Bluetooth rádio.                                                                                                                                                  |
| [**BluetoothIsConnectable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisconnectable)                               | determina se um Bluetooth rádio ou rádios é conectável.                                                                                                                                |
| [**BluetoothIsDiscoverable**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothisdiscoverable)                             | determina se um Bluetooth rádio ou rádio é detectável.                                                                                                                               |
| [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication)       | registra uma função de chamada de retorno que é chamada quando um determinado dispositivo de Bluetooth solicita autenticação.                                                                                      |
| [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex)   | Registra um aplicativo para uma solicitação de PIN, comparação numérica e função de retorno de chamada.                                                                                                         |
| [**BluetoothRemoveDevice**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothremovedevice)                                 | remove a autenticação entre um Bluetooth dispositivo e o computador, limpando todas as informações armazenadas em cache sobre o dispositivo.                                                                          |
| [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes)                       | Enumera por meio do fluxo de registro SDP e chama a função de retorno de chamada para cada atributo no registro.                                                                                    |
| [**BluetoothSdpGetAttributeValue**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetattributevalue)                 | Recupera o valor do atributo para um identificador de atributo.                                                                                                                                    |
| [**BluetoothSdpGetContainerElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetcontainerelementdata)     | Itera em um fluxo de contêiner e retorna cada elemento contido no elemento de contêiner.                                                                                     |
| [**BluetoothSdpGetElementData**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetelementdata)                       | Recupera e analisa um único elemento de um fluxo SDP.                                                                                                                                     |
| [**BluetoothSdpGetString**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpgetstring)                                 | Converte uma cadeia de caracteres bruta que é inserida no registro SDP em uma cadeia de caracteres Unicode.                                                                                                               |
| [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices)                               | habilita Bluetooth seleção de dispositivo.                                                                                                                                                           |
| [**BluetoothSelectDevicesFree**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevicesfree)                       | Libera recursos associados a uma chamada anterior à função [**BluetoothSelectDevices**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothselectdevices) .                                                                     |
| [**BluetoothSendAuthenticationResponse**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponse)     | Chamado quando uma solicitação de autenticação para enviar a resposta de chave de acesso é recebida.                                                                                                               |
| [**BluetoothSendAuthenticationResponseEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsendauthenticationresponseex) | Chamado quando uma solicitação de autenticação para enviar a chave de acesso ou a resposta de comparação numérica é recebida.                                                                                         |
| [**BluetoothSetLocalServiceInfo**](/previous-versions/windows/desktop/legacy/bb870603(v=vs.85))                   | define informações de serviço local para um rádio de Bluetooth específico.                                                                                                                                |
| [**BluetoothSetServiceState**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsetservicestate)                           | habilita ou desabilita serviços para um dispositivo Bluetooth.                                                                                                                                          |
| [**BluetoothUnregisterAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothunregisterauthentication)         | Remove o registro para uma rotina de retorno de chamada que foi registrada anteriormente com uma chamada para a função [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .      |
| [**BluetoothUpdateDeviceRecord**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothupdatedevicerecord)                     | atualiza o cache do computador local sobre um dispositivo Bluetooth.                                                                                                                                    |



 

 

 