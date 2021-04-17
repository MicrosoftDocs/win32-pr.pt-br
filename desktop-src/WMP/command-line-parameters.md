---
title: Parâmetros de linha de comando
description: Parâmetros de linha de comando
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Windows Media Player, parâmetros
- Windows Media Player, parâmetros de linha de comando
- Windows Media Player, wmplayer
- Windows Media Player, WMPConfig
- Windows Media Player, wmpnscfg
- parâmetros de linha de comando
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa65b686f8a746111a62bd6afcc3df280191c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789572"
---
# <a name="command-line-parameters"></a>Parâmetros de linha de comando

## <a name="command-line-parameters-for-wmplayer"></a>Parâmetros de linha de comando para wmplayer

O Windows Media Player dá suporte a um conjunto de parâmetros de linha de comando que especificam como o jogador se comporta quando é iniciado. A tabela a seguir detalha os parâmetros e seus comportamentos.



| Syntax                                                                                                              | Comportamento                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*Path \\ filename*" (por exemplo: `wmplayer "c:\filename.wma"` )<br/>                                            | Inicie o Player e execute o arquivo.                                                                                                                                                                                                                                                                                                        |
| /fullscreen "*Path \\ filename*" (por exemplo: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Reproduzir o arquivo especificado no modo de tela inteira. Você deve especificar o caminho e o nome de arquivo do conteúdo a ser reproduzido.<br/>                                                                                                                                                                                                                     |
| /Device: {DVD \| AudioCD} (por exemplo: `wmplayer /device:audio CD` )<br/>                                         | Reproduzir um CD de áudio ou DVD.                                                                                                                                                                                                                                                                                                                    |
| "*caminho \\ nome do arquivo*? WMPSkin =*nome da capa*"por exemplo: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Abra o Player, aplicando a capa especificada.                                                                                                                                                                                                                                                                                              |
| /Service:*KeyName*                                                                                                  | Abra o Player mostrando a loja online especificada por *KeyName*. Requer o Windows Media Player 10 ou posterior.<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | Abra o Player no recurso de **agora em execução** .                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | Abra o Player no recurso de **Guia de mídia** (repositório online ativo atual no Windows Media Player 10 ou posterior).                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | Abra o Player no recurso **Copiar do CD** (recurso **RIP** no Windows Media Player 10 ou Windows Media Player 11). Não há suporte para esse parâmetro no Windows Media Player 12.                                                                                                                                                       |
| /Task CDWrite                                                                                                       | Abra o Player no recurso de **gravação** . Requer o Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | Abra o Player no recurso de **biblioteca** .                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | Abra o Player no recurso **sintonizador de rádio** (repositório online ativo atual no Windows Media Player 10 ou posterior).                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | Abra o Player no recurso **copiar para o CD ou dispositivo** (recurso de **sincronização** no Windows Media Player 10 ou posterior).                                                                                                                                                                                                                            |
| Serviços/Tasks */Service* ServiceName                                                                               | Abra o Player no recurso **Serviços Premium** , *mostrando o serviço especificado pelo parâmetro* ServiceName. Esse valor é o nome exclusivo para o serviço. Se o serviço especificado não tiver sido exibido anteriormente, o parâmetro *ServiceName* será ignorado. (Abre o repositório online especificado no Windows Media Player 10 ou posterior.) |
| /Task de tarefa *X*                                                                                                | Abra o Player no painel de tarefas do serviço de loja online especificado por *X*. Por exemplo,/Task ServiceTask1 abre o Player no primeiro painel de tarefas do serviço de loja online.                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | Abra o Player no recurso **seletor de capa** .                                                                                                                                                                                                                                                                                           |
| *Playlistname* de/playlist                                                                                            | Abra o Player e reproduza a lista de reprodução especificada.                                                                                                                                                                                                                                                                                           |
| /Schema: {música \| imagens \| vídeo \| \| outros} por exemplo: `wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Abra o Player, mostrando a categoria de mídia especificada. Requer o Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Parâmetros de linha de comando para WMPConfig

Wmpconfig.exe é usado para executar determinados comandos no Windows Media Player que exigem permissão de administrador. Os exemplos incluem o início e a interrupção dos serviços de navegação e compartilhamento e a habilitação de exceções no firewall do Windows. A tabela a seguir descreve os valores possíveis para os parâmetros de linha de comando.



| Syntax                                                                                    | Comportamento                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *Mac*                                                                    | Desabilita o dispositivo especificado por um identificador de controle de acesso à mídia (MAC).  |
| Exemplo de HMEOff:<br/> wmpconfig HMEOff<br/>                                    | Desabilita o serviço de compartilhamento de rede do Windows Media Player.                 |
| Exemplo de HMEOn:<br/> wmpconfig HMEOn<br/>                                      | Permite o compartilhamento, a navegação e a exceção de firewall.                     |
| RemoveHMEDevice *Mac*                                                                     | Remove o dispositivo especificado por um identificador de MAC.                          |
| RestoreHMEDevice *Mac*                                                                    | Restaura o dispositivo especificado por um identificador de MAC.                         |
| Exemplo de *nível* de SetDVDParentalLevel:<br/> WMPConfig SetDVDParentalLevel 3<br/> | Define o nível de controle dos pais do DVD. O nível é especificado como um inteiro. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Parâmetros de linha de comando para wmpnscfg

O Microsoft Windows usa wmpnscfg.exe para alertar os usuários quando dispositivos de renderização de mídia são encontrados na rede. O wmpnscfg inicia o serviço de compartilhamento de rede (NSS) do Windows Media Player e aguarda as notificações do serviço. Quando wmpnscfg é notificado de que um novo dispositivo de mídia está disponível na rede, ele exibe um pop-up na bandeja do sistema que informa o usuário sobre a disponibilidade do novo dispositivo. Se o usuário clicar no pop-up, o wmpnscfg iniciará o Windows Media Player, que exibe uma caixa de diálogo que solicita ao usuário para permitir ou negar o compartilhamento com o novo dispositivo.

Normalmente, o Windows chama wmpnscfg sem parâmetros de linha de comando. No entanto, há um parâmetro disponível, descrito na tabela a seguir.



| Parâmetro | Comportamento                         |
|-----------|----------------------------------|
| /Close    | Feche todas as instâncias de wmpnscfg. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





