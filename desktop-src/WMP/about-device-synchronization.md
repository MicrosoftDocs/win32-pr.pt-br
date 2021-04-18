---
title: Sobre a sincronização do dispositivo
description: Sobre a sincronização do dispositivo
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizando dispositivos
- Modelo de objeto do Windows Media Player, sincronizando dispositivos
- modelo de objeto, sincronizando dispositivos
- Controle ActiveX do Windows Media Player, sincronizando dispositivos
- Controle ActiveX, sincronizando dispositivos
- Controle ActiveX móvel do Windows Media Player, sincronizando dispositivos
- Windows Media Player Mobile, sincronizando dispositivos
- Sincronizando dispositivos, sobre
- sincronização de dispositivo, sobre
- Sincronizando dispositivos, transferência manual
- sincronização de dispositivo, transferência manual
- Sincronizando dispositivos, sincronização automática
- sincronização de dispositivo, sincronização automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783642"
---
# <a name="about-device-synchronization"></a>Sobre a sincronização do dispositivo

O Windows Media Player 10 introduziu um novo modelo de sincronização de conteúdo de mídia digital com dispositivos portáteis. Da perspectiva do usuário, isso significa que você pode especificar quais listas de reprodução (incluindo listas de reprodução automáticas) são sincronizadas automaticamente com dispositivos. Você também pode transferir manualmente o conteúdo de mídia digital para dispositivos. Da perspectiva do desenvolvedor, isso significa que há uma nova funcionalidade exposta que você pode aproveitar em seus aplicativos. Para fazer isso, você deve criar uma instância remota do controle do Windows Media Player.

Há duas maneiras pelas quais um usuário pode copiar conteúdo de mídia digital para um dispositivo:

-   **Transferência manual.** O usuário seleciona o conteúdo de mídia digital na biblioteca e, em seguida, inicia uma transferência do conteúdo para o dispositivo. Isso é semelhante à funcionalidade fornecida pelas versões anteriores do Windows Media Player. O SDK do Windows Media Player não fornece métodos para transferir mídia digital para um dispositivo.
-   **Sincronização automática.** O usuário especifica as listas de reprodução que sincronizam automaticamente com o dispositivo. Esse é um recurso do Windows Media Player 10 ou posterior. O SDK do Windows Media Player fornece a funcionalidade para gerenciar a sincronização automática. Essa funcionalidade foi projetada para permitir que você crie uma interface do usuário personalizada para que seu aplicativo especifique como a sincronização do dispositivo ocorre e forneça informações de status aos usuários.

Para que a sincronização automática funcione, uma relação especial deve ser estabelecida entre o Windows Media Player e o dispositivo. Essa relação é chamada de *parceria*.

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

 

 




