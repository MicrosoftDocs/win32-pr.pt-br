---
title: Sobre a sincronização de playlist
description: Sobre a sincronização de playlist
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronização de playlist
- modelo de objeto Windows Media Player, sincronização de playlist
- modelo de objeto, sincronização de playlist
- controle de ActiveX de Windows Media Player, sincronização de playlist
- controle de ActiveX, sincronização de playlist
- Windows Media Player controle de ActiveX móvel, sincronização de playlist
- Windows Media Player Sincronização móvel, lista de reprodução
- Sincronizando dispositivos, listas de reprodução
- sincronização de dispositivo, listas de reprodução
- listas de reprodução, sincronização
- Windows Listas de reprodução de metarquivo de mídia, sincronização
- listas de reprodução de metarquivo, sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe54bef188fea2baee64da962dabf4eb8f700b72407772d591d73f52be2d4289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956866"
---
# <a name="about-playlist-synchronization"></a>Sobre a sincronização de playlist

o Windows Media Player 10 ou posterior foi projetado para sincronizar o conteúdo de mídia digital para dispositivos usando um modelo de sincronização de playlist. Isso significa que o conteúdo destinado a ser copiado para um dispositivo deve fazer parte de uma lista de reprodução. quando o usuário opta por transferir o conteúdo de mídia digital individual do seu computador para um dispositivo, Windows Media Player adiciona o conteúdo a uma lista de reprodução padrão para cópia.

as APIs de sincronização de dispositivo Windows Media Player também são projetadas para funcionar assim. como Windows Media Player, seu programa pode apresentar ao usuário uma lista de listas de reprodução que ele definiu. Em seguida, você pode permitir que o usuário escolha quais listas de reprodução sincronizar com um dispositivo específico e defina a ordem de prioridade para o processo de sincronização.

Como os dispositivos portáteis têm uma capacidade de armazenamento limitada, é possível que o usuário opte por sincronizar mais conteúdo de mídia digital do que o dispositivo pode armazenar. Windows Media Player sincroniza o conteúdo em ordem de prioridade. O usuário pode definir a ordem de prioridade usando uma caixa de diálogo que pode ser acessada por meio do recurso **dispositivos** . Em resposta à entrada do usuário para seu programa, você pode alterar a ordem de prioridade programaticamente alterando os valores de determinados atributos da lista de reprodução. Coletivamente, esses atributos são chamados de atributos de *sincronização* .

Cada playlist em uma biblioteca tem 16 atributos de sincronização: **Sync01** a **Sync16**. Cada atributo representa o dispositivo que tem o índice de parceria correspondente. O valor de cada atributo informa duas coisas:

-   Se a playlist deve ser sincronizada com o dispositivo.
-   O valor de prioridade para a lista de reprodução.

um valor de zero indica que Windows Media Player não deve tentar sincronizar a playlist com o dispositivo. Qualquer outro valor é um número de prioridade. Valores mais baixos recebem prioridade mais alta no tempo de sincronização.

As listas de reprodução também têm um atributo **SyncOnly** que indica se a playlist está disponível apenas para sincronização.

Itens individuais de conteúdo de mídia digital contêm metadados sobre a sincronização também. Ao recuperar um objeto de **mídia** da biblioteca, você pode inspecionar o valor do atributo **SyncState** . Esse atributo fornece informações estendidas sobre se o conteúdo foi copiado com êxito no dispositivo ou se houve falha ao copiar o conteúdo porque ele não se ajustaria.

> [!Note]  
> Você deve evitar fornecer elementos de interface do usuário que permitem ao usuário criar listas de reprodução de todo o conteúdo da biblioteca para sincronização.

 

para otimizar o desempenho, o Windows Media Player impõe um conjunto de regras para criar listas de reprodução de sincronização. Seu programa deve criar somente listas de reprodução de sincronização para o conteúdo fornecido. permita que Windows Media Player crie playlists de sincronização para o conteúdo que o usuário adicionou à biblioteca de outras fontes.

Como alternativa para criar sua própria interface do usuário de playlist, você pode apresentar aos usuários uma caixa de diálogo padrão para escolher as listas de reprodução e gerenciar a parceria para um dispositivo. Para fazer isso, chame [IWMPSyncDevice:: Configurations](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). quando você invoca esse método, Windows Media Player exibe a caixa de diálogo configurações de sincronização. quando o usuário fecha a caixa de diálogo, Windows Media Player retorna automaticamente ao seu estado de encaixe anterior e passa o controle de volta para o programa remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização do dispositivo**](about-device-synchronization.md)
</dt> <dt>

[**Gerenciando listas de reprodução de sincronização**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos da lista de reprodução**](playlist-attributes.md)
</dt> </dl>

 

 




