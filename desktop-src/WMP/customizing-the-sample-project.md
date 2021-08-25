---
title: Personalização do exemplo de Project
description: Personalização do exemplo de Project
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player online, personalização de projetos de exemplo
- lojas online, personalização de projetos de exemplo
- tipo 2 lojas online, personalização de projetos de exemplo
- Windows Media Player online, projetos de exemplo
- lojas online, projetos de exemplo
- tipo 2 lojas online, projetos de exemplo
- personalização de projetos de exemplo
- samples,type 2 online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdb57327904d81ac85114af0df9037d6c2c054938f16048f6ca72e711063cc4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902076"
---
# <a name="customizing-the-sample-project"></a>Personalização do exemplo de Project

Ao criar sua própria loja online, você deseja alterar as implementações dos seguintes métodos no arquivo chamado YourProject.cpp:

-   **CYourProject::allowPlay.** Use essa função para aplicar suas regras de negócio para permitir a reprodução de conteúdo protegido.
-   **CYourProject::allow CDYour.** Use essa função para aplicar suas regras de negócio para permitir que os usuários copiem conteúdo protegido para um CD.
-   **CYourProject::allowPDATransfer.** Use essa função para aplicar suas regras de negócio para permitir que os usuários transfiram conteúdo protegido para um dispositivo portátil.
-   **CYourProject::startBackgroundProcessing.** Use essa função para iniciar as tarefas de processamento em segundo plano necessárias. Por exemplo, você pode usar isso como uma oportunidade para verificar se há licenças expiradas.
-   **CYourProject::d eviceAvailable.** Use essa função para iniciar todas as tarefas relacionadas a um dispositivo conectado.
-   **CYourProject::p repareForSync**. Use essa função para executar as tarefas necessárias logo antes de sincronizar a mídia digital com o dispositivo.
-   **CYourProject::serviceEvent.** Use essa função para iniciar e encerrar tarefas que você deseja executar quando sua loja online for a ativa.
-   **CYourProject::stopBackgroundProcessing.** Use essa função para interromper todas as tarefas de processamento em segundo plano iniciadas Windows Media Player chamada **CYourProject::startBackgroundProcessing**.

## <a name="working-with-media-and-playlist-objects"></a>Trabalhando com objetos de mídia e playlist

O **método allowPlay** fornece um ponteiro para a interface **IWMPMedia** como um parâmetro. Essa interface é a interface Windows Media Player que representa objetos de mídia. Ao chamar os métodos nessa interface, você pode trabalhar com os atributos e as propriedades de um item de mídia individual.

Os **métodos allowCDEar** e **allowPDATransfer** fornecem um ponteiro para a interface **IWMPPlaylist** como um parâmetro. Essa interface é a interface Windows Media Player que representa objetos de playlist. Ao chamar os métodos nessa interface, você pode trabalhar com os atributos e propriedades de uma playlist, adicionar itens a uma playlist ou remover itens de uma playlist.

Para saber como remover um item de uma playlist programaticamente, consulte a implementação **de CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**. Para saber mais sobre como trabalhar com objetos de mídia e playlist, consulte [Modelo de objeto de player para linguagens de script.](player-object-model-for-scripting-languages.md)

## <a name="code-that-can-be-removed"></a>Código que pode ser removido

É provável que você queira remover o código que abre as caixas de diálogo porque é improvável que você queira que os usuários decidam quais itens de mídia podem ser reproduzidos ou copiados. Em YourProject.h, remova o seguinte código:

-   A declaração de **CAllowBaseDialog.**
-   A declaração de **CAllow Ltdalog.**
-   A declaração de **CAllowTransferDialog.**

Em YourProject.cpp, remova o seguinte código:

-   A implementação de **CAllowBaseDialog <T> ::OnInitDialog**.
-   A implementação de **CAllowBaseDialog <T> ::OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o plug-in para uma loja online do tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




