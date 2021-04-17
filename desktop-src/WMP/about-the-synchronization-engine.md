---
title: Sobre o mecanismo de sincronização
description: Sobre o mecanismo de sincronização
ms.assetid: bb57ffb0-3833-463b-b66c-c23224fa2ba7
keywords:
- Windows Media Player, mecanismo de sincronização
- Modelo de objeto do Windows Media Player, mecanismo de sincronização
- modelo de objeto, mecanismo de sincronização
- Controle ActiveX do Windows Media Player, mecanismo de sincronização
- Controle ActiveX, mecanismo de sincronização
- Controle ActiveX móvel do Windows Media Player, mecanismo de sincronização
- Windows Media Player Mobile, mecanismo de sincronização
- Sincronizando dispositivos, mecanismo de sincronização
- sincronização de dispositivo, mecanismo de sincronização
- mecanismo de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe0768c4805b074fdaf628a25daf47b9ced97ee
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365591"
---
# <a name="about-the-synchronization-engine"></a>Sobre o mecanismo de sincronização

O mecanismo de sincronização é o componente do Windows Media Player que gerencia a cópia de conteúdo de mídia digital para dispositivos portáteis. O Windows Media Player dá suporte a uma única instância do mecanismo de sincronização para cada dispositivo. Você deve usar uma instância remota do controle do Windows Media Player para executar tarefas de sincronização programaticamente. Na verdade, o programa compartilha as instâncias do mecanismo de sincronização com o Windows Media Player e todos os outros programas que usam as interfaces do Player para a sincronização do dispositivo.

Você pode usar [IWMPSyncDevice:: Start](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-start) e [IWMPSyncDevice:: Stop](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-stop) para controlar quando o mecanismo de sincronização faz seu trabalho. Na maioria dos casos, você não deve usar esses métodos. Em vez disso, você deve deixar o mecanismo de sincronização agendar seu trabalho automaticamente. Os métodos **Start** e **Stop** existem para que você possa usá-los se o programa for projetado para substituir a interface do usuário do Windows Media Player. Nesse caso, talvez você queira fornecer um botão iniciar/parar semelhante ao fornecido pelo Windows Media Player na guia **dispositivos** .

Você pode monitorar o progresso da sincronização de um dispositivo ao sondar [IWMPSyncDevice:: obter \_ progresso](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress). Esse método recupera um valor de progresso para todo o processo de sincronização com um dispositivo específico. O valor recuperado é um número que representa a porcentagem de sincronização concluída. Há dois eventos que você pode receber relacionados à sincronização. O evento **DeviceSyncError** notifica quando ocorre um problema. O evento **DeviceSyncStateChange** alertará quando o estado do mecanismo de sincronização for alterado para o dispositivo atual.

Você pode limitar a quantidade de armazenamento de dispositivo que o Windows Media Player usa para sincronização chamando [IWMPSyncDevice2:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo) com o atributo **PercentSpaceReserved** . O uso desta interface requer o Windows Media Player 11.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização do dispositivo**](about-device-synchronization.md)
</dt> <dt>

[**Interface IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Mostrando o progresso da sincronização**](showing-synchronization-progress.md)
</dt> </dl>

 

 




