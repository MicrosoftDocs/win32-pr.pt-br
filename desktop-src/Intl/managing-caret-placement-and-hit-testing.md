---
description: As linguagens de script complexo são divididas em clusters por ScriptShape. A reordenação de caracteres sempre ocorre dentro dos limites do cluster. Os clusters em si têm garantia de antecedência na direção da ordem de leitura.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Gerenciando posicionamento de cursor e teste de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60396a668c89f7392b28adde0bb123060bf50348
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757800"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Gerenciando posicionamento de cursor e teste de clique

As linguagens de script complexo são divididas em [clusters](uniscribe-glossary.md) por [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). A reordenação de caracteres sempre ocorre dentro dos limites do cluster. Os clusters em si têm garantia de antecedência na direção da ordem de leitura.

As informações de cluster na matriz de cluster lógico são usadas para compartilhar a largura de um cluster de glifos igualmente entre os caracteres lógicos que eles representam. Por exemplo, o glifo Lam Alef é dividido em quatro áreas:

-   A metade líder do Lam.
-   A metade à direita do Lam.
-   A metade líder do Alef.
-   A metade à direita do Alef.

As convenções para o posicionamento do cursor nos clusters dependem do script. Para o script em árabe, se a posição do cursor estiver definida entre um caractere base e sua marca de combinação, o cursor será exibido na metade do caractere base. Para o script tailandês, o cursor não pode ser posicionado em um cluster. Portanto, quando o usuário avança o cursor, o aplicativo deve avançar todos os glifos que compõem o cluster.

As funções [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) e [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) convertem entre posições de cursor (em deslocamentos de ponto de código) e posições x (em pixels). A função **ScriptXtoCP** tem conhecimento das convenções de posição de cursor de cada script:

-   Para Índico e tailandês, as posições do cursor são ajustadas aos limites do cluster.
-   Para árabe, as posições de cursor são interpoladas com clusters.
-   Para o Hebraico, em versões anteriores à Usp10.dll, a versão 1,420, as posições de cursor são interpoladas com clusters. A partir do Usp10.dll, a versão 1,420, as posições do cursor são ajustadas aos limites do cluster.

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) e [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) funcionam somente em execuções. As funções exigem que determinados parâmetros venham de chamadas anteriores ao Uniscribe, conforme mostrado na tabela a seguir.



| Parâmetro                                        | Fonte                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *PSA*                                            | Conforme retornado por [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Conforme retornado por [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).     |
| *piAdvance*                                      | Conforme retornado por [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).     |



 

O aplicativo deve estabelecer a execução em que um determinado deslocamento de interpolação ou posição x é antes de passar as informações para [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) ou [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp). Se o aplicativo não salvar as informações de largura, ele poderá fazer testes de clique e o posicionamento do cursor depois de exibir cada execução. Como alternativa, o aplicativo pode armazenar em cache informações suficientes para o teste de clique e o posicionamento do cursor na linha atual, sem a necessidade de reprocessar o parágrafo.

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) retorna um valor de borda à direita para que o aplicativo saiba o lado do caractere ou cluster no qual o usuário clicou. O valor é 0 ou a largura do caractere ou do cluster em pontos de código. A posição do caractere retornado é a posição do caractere em que o usuário clicou. Para obter mais informações, consulte [exibindo o cursor em cadeias bidirecionais](displaying-the-caret-in-bidirectional-strings.md).

Para idiomas como tailandês, para os quais o usuário não deseja posicionar o cursor em um cluster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) define o sinalizador do lado à direita como 0 ou a largura do cluster. Para idiomas como o árabe, para o qual o usuário espera ser capaz de editar em um cluster, **ScriptXtoCP** define o sinalizador de lado à direita como 0 ou como 1.

Para ajudar o aplicativo a estabelecer locais válidos para o cursor ao manipular as teclas de direção, o Uniscribe fornece informações sobre as posições de um cursor válido no membro **fCharStop** nos atributos lógicos retornados por [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak). **True** é retornado para a maioria dos caracteres e **false** para os caracteres entre clusters em scripts como tailandês. O aplicativo deve verificar o valor de **fNeedsCaretInfo** na estrutura de [**\_ Propriedades de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) de um item para ver se é necessário chamar **ScriptBreak** para verificar se há posições de cursor válidas. Se o valor de **fNeedsCaretInfo** for **false**, todos os pontos de código serão posições de cursor válidas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




