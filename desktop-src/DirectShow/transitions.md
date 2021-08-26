---
description: Transições
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7511a010de60cdd87907b4ad7faa59963d3f0c6037dce3adc8fc58fa1c0a67a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078688"
---
# <a name="transitions"></a>Transições

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Uma transição é uma maneira de seguir de uma faixa de vídeo para outra, usando um efeito visual, como um esmaeçando ou apagando. A ilustração a seguir mostra uma linha do tempo com uma transição:

![linha do tempo com transição](images/timeline3.png)

O objeto de transição está na faixa 1 e representa uma transição da faixa 0 para a faixa 1. No início da transição, o vídeo renderizado é totalmente da Faixa 0 (origem A). No final, o vídeo é totalmente da Faixa 1 (origem C). Entre elas, a saída faz a transição da origem A para a origem C. Por exemplo, em uma transição de esmaeça, uma origem esmaece progressivamente para a outra. A saída final é eschematizada na parte inferior da ilustração.

As transições não podem se sobrepor no tempo dentro da mesma faixa, mas você pode criar transições sobrepostas usando o objeto de composição, conforme descrito em Composição e [Camadas.](composition-and-layering.md)

Uma transição tem uma direção. Por padrão, ele começa na faixa de prioridade mais baixa (origem A, no exemplo anterior) e termina na faixa de prioridade mais alta (origem C). Entre elas, o vídeo é uma combinação das duas fontes. No entanto, você pode especificar o comportamento oposto, conforme mostrado na ilustração a seguir:

![ntrack com duas transições](images/fade.png)

Aqui, a primeira transição esmaece da faixa 0 esmaece a faixa 1, que é o comportamento padrão. A segunda transição esmaece da faixa 1 de volta para a Faixa 0. Observe que ambas as transições estão localizadas na faixa 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ponto de Partida com os DirectShow de Edição](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transições e efeitos](transitions-and-effects.md)
</dt> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



