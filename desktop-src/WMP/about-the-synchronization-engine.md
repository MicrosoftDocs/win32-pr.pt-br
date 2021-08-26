---
title: Sobre o Mecanismo de Sincronização
description: Sobre o Mecanismo de Sincronização
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, mecanismo de sincronização
- Windows Media Player de objeto, mecanismo de sincronização
- modelo de objeto, mecanismo de sincronização
- Windows Media Player ActiveX controle, mecanismo de sincronização
- ActiveX controle, mecanismo de sincronização
- Windows Media Player Controle de ActiveX móvel, mecanismo de sincronização
- Windows Media Player Dispositivo móvel, mecanismo de sincronização
- sincronizando dispositivos, mecanismo de sincronização
- sincronização de dispositivo, mecanismo de sincronização
- mecanismo de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccac14f6416b080ae22407930d720df84bd5b4dc399892b9a2d8678d03eee6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903066"
---
# <a name="about-the-synchronization-engine"></a>Sobre o Mecanismo de Sincronização

O mecanismo de sincronização é o componente do Windows Media Player que gerencia a cópia de conteúdo de mídia digital para dispositivos portáteis. Windows Media Player dá suporte a uma única instância do mecanismo de sincronização para cada dispositivo. Você deve usar uma instância remota do controle Windows Media Player para executar tarefas de sincronização programaticamente. Na verdade, seu programa compartilha as instâncias do mecanismo de sincronização com Windows Media Player e todos os outros programas que usam as interfaces do Player para sincronização do dispositivo.

Você pode usar [IWMPSyncDevice::start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice::stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) para controlar quando o mecanismo de sincronização faz seu trabalho. Na maioria dos casos, você não deve usar esses métodos. Em vez disso, você deve permitir que o mecanismo de sincronização agende seu trabalho automaticamente. Os **métodos start** e **stop** existem para que você possa usá-los se o programa for projetado para substituir a interface do Windows Media Player usuário. Nesse caso, talvez você queira fornecer um botão iniciar/parar semelhante ao que Windows Media Player fornece na **guia Dispositivos.**

Você pode monitorar o progresso da sincronização de um dispositivo sondando [IWMPSyncDevice::get \_ progress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Esse método recupera um valor de progresso para todo o processo de sincronização com um dispositivo específico. O valor recuperado é um número que representa a porcentagem de sincronização concluída. Há dois eventos que você pode receber relacionados à sincronização. O **evento DeviceSyncError** notifica você quando ocorre um problema. O **evento DeviceSyncStateChange** alerta quando o mecanismo de sincronização mudou de estado para o dispositivo atual.

Você pode limitar a quantidade de armazenamento do dispositivo Windows Media Player para sincronização chamando [IWMPSyncDevice2::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) com o atributo **PercentSpaceReserved.** Usar essa interface requer Windows Media Player 11.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização de dispositivos**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Mostrando o progresso da sincronização**](showing-synchronization-progress.md)
</dt> </dl>

 

 




