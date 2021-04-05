---
title: Estabelecer comunicação remota do controle do Windows Media Player
description: Estabelecer comunicação remota do controle do Windows Media Player
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Windows Media Player, controle ActiveX remoto
- Modelo de objeto do Windows Media Player, controle ActiveX remoto
- modelo de objeto, controle de ActiveX remoto
- Windows Media Player Mobile, controle remoto de comunicação remota
- Controle ActiveX do Windows Media Player, comunicação remota
- Controle de ActiveX móvel do Windows Media Player, comunicação remota
- Controle ActiveX, comunicação remota
- controle ActiveX do Windows Media Player de comunicação remota
- incorporação, controle ActiveX remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615d3d31535abea098939af65ea67c13acbf8f6c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007239"
---
# <a name="remoting-the-windows-media-player-control"></a>Estabelecer comunicação remota do controle do Windows Media Player

Ao inserir o controle do Windows Media Player em um programa C++, você pode usá-lo como uma extensão remota do modo completo do Player. Isso é chamado de "comunicação remota" do controle do Windows Media Player e permite que você forneça todos os recursos do player de modo completo sem implementá-los por conta própria.

Quando você remota o controle, ele compartilha o mesmo mecanismo de reprodução que o modo completo do Player e os usuários podem alternar entre o modo incorporado (o estado "encaixado") e o modo completo (o estado "desencaixado") enquanto a reprodução de mídia digital continua sem interrupção.

## <a name="enabling-remote-embedding"></a>Habilitando a inserção remota

Para habilitar a inserção remota do controle do Windows Media Player, o programa deve implementar as interfaces **IServiceProvider** e [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) . **IServiceProvider** é uma interface de Component Object Model padrão (com) com um único método chamado **QueryService**. O Windows Media Player chama esse método para recuperar um ponteiro para uma interface **IWMPRemoteMediaServices** .

O **IWMPRemoteMediaServices** tem vários métodos, mas apenas dois deles são diretamente relevantes para a comunicação remota. Em [getApplicationName](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname), você retorna o nome do programa, que o Windows Media Player adiciona à lista **alternar para outro programa** no menu **Exibir** . Em [Getservicetype](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype), você indica o modo de inserção do controle retornando um valor de "Remote" ou "local". Se uma conexão remota for estabelecida com êxito, o método [Get \_ IsRemote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote) da interface [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4) retornará true.

## <a name="specifying-an-exclusive-online-store"></a>Especificando um repositório online exclusivo

Com o Windows Media Player 11, um aplicativo que incorpora o controle Player remotamente pode especificar um repositório online exclusivo. Nesse caso, o seletor de serviço no Windows Media Player é desabilitado e somente o repositório online especificado está disponível para o usuário. Para obter informações detalhadas sobre como especificar um repositório online exclusivo, consulte [repositórios online exclusivos](exclusive-online-stores.md).

## <a name="docking-and-undocking"></a>Encaixe e desencaixe

A interface **IWMPPlayer4** também fornece acesso à interface [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication) por meio do método [Get \_ playerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication) . Use **IWMPPlayerApplication** para alternar entre os Estados encaixados e desencaixados e para determinar o estado atual encaixado e o local da exibição de vídeo ou visualização.

O método [IWMPPlayerApplication:: switchToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication) desencaixa o controle abrindo o modo completo do Windows Media Player e transferindo a exibição de vídeo ou visualização para o painel **agora em execução** . O método [IWMPPlayerApplication:: switchToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol) encaixa o controle transferindo a exibição de vídeo ou visualização para o seu programa e fechando o modo completo do Player, se ele estiver aberto. O controle também pode ser encaixado selecionando um programa na lista **alternar para outro programa** ou fechando o modo completo do Player. Em ambos os casos, qualquer mídia digital que estiver sendo executada continuará sem interrupção.

## <a name="transferring-the-video-or-visualization-display"></a>Transferindo a exibição de vídeo ou visualização

Quando vários programas com controles do Windows Media Player incorporados e remotos são executados simultaneamente, todos os controles compartilham o mesmo mecanismo de reprodução. Eles também compartilham a mesma instância do modo completo do Player no estado desencaixado. No entanto, no estado encaixado, apenas um controle pode exibir o vídeo ou a visualização. No estado desencaixado, somente o modo completo do Player exibe o vídeo ou a visualização. O método **switchToControl** funciona nos Estados encaixados e desencaixados e transferirá a exibição de vídeo ou visualização para qualquer programa que o chame.

A única diferença entre os Estados encaixados e desencaixados é a presença do modo completo do Windows Media Player e sua propriedade da exibição de vídeo ou visualização. No estado desencaixado, todos os controles incorporados e remotos em execução no momento ainda estão visíveis e suas interfaces de usuário ainda estão totalmente funcionais. No entanto, se houver uma janela de vídeo ou visualização, ela estará vazia. No estado encaixado, apenas um dos controles incorporados e remotos possui a exibição, mas todas as interfaces do usuário continuam a funcionar.

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>Ocultando ou alterando o controle no estado desencaixado

Você deve fornecer sua própria implementação se quiser ocultar ou alterar a interface do usuário de um controle inserido no estado desencaixado ou quando o programa não possuir a exibição. Você pode fazer essas alterações ao encaixar e desencaixar o controle ou pode fazê-los em resposta aos eventos do Windows Media Player. Como o player pode ser encaixado na opção de menu **alternar para outro programa** , no entanto, geralmente é melhor fornecer essa funcionalidade em resposta a eventos.

Você pode implementar manipuladores de eventos para os eventos [SwitchedToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) e [SwitchedToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) , ou você pode implementar um único manipulador de eventos para o evento [PlayerDockedStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) . No último caso, você pode determinar o estado encaixado chamando [IWMPPlayerApplication:: get \_ playerDocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked). Em ambos os casos, use [IWMPPlayerApplication:: get \_ hasDisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) para determinar se o programa possui a exibição de vídeo ou visualização.

## <a name="re-establishing-a-remote-connection"></a>Restabelecendo uma conexão remota

Em determinadas circunstâncias, a conexão entre um controle remoto incorporado e o Player autônomo falhará, invalidando seus ponteiros para as interfaces do Windows Media Player. O Windows Media Player tentará se reconectar automaticamente e acionará o evento [PlayerReconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) para sinalizar essa tentativa. Embora a reconexão seja automática, você deve fornecer um manipulador de eventos para esse evento se desejar liberar seus ponteiros inválidos e recuperar novos para poder acessar o Player autônomo por meio da nova conexão.

## <a name="controlling-the-undocked-player"></a>Controlando o Player desencaixado

Todas as instâncias remotas do controle do Windows Media Player podem manipular o modo completo do Player, independentemente do estado encaixado. Os recursos que não têm nenhuma relevância para o modo completo do Player, no entanto, são ignorados até que o controle do Windows Media Player seja encaixado. Isso inclui propriedades de [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) e interfaces derivadas, como **Enabled**, **enableContextMenu**, **UIMODE** e **windowlessVideo**.

## <a name="error-dialog-boxes"></a>Caixas de diálogo de erro

Em uma instância remota de controle do Windows Media Player, as *configurações*. a propriedade **enableErrorDialogs** se comporta de maneira específica. As seguintes regras se aplicam:

-   Quando o Windows Media Player está desencaixado (a interface do usuário do Windows Media Player está visível), a propriedade **enableErrorDialogs** é ignorada e as caixas de diálogo de erro são tratadas pelo Player.
-   Quando o Windows Media Player é encaixado, o valor especificado por cada instância remota do controle para **enableErrorDialogs** aplica-se somente à instância de controle individual. Ou seja, se uma determinada instância de controle especificar um valor de "true" para **enableErrorDialogs**, somente essa instância exibirá uma caixa de diálogo quando ocorrer um erro se todas as outras instâncias do controle tiverem especificado um valor de "false".

## <a name="remoting-in-the-background"></a>Comunicação remota em segundo plano

Você deve evitar manter uma instância remota do Player em execução em segundo plano durante os horários em que o controle não está em uso. Como a instância de controle do Player remoto compartilha seu mecanismo de reprodução com o player de modo completo, manter uma instância em segundo plano em execução pode causar um comportamento inesperado. Por exemplo, o usuário pode fechar o player de modo completo enquanto um arquivo está sendo reproduzido. O usuário esperaria que a reprodução do arquivo fosse interrompida completamente quando o jogador fechar, mas o áudio pode continuar a reproduzir porque o mecanismo de reprodução ainda está ativo.

## <a name="samples"></a>Exemplos

O pacote de instalação do SDK do Windows Media Player instala exemplos que demonstram comunicação remota. Consulte os exemplos de RemoteSkin e WMPML para obter mais informações.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em um programa C++**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




