---
title: Sobre a sincronização de playlist
description: Sobre a sincronização de playlist
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronização de playlist
- Modelo de objeto do Windows Media Player, sincronização de playlist
- modelo de objeto, sincronização de playlist
- Controle ActiveX do Windows Media Player, sincronização de playlist
- Controle ActiveX, sincronização de playlist
- Controle ActiveX móvel do Windows Media Player, sincronização de playlist
- Windows Media Player Mobile, sincronização de playlist
- Sincronizando dispositivos, listas de reprodução
- sincronização de dispositivo, listas de reprodução
- listas de reprodução, sincronização
- Listas de reprodução do metarquivo do Windows Media, sincronização
- listas de reprodução de metarquivo, sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293762"
---
# <a name="about-playlist-synchronization"></a>Sobre a sincronização de playlist

O Windows Media Player 10 ou posterior foi projetado para sincronizar o conteúdo de mídia digital para dispositivos usando um modelo de sincronização de playlist. Isso significa que o conteúdo destinado a ser copiado para um dispositivo deve fazer parte de uma lista de reprodução. Quando o usuário opta por transferir o conteúdo de mídia digital individual do seu computador para um dispositivo, o Windows Media Player adiciona o conteúdo a uma lista de reprodução padrão para cópia.

As APIs de sincronização de dispositivo do Windows Media Player também são projetadas para funcionar dessa forma. Como o Windows Media Player, seu programa pode apresentar ao usuário uma lista de listas de reprodução que ele definiu. Em seguida, você pode permitir que o usuário escolha quais listas de reprodução sincronizar com um dispositivo específico e defina a ordem de prioridade para o processo de sincronização.

Como os dispositivos portáteis têm uma capacidade de armazenamento limitada, é possível que o usuário opte por sincronizar mais conteúdo de mídia digital do que o dispositivo pode armazenar. O Windows Media Player sincroniza o conteúdo em ordem de prioridade. O usuário pode definir a ordem de prioridade usando uma caixa de diálogo que pode ser acessada por meio do recurso **dispositivos** . Em resposta à entrada do usuário para seu programa, você pode alterar a ordem de prioridade programaticamente alterando os valores de determinados atributos da lista de reprodução. Coletivamente, esses atributos são chamados de atributos de *sincronização* .

Cada playlist em uma biblioteca tem 16 atributos de sincronização: **Sync01** a **Sync16**. Cada atributo representa o dispositivo que tem o índice de parceria correspondente. O valor de cada atributo informa duas coisas:

-   Se a playlist deve ser sincronizada com o dispositivo.
-   O valor de prioridade para a lista de reprodução.

Um valor de zero indica que o Windows Media Player não deve tentar sincronizar a playlist com o dispositivo. Qualquer outro valor é um número de prioridade. Valores mais baixos recebem prioridade mais alta no tempo de sincronização.

As listas de reprodução também têm um atributo **SyncOnly** que indica se a playlist está disponível apenas para sincronização.

Itens individuais de conteúdo de mídia digital contêm metadados sobre a sincronização também. Ao recuperar um objeto de **mídia** da biblioteca, você pode inspecionar o valor do atributo **SyncState** . Esse atributo fornece informações estendidas sobre se o conteúdo foi copiado com êxito no dispositivo ou se houve falha ao copiar o conteúdo porque ele não se ajustaria.

> [!Note]  
> Você deve evitar fornecer elementos de interface do usuário que permitem ao usuário criar listas de reprodução de todo o conteúdo da biblioteca para sincronização.

 

Para otimizar o desempenho, o Windows Media Player impõe um conjunto de regras para a criação de listas de reprodução de sincronização. Seu programa deve criar somente listas de reprodução de sincronização para o conteúdo fornecido. Permitir que o Windows Media Player crie listas de reprodução de sincronização para o conteúdo que o usuário adicionou à biblioteca de outras fontes.

Como alternativa para criar sua própria interface do usuário de playlist, você pode apresentar aos usuários uma caixa de diálogo padrão para escolher as listas de reprodução e gerenciar a parceria para um dispositivo. Para fazer isso, chame [IWMPSyncDevice:: Configurations](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings). Quando você invoca esse método, o Windows Media Player exibe a caixa de diálogo Configurações de sincronização. Quando o usuário fecha a caixa de diálogo, o Windows Media Player retorna automaticamente ao seu estado de encaixe anterior e passa o controle de volta para o programa remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre a sincronização do dispositivo**](about-device-synchronization.md)
</dt> <dt>

[**Gerenciando listas de reprodução de sincronização**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos da lista de reprodução**](playlist-attributes.md)
</dt> </dl>

 

 




