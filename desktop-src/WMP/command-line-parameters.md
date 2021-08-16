---
title: Parâmetros de linha de comando
description: Parâmetros de linha de comando
ms.assetid: c4af8a03-2cab-4ecd-bbd8-c83869822901
keywords:
- Windows Media Player, parâmetros
- Windows Media Player, parâmetros de linha de comando
- Windows Media Player,Wmplayer
- Windows Media Player,Wmpconfig
- Windows Media Player,Wmpnscfg
- parâmetros de linha de comando
- Wmplayer
- Wmpconfig
- Wmpnscfg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2240040453bc60a7a03ca56f205643f97202eb840a501fd13aa417b86aef060d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341946"
---
# <a name="command-line-parameters"></a>Parâmetros de linha de comando

## <a name="command-line-parameters-for-wmplayer"></a>Parâmetros de linha de comando para Wmplayer

Windows Media Player dá suporte a um conjunto de parâmetros de linha de comando que especificam como o Player se comporta quando ele é iniciado. A tabela a seguir detalha os parâmetros e seus comportamentos.



| Syntax                                                                                                              | Comportamento                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*path \\ filename*"(Por exemplo: `wmplayer "c:\filename.wma"` )<br/>                                            | Inicie o Player e reproduza o arquivo.                                                                                                                                                                                                                                                                                                        |
| "*path \\ filename*" /fullscreen(Por exemplo: `wmplayer "c:\filename.wmv" /fullscreen` )<br/>                    | Reproduza o arquivo especificado no modo de tela inteira. Você deve especificar o caminho e o nome do arquivo do conteúdo a ser reproduzir.<br/>                                                                                                                                                                                                                     |
| /Device:{DVD \| AudioCD}(Por exemplo: `wmplayer /device:audio CD` )<br/>                                         | Reproduzir um DVD ou CD de áudio.                                                                                                                                                                                                                                                                                                                    |
| "*nome do arquivo de \\ caminho*? WMPSkin=*nome da capa*"Por exemplo: `wmplayer "c:\filename.wma?wmpskin=headspace"`<br/>        | Abra o Player, aplicando a capa especificada.                                                                                                                                                                                                                                                                                              |
| /Service:*keyname*                                                                                                  | Abra o Player mostrando a loja online especificada por *keyname*. Requer Windows Media Player 10 ou posterior.<br/>                                                                                                                                                                                                                      |
| /Task NowPlaying                                                                                                    | Abra o Player no **recurso Agora Em** Jogo.                                                                                                                                                                                                                                                                                            |
| /Task MediaGuide                                                                                                    | Abra o Player no recurso **Guia de** Mídia (loja online ativa atual Windows Media Player 10 ou posterior).                                                                                                                                                                                                                          |
| /Task CDAudio                                                                                                       | Abra o Player no recurso **Copiar do CD** ( recurso **Desmão** no Windows Media Player 10 ou Windows Media Player 11). Não há suporte para esse parâmetro no Windows Media Player 12.                                                                                                                                                       |
| /Task CDWrite                                                                                                       | Abra o Player no **recurso Gravar.** Requer Windows Media Player 10.<br/>                                                                                                                                                                                                                                                       |
| /Task MediaLibrary                                                                                                  | Abra o Player no recurso **Biblioteca.**                                                                                                                                                                                                                                                                                                |
| /Task RadioTuner                                                                                                    | Abra o Player no recurso **Radio Tuner** (loja online ativa atual no Windows Media Player 10 ou posterior).                                                                                                                                                                                                                          |
| /Task PortableDevice                                                                                                | Abra o Player no recurso **Copiar para CD ou** Dispositivo ( recurso sincronizar no Windows Media Player 10 ou posterior).                                                                                                                                                                                                                            |
| /Task Services /Service *servicename*                                                                               | Abra o Player no recurso **Premium Services,** mostrando o serviço especificado pelo *parâmetro servicename.* Esse valor é o nome exclusivo do serviço. Se o serviço especificado não tiver sido exibido anteriormente, o *parâmetro servicename* será ignorado. (Abre a loja online especificada no Windows Media Player 10 ou posterior.) |
| /Task ServiceTask *X*                                                                                                | Abra o Player no painel de tarefas do serviço de loja online especificado por *X*. Por exemplo, /Task ServiceTask1 abre o Player no primeiro painel de tarefas do serviço de loja online.                                                                                                                                                                      |
| /Task SkinViewer                                                                                                    | Abra o Player no recurso **De escolha de** capa.                                                                                                                                                                                                                                                                                           |
| /Playlist *PlaylistName*                                                                                            | Abra o Player e reproduza a playlist especificada.                                                                                                                                                                                                                                                                                           |
| /Schema:{Music \| Pictures Video TV \| \| \| Other}Por exemplo: `wmplayer /Schema:Pictures /Task:PortableDevice`<br/> | Abra o Player, mostrando a categoria de mídia especificada. Requer Windows Media Player 11.                                                                                                                                                                                                                                                   |



 

## <a name="command-line-parameters-for-wmpconfig"></a>Parâmetros de linha de comando para Wmpconfig

Wmpconfig.exe é usado para executar determinados comandos em Windows Media Player que exigem permissão de administrador. Os exemplos incluem o início e a interrupção de serviços de navegação e compartilhamento e a habilitação de exceções no firewall Windows aplicativo. A tabela a seguir descreve os valores possíveis para os parâmetros de linha de comando.



| Syntax                                                                                    | Comportamento                                                                   |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| DisableHMEDevice *MAC*                                                                    | Desabilita o dispositivo especificado por um identificador MAC (Controle de Acesso de Mídia).  |
| Exemplo de HMEOff:<br/> wmpconfig HMEOff<br/>                                    | Desabilita o serviço Windows Media Player de compartilhamento de rede.                 |
| Exemplo de HMEOn:<br/> Wmpconfig HMEOn<br/>                                      | Habilita o compartilhamento, a navegação e a exceção de firewall.                     |
| RemoveHMEDevice *MAC*                                                                     | Remove o dispositivo especificado por um identificador MAC.                          |
| RestoreHMEDevice *MAC*                                                                    | Restaura o dispositivo especificado por um identificador MAC.                         |
| Exemplo de nível SetDVDParentalLevel: <br/> wmpconfig SetDVDParentalLevel 3<br/> | Define o nível de controle dos pais do DVD. O nível é especificado como um inteiro. |



 

## <a name="command-line-parameters-for-wmpnscfg"></a>Parâmetros de linha de comando para Wmpnscfg

O Microsoft Windows usa wmpnscfg.exe para alertar os usuários quando os dispositivos de renderização de mídia são encontrados na rede. O Wmpnscfg inicia Windows Media Player NSS (Serviço de Compartilhamento de Rede) e aguarda notificações do serviço. Quando wmpnscfg é notificado de que um novo dispositivo de mídia está disponível na rede, ele exibe um pop-up na bandeja do sistema que informa ao usuário sobre a disponibilidade do novo dispositivo. Se o usuário clicar no pop-up, o wmpnscfg iniciará o Windows Media Player, que exibe uma caixa de diálogo que solicita que o usuário permita ou negue o compartilhamento com o novo dispositivo.

Normalmente, o Windows chama wmpnscfg sem parâmetros de linha de comando. No entanto, há um parâmetro disponível, descrito na tabela a seguir.



| Parâmetro | Comportamento                         |
|-----------|----------------------------------|
| /Close    | Feche todas as instâncias de wmpnscfg. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 





