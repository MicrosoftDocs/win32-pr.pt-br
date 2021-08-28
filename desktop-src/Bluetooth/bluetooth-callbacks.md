---
title: Retornos de chamada Bluetooth
description: As funções de retorno de chamada do Bluetooth nesta seção são usadas em combinação com funções que possibilitam o gerenciamento de dispositivos e serviços Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad822a0c7af4b0bbc5d649919bda638776014dfe7e8195ed1f45bb99032c6d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588356"
---
# <a name="bluetooth-callbacks"></a>Retornos de chamada Bluetooth

As funções de retorno de chamada do Bluetooth nesta seção são usadas em combinação com funções que possibilitam o gerenciamento de dispositivos e serviços Bluetooth.

O Bluetooth também tem suporte usando a interface de programação do Windows Sockets. Para obter mais informações sobre como programar o Bluetooth usando a interface do Windows Sockets, consulte [suporte do Windows Sockets para Bluetooth](windows-sockets-support-for-bluetooth.md).



| Seção                                                                                      | Conteúdo                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**retorno de chamada de \_ autenticação PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | Usado em conjunto com a função [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .                                                  |
| [**\_retorno de chamada de autenticação PFN \_ \_ ex**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | Usado em conjunto com a função [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .                                              |
| [**\_retorno de \_ \_ chamada de atributos de enumeração Bluetooth PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | Chamado uma vez para cada atributo encontrado no parâmetro *pSDPStream* que é passado para a chamada de função [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) . |
| [**retorno de chamada do \_ dispositivo PFN \_**](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | Usado em associação com a seleção de dispositivos Bluetooth.                                                                                                                    |



 

 

 




