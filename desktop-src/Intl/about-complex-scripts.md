---
description: Um script complexo é um script para o qual o membro fComplex das \_ Propriedades de script está definido como true. Este tópico detalha as propriedades que um script complexo pode ter.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Sobre scripts complexos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011305"
---
# <a name="about-complex-scripts"></a>Sobre scripts complexos

Um [script complexo](uniscribe-glossary.md) é um script para o qual  o membro FComplex [**das \_ Propriedades de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) está definido como **true**. Este tópico detalha as propriedades que um script complexo pode ter.

## <a name="bidirectional-rendering"></a>Renderização bidirecional

A renderização bidirecional é o manuseio de texto que é lido da esquerda para a direita e da direita para a esquerda. Por exemplo, na renderização bidirecional de árabe, a direção de leitura padrão para texto é da direita para a esquerda, mas é da esquerda para a direita para alguns números. O processamento de um script complexo deve considerar a diferença entre a ordem lógica (pressionamento de tecla) e a ordem visual dos glifos. Além disso, o processamento deve lidar corretamente com movimentação de cursor e teste de clique. O mapeamento entre a posição da tela e um índice de caracteres requer uma compreensão dos algoritmos de layout para a exibição específica, por exemplo, a seleção da exibição de texto ou de cursor.

## <a name="contextual-shaping"></a>Shaping contextual

No shaping contextual, os caracteres do script alteram a forma dependendo dos caracteres que os circundam. Tal Shaping ocorre em escrita em modo cursivo em inglês quando uma forma "l" de letras minúsculas, dependendo do caractere que a precede, como "a" (conecta-se insuficiente ao "l") ou a um "o" (conecta-se alta). Por exemplo, o árabe é um script que exibe o shaping contextual.

## <a name="combining-characters"></a>Combinação de caracteres

A combinação de caracteres, também chamadas de "ligaturas", são caracteres que entram em um caractere quando colocados juntos. O árabe é um script que tem muitos caracteres de combinação. Um exemplo do uso de caracteres combináveis é o "a" seguido por "combinar acento grave", para o qual a representação renderizada é "à". O fluxo Unicode "U + 0061 U + 0300" requer algum processamento para garantir que a "combinação de acento grave" esteja posicionada corretamente acima de "a".

## <a name="specialized-word-break-and-justification"></a>Quebra de palavra especializada e justificativa

Alguns scripts, por exemplo, tailandês, têm regras complexas para dividir palavras entre linhas ou justificar texto em uma linha.

## <a name="filtering-for-illegal-character-combinations"></a>Filtragem de combinações de caracteres ilegais

Um script complexo, por exemplo, tailandês, pode filtrar combinações de caracteres ilegais quando um idioma não permite determinadas combinações de caracteres.

## <a name="font-fallback"></a>Fallback de fonte

Fallback de fonte é a seleção automatizada de uma fonte diferente da fonte selecionada pelo usuário. No Uniscribe, o fallback de fonte é aplicado pela função [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando todo ou parte do texto está em um script para o qual a fonte selecionada pelo usuário não dá suporte. Para obter mais informações, consulte [usando o fallback de fonte](using-font-fallback.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



