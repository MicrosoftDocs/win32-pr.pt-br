---
title: Modo retido versus modo imediato
description: As APIs de gráficos podem ser divididas em APIs de modo retido e em APIs de modo imediato.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559798"
---
# <a name="retained-mode-versus-immediate-mode"></a>Modo retido versus modo imediato

As APIs de gráficos podem ser divididas em APIs de *modo retido* e em APIs *de modo imediato* . Direct2D é uma API de modo imediato. Windows Presentation Foundation (WPF) é um exemplo de uma API de modo retido.

Uma API de modo retido é declarativa. O aplicativo constrói uma cena a partir de primitivos gráficos, como formas e linhas. A biblioteca de gráficos armazena um modelo da cena na memória. Para desenhar um quadro, a biblioteca de gráficos transforma a cena em um conjunto de comandos de desenho. Entre os quadros, a biblioteca de gráficos mantém a cena na memória. Para alterar o que é renderizado, o aplicativo emite um comando para atualizar a cena, por exemplo, para adicionar ou remover uma forma. Em seguida, a biblioteca é responsável por redesenhar a cena.

![um diagrama que mostra gráficos de modo retido.](images/graphics06.png)

Uma API de modo imediato é o procedimento. Cada vez que um novo quadro é desenhado, o aplicativo emite diretamente os comandos de desenho. A biblioteca de gráficos não armazena um modelo de cena entre os quadros. Em vez disso, o aplicativo controla a cena.

![um diagrama que mostra gráficos de modo imediato.](images/graphics07.png)

APIs de modo retido podem ser mais simples de usar, porque a API faz mais do que o trabalho para você, como inicialização, manutenção de estado e limpeza. Por outro lado, geralmente eles são menos flexíveis, porque a API impõe seu próprio modelo de cena. Além disso, uma API de modo retido pode ter mais requisitos de memória, pois precisa fornecer um modelo de cena de uso geral. Com uma API de modo imediato, você pode implementar otimizações direcionadas.

## <a name="next"></a>Avançar

[Seu primeiro programa Direct2D](your-first-direct2d-program.md)

 

 




