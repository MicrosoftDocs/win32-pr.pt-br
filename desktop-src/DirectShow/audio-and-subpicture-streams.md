---
description: Fluxos de áudio e subimagem
ms.assetid: 8d361da3-a33a-401c-a750-f9b952022cf6
title: Fluxos de áudio e subimagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f553b5e569274cf7abafd34e897ba53f82e0292899661fb47ace9ada92dd84f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001358"
---
# <a name="audio-and-subpicture-streams"></a>Fluxos de áudio e subimagem

Um disco DVD-Video pode ter até oito fluxos de áudio, numerados de zero a sete, cada um com até seis canais discretos. (Observe que os fluxos de áudio e subimagem são numerados de zero, enquanto os títulos, ângulos e níveis de pais são numerados de um.) Somente um desses fluxos pode ser selecionado em um determinado momento. Para subfiguras, até 32 fluxos estão disponíveis, embora apenas um fluxo possa ser ativado em um determinado momento. Os discos geralmente são criados com fluxos de áudio e subimagem padrão, mas um aplicativo pode permitir que os usuários exibam uma lista de todos os fluxos disponíveis e selecione aquele no idioma que preferirem. As etapas básicas nesse processo são as mesmas para os fluxos de áudio e subimagem.

1.  Determine o número de fluxos disponíveis para um título.
2.  Itere pelos fluxos e recupere os atributos de fluxo para cada um.
3.  Recupere o código de idioma do LCID (identificador de localidade) retornado e crie uma cadeia de caracteres legível.
4.  Preencha uma caixa de listagem ou outro controle de interface do usuário (IU) para permitir que o usuário selecione um fluxo preferencial.

No aplicativo de exemplo de DVD, o método CAudioLangDlg:: MakeAudioStreamList em Dialogs. cpp demonstra as etapas básicas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



