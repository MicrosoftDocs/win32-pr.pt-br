---
description: Uma largura ABC é um valor composto definido por uma estrutura GDI ABC. A estrutura contém membros abcA, abcB e abcC, correspondentes ao &\# 0034; Um&\# 0034;, &\# 0034; B&\# 0034;e &\# 0034; C&\# 0034; larguras de um glifo ou executar.
ms.assetid: 48c766e5-a69d-47d2-a885-f24b80e910d8
title: Glossário uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 808ff2e9620810fe2ec344a037437e6ce8d62bff9460a53cf7b777cedc9d46b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146959"
---
# <a name="uniscribe-glossary"></a>Glossário uniscribe

Uma largura ABC é um valor composto definido por uma estrutura GDI [**ABC.**](/windows/win32/api/wingdi/ns-wingdi-abc) A estrutura contém membros **abcA**, **abcB** e **abcC**, correspondentes às larguras "A", "B" e "C" de um [glifo](#glyph) ou [executar](#run).

A largura "A" é sublinhada [(positiva;](#underhang) também conhecida como "preenchimento") ou sobrecarro [(negativa)](#overhang) à esquerda do equivalente de tinta na tela que representa o glifo ou a run. A largura "B" é a largura preta, a largura da tinta mais à esquerda até a tinta mais à direita. A largura "C" é sobressupida à direita da tinta.

A ilustração a seguir mostra um F minúsculo itálico com sobreabo à esquerda e à direita. Ou seja, as larguras "A" e "C" aqui são ambas negativas. Confira [abaixo para ver](#underhang) uma ilustração das larguras positivas "A" e "C".

![ilustração mostrando um F minúsculo itálico com sobreabo à esquerda e à direita.](images/abcwidth.gif)

Quando dois ou mais glifos são exibidos como uma unidade, geralmente apenas o glifo mais à esquerda contribui para a largura "A" da corrida e apenas o glifo mais à direita contribui para a largura "C" da run. No entanto, essa não é uma regra estrita. Por exemplo, se o primeiro glifo em uma corrida for uma letra estreita e o segundo glifo for uma marca diacrítica larga e eles são tratados como glifos separados, a marca diacrítica pode realmente se estender além da letra.

## <a name="abc-width"></a>Largura ABC

Uma largura ABC é um valor composto definido por uma estrutura GDI [**ABC.**](/windows/win32/api/wingdi/ns-wingdi-abc) A estrutura contém membros **abcA**, **abcB** e **abcC**, correspondentes às larguras "A", "B" e "C" de um [glifo](#glyph) ou [executar](#run).

A largura "A" é sublinhada [(positiva;](#underhang) também conhecida como "preenchimento") ou sobrecarro [(negativa)](#overhang) à esquerda do equivalente de tinta na tela que representa o glifo ou a run. A largura "B" é a largura preta, a largura da tinta mais à esquerda até a tinta mais à direita. A largura "C" é sobressupida à direita da tinta.

A ilustração a seguir mostra um F minúsculo itálico com sobreabo à esquerda e à direita. Ou seja, as larguras "A" e "C" aqui são ambas negativas. Confira [abaixo para ver](#underhang) uma ilustração das larguras positivas "A" e "C".

![ilustração mostrando um F minúsculo itálico com sobreabo à esquerda e à direita.](images/abcwidth.gif)

Quando dois ou mais glifos são exibidos como uma unidade, geralmente apenas o glifo mais à esquerda contribui para a largura "A" da corrida e apenas o glifo mais à direita contribui para a largura "C" da run. No entanto, essa não é uma regra estrita. Por exemplo, se o primeiro glifo em uma corrida for uma letra estreita e o segundo glifo for uma marca diacrítica larga e eles são tratados como glifos separados, a marca diacrítica pode realmente se estender além da letra.

## <a name="advance-width"></a>largura de avanço

A largura de avanço de um [glifo](#glyph) é o movimento na direção da escrita do ponto de partida para renderizar esse glifo até o ponto de partida para renderizar o próximo glifo.

## <a name="bidirectional-stack"></a>pilha bidirecional

A pilha bidirecional é um inteiro de 5 bits que acompanha os níveis de aninhamento entre o texto da esquerda para a direita e da direita para a esquerda. Ele sempre começa em zero para a esquerda para a direita. Portanto, todos os valores numerados ainda representam o texto da esquerda para a direita e todos os valores numerados ímpares representam o texto da direita para a esquerda. A pilha bidirecional é representada no membro **uBidiLevel** de uma [**estrutura SCRIPT \_ STATE.**](/windows/win32/api/usp10/ns-usp10-script_state)

## <a name="bidirectional-text"></a>texto bidirecional

O texto bidirecional contém partes da esquerda para a direita e da direita para a esquerda, mas o termo também é, às vezes, aplicado livremente ao texto puro da direita para a esquerda. Todo o texto da direita para a esquerda requer o uso [](#embedding-level) da pilha [bidirecional](#bidirectional-stack), porque o nível de incorporação padrão de zero implica texto da esquerda para a direita.

## <a name="cell-width"></a>largura da célula

Um aplicativo pode justificar o texto para ajustar uma linha ajustando a largura da célula para determinados glifos. Para texto não verificado, a largura da célula para um glifo é a mesma que sua [largura de avanço.](#advance-width)

## <a name="cluster"></a>cluster

Um cluster é a menor unidade linguística que pode ser formaada. Em linguagens como árabe e muitas das linguagens indic, os glifos usados para representar cada caractere (ponto de código Unicode) dependem fortemente dos pontos de código ao redor, que constituem o cluster. Nesses idiomas, os aplicativos podem converter pontos de código em glifos apropriados apenas observando o cluster. Em alguns scripts, como Devanagari, a ordem de glifos em um cluster pode ser diferente da ordem dos pontos de código Unicode correspondentes. Para obter mais informações, [Windows processamento de glifo no](/typography/develop/processing-part1) site de tipografia da Microsoft.

## <a name="complex-script"></a>script complexo

Um script complexo é um [script](#complex-script) com qualquer uma das seguintes propriedades:

-   Permite a renderização bidirecional.
-   Tem formatação contextual.
-   Tem caracteres de combinação.
-   Tem regras especializadas de quebra de palavras e justificativa.
-   Filtra combinações de caracteres ilícitos.
-   Não há suporte no núcleo de fontes Windows e, portanto, pode exigir [fallback de fonte](#font-fallback).

Em alguns scripts complexos, a ordem dos glifos pode ser bem diferente da ordem dos caracteres Unicode subjacentes que eles representam. Consulte [Sobre scripts complexos](about-complex-scripts.md) para obter mais detalhes.

> [!Note]  
> No contexto da tipografia, às vezes é desejável lidar com o script latino usado na escrita em inglês como um script complexo. Exemplos incluem o recurso Alternativas Estilísticas descrito na documentação do [**OPENTYPE \_ FEATURE \_ RECORD**](/windows/desktop/api/Usp10/ns-usp10-opentype_feature_record)ou ligaduras, como "fi", em que um único glifo representa dois ou mais caracteres consecutivos.

 

## <a name="embedding-level"></a>nível de incorporação

No [texto bidirecional](#bidirectional-text), o nível de incorporação é o índice da [pilha bidirecional](#bidirectional-stack).

## <a name="font-fallback"></a>fallback de fonte

O fallback de fonte é uma seleção automatizada de uma fonte diferente da fonte selecionada pelo usuário em um aplicativo. No Uniscribe, o fallback de fonte é aplicado pela função [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando todo ou parte do texto está em um script que a fonte selecionada pelo usuário não dá suporte.

## <a name="glyph"></a>glyph

Um glifo é uma única unidade de exibição em uma fonte. Para OpenType, essa unidade é definida por um contorno. Para outros tipos de fontes, ele pode ser definido por um bitmap, um conjunto de comandos gráficos e outros tipos. Um glifo não corresponde necessariamente a um único caractere. Por exemplo, a ligatura "fi" ("fi") representa os dois caracteres "f" e "i". O "o" em minúsculas do Grupo com circunflexo e til ("") normalmente é composto de vários glifos.

## <a name="item"></a>item

Um item tem um único [script e](#complex-script) direção. A [**função ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) ou [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) pode analisar um parágrafo em itens. Um item não é necessariamente uma [executar](#run). Ele pode conter caracteres de vários estilos. As informações de item e de executar devem ser combinadas para determinar [intervalos](#range).

## <a name="lrm"></a>LRM

LRM indica a MARCA DA ESQUERDA PARA A DIREITA (ponto de código Unicode U+200E). Essa marca especifica que os caracteres que o seguem na ordem lógica devem ser renderizados da esquerda para a direita.

## <a name="ltr"></a>Ltr

LTR indica da esquerda para a direita.

## <a name="range"></a>range

Um intervalo é um caso especial de uma [executar](#run). Ele se enquadra inteiramente em um [item](#item). Portanto, se um item for dividido em executações, cada uma dessas executações será um intervalo.

## <a name="rlm"></a>Rlm

A RLM indica a MARCA DA DIREITA PARA A ESQUERDA (ponto de código Unicode U+200F). Essa marca indica que os caracteres que o seguem na ordem lógica devem ser renderizados da direita para a esquerda.

## <a name="rtl"></a>RTL

RTL indica da direita para a esquerda.

## <a name="run"></a>Executar

Uma run é uma passagem de texto para o Uniscribe renderizar. Ele deve ter um único estilo, ou seja, fonte, tamanho e cor, mas pode ser desenhado de uma variedade de [scripts](#complex-script). Uma run pode conter conteúdo da esquerda para a direita e da direita para a esquerda.

## <a name="nads"></a>Nads

NADS indica FORMAS NATIONAL DIGIT (ponto de código Unicode U+206E. O termo especifica que os dígitos europeus (U+0030 a U+0039) devem ser renderizados como dígitos nacionais. Consulte [Formas de dígito](digit-shapes.md) para mais discussão sobre dígitos nacionais.

## <a name="nods"></a>NÓS nesta

NÓS nesta indica formas de dígitos nominais (ponto de código Unicode U + 206F). O termo especifica que os dígitos europeus (U + 0030 a U + 0039) devem ser renderizados normalmente, e não como dígitos nacionais.

## <a name="overhang"></a>folga

A folga é a parte da tinta de um glifo que se estende além da [largura antecipada](#advance-width) do glifo. A maioria dos glifos (como "H") não tem nenhuma folga, pois há um pouco de espaço em branco em ambos os lados para separá-los dos glifos adjacentes. Um exemplo de um glifo com folga é o "f" em itálico usado neste tópico para ilustrar a [largura ABC](#abc-width). Tanto a parte superior quanto a inferior do itálico "f" os glifos adjacentes. A folga corresponde a uma largura negativa de "A" ou "C".

## <a name="padding"></a>preenchimento

Confira em [suspensão](#underhang).

## <a name="script"></a>Script

Um script é um sistema de linguagem escrita, por exemplo, script latino, script árabe, script de chinês. Um único script pode ser aplicado a um ou vários idiomas humanos. O script não tem nenhuma relação específica com uma fonte. Por exemplo, o script Latin pode ser renderizado igualmente bem pela fonte Times New Roman ou Arial.

## <a name="underhang"></a>em suspensão

O subtrave é uma largura de espaço em branco à esquerda ou à direita da parte sólida de um glifo. Subhang corresponde a uma largura "A" ou "C" positiva, conforme descrito para a [largura ABC](#abc-width). A subparada é, às vezes, conhecida como "Padding". A ilustração a seguir mostra a subsuspensão da letra minúscula n.

![ilustração mostrando a subsuspensão da letra minúscula n.](images/underhang.gif)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 
