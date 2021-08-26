---
title: Sobre a sincronização do dispositivo
description: Sobre a sincronização do dispositivo
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizando dispositivos
- modelo de objeto Windows Media Player, sincronizando dispositivos
- modelo de objeto, sincronizando dispositivos
- Windows Media Player controle de ActiveX, sincronizando dispositivos
- controle de ActiveX, sincronizando dispositivos
- Windows Media Player controle de ActiveX móvel, sincronizando dispositivos
- Windows Media Player Dispositivos móveis, sincronizando
- Sincronizando dispositivos, sobre
- sincronização de dispositivo, sobre
- Sincronizando dispositivos, transferência manual
- sincronização de dispositivo, transferência manual
- Sincronizando dispositivos, sincronização automática
- sincronização de dispositivo, sincronização automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6a03781121a58bee36fd9ff1f74bf21a85347f81384f30c2db5afb4ef3e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903555"
---
# <a name="about-device-synchronization"></a>Sobre a sincronização do dispositivo

o Windows Media Player 10 introduziu um novo modelo para sincronizar o conteúdo de mídia digital com dispositivos portáteis. Da perspectiva do usuário, isso significa que você pode especificar quais listas de reprodução (incluindo listas de reprodução automáticas) são sincronizadas automaticamente com dispositivos. Você também pode transferir manualmente o conteúdo de mídia digital para dispositivos. Da perspectiva do desenvolvedor, isso significa que há uma nova funcionalidade exposta que você pode aproveitar em seus aplicativos. para fazer isso, você deve criar uma instância remota do controle de Windows Media Player.

Há duas maneiras pelas quais um usuário pode copiar conteúdo de mídia digital para um dispositivo:

-   **Transferência manual.** O usuário seleciona o conteúdo de mídia digital na biblioteca e, em seguida, inicia uma transferência do conteúdo para o dispositivo. Isso é semelhante à funcionalidade fornecida pelas versões anteriores do Windows Media Player. o SDK do Windows Media Player não fornece métodos para transferir mídia digital para um dispositivo.
-   **Sincronização automática.** O usuário especifica as listas de reprodução que sincronizam automaticamente com o dispositivo. esse é um recurso do Windows Media Player 10 ou posterior. o SDK do Windows Media Player fornece funcionalidade para gerenciar a sincronização automática. Essa funcionalidade foi projetada para permitir que você crie uma interface do usuário personalizada para que seu aplicativo especifique como a sincronização do dispositivo ocorre e forneça informações de status aos usuários.

para que a sincronização automática funcione, uma relação especial deve ser estabelecida entre Windows Media Player e o dispositivo. Essa relação é chamada de *parceria*.

As seções a seguir fornecem mais informações sobre a sincronização de dispositivos.

-   [Sobre dispositivos](about-devices.md)
-   [Sobre parcerias](about-partnerships.md)
-   [Sobre o mecanismo de sincronização](about-the-synchronization-engine.md)
-   [Sobre a sincronização de playlist](about-playlist-synchronization.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> <dt>

[**Estabelecer comunicação remota do controle do Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




