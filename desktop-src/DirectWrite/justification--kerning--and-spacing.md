---
title: Justificativa, kerning e espaçamento
description: a partir do Windows 8, o DirectWrite fornece vários recursos que permitem controlar os recursos básicos tipográficos, de layout e de espaçamento, como espaçamento de caracteres, kerning de pares e justificação.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdd82e201429adb62e687021f003d7d5d6bedcd228c3102f448b04d1f079f71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632619"
---
# <a name="justification-kerning-and-spacing"></a>Justificativa, kerning e espaçamento

a partir do Windows 8, o [DirectWrite](direct-write-portal.md) fornece vários recursos que permitem controlar os recursos básicos tipográficos, de layout e de espaçamento, como espaçamento de caracteres, kerning de pares e justificação.

## <a name="character-spacing"></a>Espaçamento de caracteres

O espaçamento de caracteres, também conhecido como "acompanhamento", é o espaçamento entre os caracteres em uma execução de texto.

Aqui está um exemplo de controle. A primeira linha não aplica nenhum controle ao texto. A segunda linha aumenta o espaçamento de caracteres e a terceira linha diminui o espaçamento de caracteres.

![três exemplos do mesmo texto sem acompanhamento, mais espaçamento e menos espaçamento.](images/spacing.png)

a partir do Windows 8, [DirectWrite](direct-write-portal.md) adiciona esses métodos aqui para controlar o espaçamento de caracteres em seu texto.

se você estiver usando o layout de [DirectWrite](direct-write-portal.md) , poderá usar os métodos [**IDWriteTextLayout1:: GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) e [**IDWriteTextLayout1:: SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) para essa finalidade.

Use o método [**GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) para determinar o espaçamento de caracteres atual e retorna o caractere atual, o espaçamento antes e depois do caractere, a largura mínima de avanço e uma estrutura de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que contém informações sobre a posição inicial e o comprimento do texto restante.

Use o [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) em uma interface [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) para aplicar seu próprio espaçamento de caracteres ao texto no layout. O método **SetCharacterSpacing** assume a quantidade de espaço que você deseja antes e depois do caractere, o avanço mínimo permitido e um [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que define o intervalo para aplicar o espaçamento.

se você estiver usando um layout personalizado, [DirectWrite](direct-write-portal.md) terá suporte para definir o espaçamento de caracteres com [**IDWriteTextAnalyzer1:: ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Use esse método se você precisar de um layout de texto personalizado para ter controle avançado sobre seu layout. Esse método permite que você forneça **ApplyCharacterSpacing** com o espaçamento à esquerda e à direita, a largura mínima de avanço, o comprimento do mapa do cluster, o número de glifos, o mapeamento de intervalos de caracteres para glifos e a largura antecipada de cada glifo se você usar um layout personalizado. O método retorna os avanços de glifo modificados e uma enumeração de [**\_ \_ deslocamento de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) com os novos deslocamentos para a origem de cada glifo.

## <a name="kerning"></a>Kerning

Kerning é o ajuste de espaçamento contextual entre pares ou tercetos de letras. O espaçamento específico entre conjuntos de caracteres pode aumentar a legibilidade e melhorar a aparência do texto. A diferença importante entre kerning e espaçamento de caracteres é o fato de que o espaçamento de letras é independente do texto que ele Space, enquanto o kerning é usado em determinadas situações entre determinados pares de caracteres, conforme definido na fonte.

A imagem é um exemplo de kerning. O AVATAR do Word na linha superior tem kerning para tornar a palavra mais natural. Como você pode ver nas caixas vermelhas ao lado dos caracteres, há mais espaçamento aplicado entre as quatro primeiras letras, enquanto o R no final tem mais espaço antes dela. O texto original sem kerning está na segunda linha. O kerning neste exemplo torna a palavra mais legível e mais natural.

![um exemplo da mesma palavra com e sem kerning aplicado.](images/kerning.png)

o caractere avança entre pares de caracteres que os kerns de fonte são armazenados na tabela de kerning e [DirectWrite](direct-write-portal.md) analisa essa tabela e retorna as informações para você por meio das APIs de kerning.

Se você quiser saber se uma fonte dá suporte a kerning de pares, você pode usar o método [**IDWriteFontFace1:: HasKerningPairs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) . Esse método retornará um valor bool de 1 se a fonte der suporte a pares de kerning.

O [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) também tem um método que permite que você obtenha acesso aos ajustes de par de kerning para índices de glifos. [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) permite que você insira uma matriz de índices de glifos e [DirectWrite](direct-write-portal.md) retorna uma matriz de ajustes de avanço de glifo. Se uma fonte não oferecer suporte à tabela de kerning, o método retornará zeros para os ajustes de avanço de glifo.

se você estiver usando o layout de [DirectWrite](direct-write-portal.md) , há dois métodos na interface [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) que permitem que você defina o kerning de pares e saiba mais sobre o kerning de pares no layout. O método [**SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) usa uma representação booliana de se você deseja ou não o kerning de pares habilitado e um [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que define o intervalo de texto ao qual aplicar. Se desejar saber se o kerning de pares está habilitado em um intervalo de texto, você pode usar o método [**GetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) , que usa a posição atual e retorna um bool que corresponde a se o kerning de pares está habilitado e o intervalo de texto ao qual a configuração de kerning se aplica.

## <a name="justification"></a>Justificativa

A justificativa é o processo de alinhar o texto para que ele preencha todo o espaço dentro de uma coluna, aumentando os avanços entre os caracteres ou os clusters de glifos ou adicionando caracteres de justificação para obter o mesmo efeito. Em geral, isso é feito determinando onde o espaço precisa ser adicionado a uma linha de texto e inserindo caracteres de espaçamento nessas oportunidades de interrupção. Esses elementos de espaçamento também podem diferir, em scripts latinos, o texto é justificado aumentando as larguras de avanço entre os elementos, enquanto em árabe, o texto é justificado com um kashida. Aqui está um exemplo de script árabe e latino justificado e não justificado.

![um exemplo de script árabe e Latin justificado e não justificado.](images/justification.png)

a partir do Windows 8, [DirectWrite](direct-write-portal.md) tem vários métodos que permitem que você justifique o texto em seus aplicativos.

Há um valor adicional na enumeração de [**\_ \_ alinhamento de texto DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) . você pode usar o método [**settextalignion**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e passar a constante **de \_ alinhamento de texto DWRITE \_ \_ justificada** e [DirectWrite](direct-write-portal.md) justificar o texto e inserir o caractere de justificativa apropriado para o script.

Se você estiver usando um layout personalizado, terá um número de métodos disponíveis para que possa aproveitar a justificativa. [DirectWrite](direct-write-portal.md) tem três métodos na interface [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) que você pode usar para adicionar justificativas a um layout personalizado.

O primeiro método é [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities), que usa o texto que você deseja justificar e retorna uma estrutura de [**\_ \_ oportunidade de justificativa de DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que descreve onde os caracteres de justificação podem ser adicionados para justificar o texto.

A segunda função é [**JustifyGlyphAdvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances), que justifica uma matriz de avanços de glifo para que caibam na largura da linha. Esse método usa a estrutura [**de \_ \_ oportunidade de justificação de DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que o [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) gera, os avanços de glifo e os deslocamentos de glifo. Em seguida, ele gera os avanços de glifo justificados e uma enumeração de [**\_ \_ deslocamento de glifo DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) que contém os deslocamentos de glifo justificados.

A terceira função é [**GetJustifiedGlyphs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs), que preenche os novos glifos para scripts complexos em que a justificativa aumentou os avanços dos glifos. **GetJustifiedGlyphs** só precisa ser chamado se o script tiver um caractere de justificativa específico, como retornado por [**getscriptproperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties). Esse método recebe informações sobre a fonte, o comprimento do texto, o tamanho dos glifos, o script do texto, o número de glifos, o mapa do cluster, avanços/deslocamentos de glifo original, avanços/deslocamentos de glifo justificados e propriedades de glifo. O método retorna a contagem de glifos real, o mapa de cluster atualizado, os índices de glifos atualizados com glifos de justificação inseridos, deslocamentos de glifos atualizados e avanços de glifo atualizados.

 

 