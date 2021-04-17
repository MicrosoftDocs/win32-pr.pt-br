---
title: Sobre parcerias
description: Sobre parcerias
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, parcerias
- Modelo de objeto do Windows Media Player, parcerias
- modelo de objeto, parcerias
- Controle ActiveX do Windows Media Player, parcerias
- Controle ActiveX, parcerias
- Controle ActiveX móvel do Windows Media Player, parcerias
- Windows Media Player Mobile, parcerias
- Sincronizando dispositivos, parcerias
- sincronização de dispositivo, parcerias
- parcerias entre dispositivos e o Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104453846"
---
# <a name="about-partnerships"></a>Sobre parcerias

Uma parceria é uma relação especial entre um dispositivo portátil e o Windows Media Player. Os usuários podem estabelecer uma parceria para um dispositivo específico usando a interface do usuário do Windows Media Player. Você pode gerenciar parcerias programaticamente usando [IWMPSyncDevice:: Createpartnere](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). O método **Createpartnership** inicia um processo assíncrono que termina quando o evento **CreatePartnershipComplete** é recebido por meio da interface **IWMPEvents2** .

O Windows Media Player 10 ou posterior dá suporte à criação de parcerias com até 16 dispositivos. Cada parceria tem um índice de parceria associado. Você pode recuperar o índice de parceria para um dispositivo específico chamando [IWMPSyncDevice:: get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Os índices de parceria são numerados de 1 a 16. Quando um dispositivo específico não tem uma parceria com o Windows Media Player, **getPartnershipIndex** retorna zero para o índice.

Você pode recuperar o status de parceria de um determinado dispositivo chamando [IWMPSyncDevice:: get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e, em seguida, inspecionando o valor de [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. O Windows Media Player permite que uma parceria com a biblioteca de um usuário em um computador para cada dispositivo. Isso significa que a criação de uma nova parceria destrói qualquer parceria existente que o dispositivo atual pode ter com outro computador. Para saber quando o status é alterado para um dispositivo, você pode receber o evento **DeviceStatusChange** .

O Windows Media Player não pode criar uma parceria com um dispositivo com o status **wmpdsManualDevice**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização do dispositivo**](about-device-synchronization.md)
</dt> <dt>

[**Interface IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




