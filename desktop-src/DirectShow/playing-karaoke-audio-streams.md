---
description: reproduzindo Fluxos de áudio do karaokê
ms.assetid: 1a8d0f42-35b8-4743-9ae7-619b99936f76
title: reproduzindo Fluxos de áudio do karaokê
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10912761034feb9ed82c85625324cd3091514b2c492c66b4e49af711d7d2152
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213296"
---
# <a name="playing-karaoke-audio-streams"></a>reproduzindo Fluxos de áudio do karaokê

O navegador de DVD pode reproduzir discos DVD-Video com fluxos de áudio do karaokê, mas a reprodução do karaokê também requer um decodificador que dá suporte à mixagem de karaokê multicanal. Especificamente, o decodificador deve dar suporte ao [**conjunto de propriedades do DVD karaokê**](dvd-karaoke-property-set.md) (am \_ Property \_ DVDKARAOKE).

Os discos do karaokê são um tipo de disco DVD-Video e têm a mesma estrutura de navegação. As músicas geralmente são formatadas como títulos, e os títulos podem ser agrupados em conjuntos de títulos com base no desempenho, no estilo musical ou em outros critérios. A principal diferença entre o karaokê e outros tipos de DVD-Videos é o fluxo de áudio. Todos os discos do karaokê contêm áudio multicanal, geralmente Dolby AC-3. Os canais 0 e 1 sempre contêm a música instrumenta de plano de fundo, enquanto os canais de 2 a 5 podem conter qualquer combinação de vozes de guia, Melodies de guia e efeitos sonoros. Um aplicativo de karaokê pode controlar o volume e o alto-falante de destino para cada canal auxiliar.

Quando o navegador de DVD detecta o conteúdo do karaokê em um disco e entra no modo do karaokê, ele informa ao decodificador que, em seguida, deve ativar mudo dos três canais superiores (os canais auxiliares) até que qualquer um deles seja explicitamente ativado por um aplicativo. As tarefas básicas de um aplicativo do karaokê são:

1.  Determine o número de canais auxiliares e seu conteúdo usando métodos [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) .
2.  Forneça uma interface do usuário que exibe o conteúdo do canal e permite que os usuários ativem ou desativem qualquer canal auxiliar a qualquer momento, usando [**IDvdControl2:: SelectKaraokeAudioPresentationMode**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectkaraokeaudiopresentationmode).

Essas etapas são ilustradas no aplicativo de exemplo de DVD em DVDCore. cpp no método **Getaudioattributes** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



