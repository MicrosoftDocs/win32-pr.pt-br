---
title: Sobre parcerias
description: Sobre parcerias
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, parcerias
- Windows Media Player modelo de objeto, parcerias
- modelo de objeto, parcerias
- Windows Media Player ActiveX controle, parcerias
- ActiveX, parcerias
- Windows Media Player Controle de ActiveX móvel, parcerias
- Windows Media Player Mobile,partnerships
- sincronizando dispositivos, parcerias
- sincronização de dispositivos, parcerias
- parcerias entre dispositivos e Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c018934ed06e5872d5866a463bdd909ea2501a1872ded29231be222572b2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004486"
---
# <a name="about-partnerships"></a>Sobre parcerias

Uma parceria é uma relação especial entre um dispositivo portátil e Windows Media Player. Os usuários podem estabelecer uma parceria para um dispositivo específico usando a Windows Media Player do usuário. Você pode gerenciar programaticamente parcerias usando [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) e [IWMPSyncDevice::d eletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). O **método createPartnership** inicia um processo assíncrono que termina quando o evento **CreatePartnershipComplete** é recebido por meio da interface **IWMPEvents2.**

Windows Media Player 10 ou posterior dá suporte à criação de parcerias com até 16 dispositivos. Cada parceria tem um índice de parceria associado. Você pode recuperar o índice de parceria para um dispositivo específico chamando [IWMPSyncDevice::get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Índices de parceria são numerados de 1 a 16. Quando um dispositivo específico não tem uma parceria com Windows Media Player, **getPartnershipIndex retorna** zero para o índice.

Você pode recuperar o status da parceria de um dispositivo específico chamando [IWMPSyncDevice::get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) e inspecionando o [valor WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) recuperado. Windows Media Player permite uma parceria com a biblioteca de um usuário em um computador para cada dispositivo. Isso significa que a criação de uma nova parceria destrói qualquer parceria existente que o dispositivo atual possa ter com outro computador. Para saber quando o status muda para um dispositivo, você pode receber o **evento DeviceStatusChange.**

Windows Media Player pode criar uma parceria com um dispositivo com o status **wmpdsManualDevice**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




