---
description: Você pode usar o Microsoft Direct3D para simular fenômenos naturais que envolvem lançamentos de energia.
ms.assetid: a16af13d-3a38-42b5-900b-ff58a0c917b2
title: Fogo, flares e explosões (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4684f94932e7cc9db2560ae23b5be9a07af66727cf05967a5df82bb2e6b5158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095047"
---
# <a name="fire-flares-and-explosions-direct3d-9"></a>Fogo, flares e explosões (Direct3D 9)

Você pode usar o Microsoft Direct3D para simular fenômenos naturais que envolvem lançamentos de energia. Por exemplo, um aplicativo pode gerar a aparência de incêndio aplicando texturas semelhantes a um conjunto de murals. Isso é especialmente eficaz se o aplicativo usa uma sequência de texturas de incêndio para animar o chamas em cada mural no fogo. A variação da velocidade da reprodução da animação do mural para o mural aumenta a aparência do real chamas. A Semblance de chamas 3D intermisturadas pode ser obtida por meio da camada de murals e das texturas nas murals.

Você pode simular flares e piscar aplicando mapas de luz mais brilhantes sucessivamente a todos os primitivos em uma cena. Embora essa seja uma técnica de alta sobrecarga computacional, ela permite que seu aplicativo simule um flare ou flash localizado. Ou seja, a parte da cena em que o FLARE ou o flash se origina pode clarear primeiro.

Outra técnica é posicionar uma mensagem na frente da cena para que toda a área de destino de renderização seja coberta. O aplicativo aplica texturas de branco sucessivas ao mural e diminui a transparência ao longo do tempo. A cena inteira esmaece para o branco como passar o tempo. Esse é um método de sobrecarga baixa de criação de um clarão. No entanto, usando essa técnica, pode ser difícil gerar a aparência de um flash brilhante a partir de uma fonte de luz de ponto único.

As explosões podem ser exibidas em um procedimento de cena 3D semelhante àqueles usados para incêndios, flashes e flares. Por exemplo, seu aplicativo pode usar um mural para exibir uma onda de choques e Plume crescentes de fumaça quando ocorrer a explosão. Ao mesmo tempo, seu aplicativo pode usar um conjunto de murals para simular chamas. Além disso, ele pode posicionar uma única mensagem na frente da cena para adicionar um clarão de luz a toda a cena.

Os enmissões de energia podem ser simulados usando os murals. Seu aplicativo também pode exibi-los usando primitivos que são definidos como listas de linhas ou faixas de linhas. Para obter detalhes, consulte [listas de linhas](line-lists.md) e faixas de [linha](line-strips.md).

Seu aplicativo pode criar campos de força usando os murals ou primitivos definidos como listas de triângulos. Para criar um campo de força de listas de triângulo, defina um conjunto de triângulos não contíguos em uma lista de triângulo igualmente espaçado na região coberta pelo campo de força. As lacunas entre os triângulos permitem que o usuário veja a cena por trás dos triângulos, como você pode esperar ao examinar um campo de força. Aplique uma textura à lista de triângulo que dá aos triângulos a aparência de brilho com energia. Para obter mais informações, consulte as [listas de triângulo](triangle-lists.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos alfa](alpha-examples.md)
</dt> </dl>

 

 



