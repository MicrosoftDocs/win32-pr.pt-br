---
title: Personalizando o projeto de exemplo
description: Personalizando o projeto de exemplo
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Lojas online do Windows Media Player, personalizando projetos de exemplo
- lojas online, personalizando projetos de exemplo
- Digite 2 lojas online, personalizando projetos de exemplo
- Lojas online do Windows Media Player, projetos de exemplo
- lojas online, projetos de exemplo
- Digite 2 lojas online, projetos de exemplo
- Personalizando projetos de exemplo
- exemplos, tipo 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916559"
---
# <a name="customizing-the-sample-project"></a>Personalizando o projeto de exemplo

Ao criar sua própria loja online, você desejará alterar as implementações dos seguintes métodos no arquivo chamado seuprojeto. cpp:

-   **CYourProject:: allowPlay**. Use essa função para aplicar suas regras de negócio para permitir a reprodução de conteúdo protegido.
-   **CYourProject:: permitir cdburn**. Use essa função para aplicar suas regras de negócio para permitir que os usuários copiem conteúdo protegido em um CD.
-   **CYourProject:: allowPDATransfer**. Use essa função para aplicar suas regras de negócio para permitir que os usuários transfiram conteúdo protegido em um dispositivo portátil.
-   **CYourProject:: startBackgroundProcessing**. Use essa função para iniciar as tarefas de processamento em segundo plano que você precisa. Por exemplo, você pode usar isso como uma oportunidade de verificar se há licenças expiradas.
-   **CYourProject::D eviceavailable**. Use essa função para iniciar qualquer tarefa relacionada a um dispositivo conectado.
-   **CYourProject::P repareforsync**. Use essa função para executar as tarefas necessárias antes de sincronizar mídia digital para o dispositivo.
-   **CYourProject:: CreateEvent**. Use essa função para iniciar e encerrar tarefas que você deseja executar quando sua loja online for a ativa.
-   **CYourProject:: stopBackgroundProcessing**. Use essa função para interromper qualquer tarefa de processamento em segundo plano iniciada quando o Windows Media Player chamou **CYourProject:: startBackgroundProcessing**.

## <a name="working-with-media-and-playlist-objects"></a>Trabalhando com objetos de mídia e playlist

O método **allowPlay** fornece um ponteiro para a interface **IWMPMedia** como um parâmetro. Essa interface é a interface do Windows Media Player que representa os objetos de mídia. Ao chamar os métodos nessa interface, você pode trabalhar com os atributos e as propriedades de um item de mídia individual.

Os métodos **allowCDBurn** e **allowPDATransfer** fornecem um ponteiro para a interface **IWMPPlaylist** como um parâmetro. Essa interface é a interface do Windows Media Player que representa os objetos da lista de reprodução. Ao chamar os métodos nessa interface, você pode trabalhar com os atributos e as propriedades de uma lista de reprodução, adicionar itens a uma lista de reprodução ou remover itens de uma lista de reprodução.

Para saber como remover um item de uma playlist programaticamente, consulte a implementação de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**. Para saber mais sobre como trabalhar com objetos de mídia e playlist, confira [modelo de objeto do Player para linguagens de script](player-object-model-for-scripting-languages.md).

## <a name="code-that-can-be-removed"></a>Código que pode ser removido

Provavelmente, você desejará remover o código que abre as caixas de diálogo porque é improvável que você queira que os usuários decidam quais itens de mídia podem ser reproduzidos ou copiados. Em seuprojeto. h, remova o seguinte código:

-   A declaração de **CAllowBaseDialog**.
-   A declaração de **CAllowBurnDialog**.
-   A declaração de **CAllowTransferDialog**.

Em seuprojeto. cpp, remova o seguinte código:

-   A implementação de **CAllowBaseDialog <T> :: OnInitDialog**.
-   A implementação de **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o plug-in para uma loja online tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




