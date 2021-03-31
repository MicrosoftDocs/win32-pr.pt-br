---
description: Transições
ms.assetid: 432db77f-c3fa-4234-bbce-cf17d8878b99
title: Transições
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01fef1cd888293ad83ab1ba9f05ab4bb83ddafa9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837011"
---
# <a name="transitions"></a>Transições

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Uma transição é uma maneira de transiçãor de uma faixa de vídeo para outra, usando um efeito visual, como um esmaecimento ou um apagamento. A ilustração a seguir mostra uma linha do tempo com uma transição:

![linha do tempo com transição](images/timeline3.png)

O objeto de transição está no Track 1 e representa uma transição do Track 0 para o Track 1. No início da transição, o vídeo renderizado é inteiramente do Track 0 (origem A). No final, o vídeo é totalmente do Track 1 (fonte C). No between, a saída faz a transição da origem A para a fonte C. Por exemplo, em uma transição de esmaecimento, uma fonte desaparece progressivamente para a outra. A saída final é esquematizados ao longo da parte inferior da ilustração.

As transições não podem se sobrepor no tempo dentro da mesma faixa, mas você pode criar transições sobrepostas usando o objeto de composição, conforme descrito em [composição e camadas](composition-and-layering.md).

Uma transição tem uma direção. Por padrão, ele começa da faixa de prioridade mais baixa (origem A, no exemplo anterior) e termina na faixa de prioridade mais alta (fonte C). No, o vídeo é uma mistura das duas fontes. No entanto, você pode especificar o comportamento oposto, conforme mostrado na ilustração a seguir:

![ntrack com duas transições](images/fade.png)

Aqui, a primeira transição esmaece de Track 0 esmaece Track 1, que é o comportamento padrão. A segunda transição esmaece do Track 1 de volta para o Track 0. Observe que ambas as transições estão localizadas no Track 1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução com os serviços de edição do DirectShow](getting-started-with-directshow-editing-services.md)
</dt> <dt>

[Transições e efeitos](transitions-and-effects.md)
</dt> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



