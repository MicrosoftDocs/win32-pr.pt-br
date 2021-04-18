---
title: Tentativas de renderização
description: O consórcio de cor internacional (ICC) definiu quatro valores diferentes chamados de tentativas de renderização.
ms.assetid: c980f3ea-daff-491a-a10a-03ba446d383e
keywords:
- WCS (sistema de cores do Windows), tentativas de renderização
- WCS (sistema de cores do Windows), tentativas de renderização
- gerenciamento de cores de imagem, tentativas de renderização
- gerenciamento de cores, tentativas de renderização
- cores, tentativas de renderização
- tentativas de renderização
- ICC (International Color Consortium)
- IIC (consórcio de cor internacional)
- Intenção de imagem
- Intenção gráfica
- Tentativa de prova
- Tentativa de correspondência
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72df148cf4c439c8081e41f3eb8089c5588e7fe2
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105773943"
---
# <a name="rendering-intents"></a>Tentativas de renderização

O consórcio de cor internacional (ICC) definiu quatro valores diferentes chamados de *tentativas de renderização*. Elas representam quatro abordagens diferentes para criar uma renderização de cor. Essas quatro intenções, e as constantes usadas para fazer referência a elas no código são as seguintes.



| Intencional                            | Nome ICC              | Descrição                    |
|-----------------------------------|-----------------------|--------------------------------|
| Picture | Perceptiva            | \_PERCEPTIVA intenção             |
| Graphic | Saturação            | saturação da intenção \_             |
| Prova     | Colorimétrico relativo | \_colorimétrico relativo da intenção \_ |
| Corresponder a     | Colorimétrico absoluto | \_colorimétrico absoluto da intenção \_ |




 

A especificação de formato de perfil ICC versão 3,4, que descreve essas intenções, pode ser baixada em color.org.

## <a name="picture-intent"></a>Intenção de imagem

Chamado perceptiva intenção na cláusula de especificação ICC 4,9, uma intenção de imagem faz com que a [gama](./g.md) completa da imagem seja compactada ou expandida para preencher a gama do dispositivo de destino, de modo que o saldo em cinza seja preservado, mas a precisão colorimétrico pode não ser preservada.

Em outras palavras, se determinadas cores em uma imagem ficarem fora do intervalo de cores que o dispositivo de saída puder renderizar, a intenção de imagem fará com que todas as cores da imagem sejam ajustadas para que cada cor da imagem esteja dentro do intervalo que pode ser renderizado e que a relação entre as cores seja preservada o máximo possível.

Essa intenção é mais adequada para a exibição de fotografias e imagens, e geralmente é a intenção padrão.

## <a name="graphic-intent"></a>Intenção gráfica

A cláusula de especificação ICC 4,12 chama a intenção gráfica uma intenção de [saturação](s.md) . Ele preserva o croma de cores na imagem em uma possível despesa de [matiz](h.md) e [claridade](l.md).

A implementação dessa tentativa permanece um tanto problema, e o ICC ainda está trabalhando em métodos para atingir os efeitos desejados.

Essa intenção é mais adequada para gráficos de negócios, como gráficos, em que é mais importante que as cores sejam vivas e contrastem bem entre si, em vez de uma cor específica.

## <a name="proof-intent"></a>Tentativa de prova

A intenção de prova, chamada de intenção de colorimétrico na especificação ICC, é definida de modo que qualquer cor que esteja fora do intervalo que o dispositivo de saída pode processar seja ajustada para a mais próxima que possa ser renderizada, enquanto todas as outras cores permanecem inalteradas.

A tentativa de prova não preserva o [ponto branco](w.md).

Por exemplo, o branco mais branco de um papel é mais amarelo do que o branco mais branco de um monitor de computador. Uma imagem convertida na gama da impressora usando a intenção colorimétrico relativa resultaria em todas as cores se tornando mais amarelas. O ponto branco da imagem é movido para corresponder ao ponto branco da impressora. Todas as outras cores na imagem mantêm sua posição em relação ao ponto branco. Isso produz uma imagem que reflete com mais precisão qual será a aparência da imagem impressa. No entanto, o usuário pode encontrá-lo visualmente desconcerto.

## <a name="match-intent"></a>Tentativa de correspondência

Em uma tentativa de correspondência, todas as cores que estão fora do intervalo que o dispositivo de saída pode processar são ajustadas para a cor mais próxima que pode ser renderizada, enquanto todas as outras cores permanecem inalteradas. A especificação ICC chama a intenção colorimétrico absoluta de tentativa de correspondência.

A tentativa de correspondência preserva o ponto branco.

Por exemplo, o branco mais branco de um papel é mais amarelo do que o branco mais branco de um monitor de computador. Uma imagem convertida na [gama](./g.md) da impressora usando a tentativa de correspondência resultaria em todas as cores sendo convertidas e correspondidas na gama da impressora. O ponto branco da imagem não é movido para corresponder ao ponto branco da impressora. Portanto, a distância das cores para o ponto branco pode ser alterada. Isso produz uma imagem que é menos visualmente desconcerta ao usuário, mas também é uma representação menos precisa da saída da impressora.

 

 