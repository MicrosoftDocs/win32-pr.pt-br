---
description: Seus aplicativos podem usar funções de API do Uniscribe para dar suporte à tipografia e à exibição e edição de texto internacional. O Uniscribe usa o parágrafo como a unidade para exibição de texto e a funcionalidade de Uniscribe deve ser usada para o parágrafo inteiro.
ms.assetid: e1adc567-0445-4deb-8634-25653f82127c
title: Exibindo texto com o Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17caf7e7880a61bdf9afbaf6db5b60065b01d3d3960f2ed5629a007aa304b7b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949601"
---
# <a name="displaying-text-with-uniscribe"></a>Exibindo texto com o Uniscribe

Seus aplicativos podem usar funções de API do Uniscribe para dar suporte à tipografia e à exibição e edição de texto internacional. O Uniscribe usa o parágrafo como a unidade para exibição de texto e a funcionalidade de Uniscribe deve ser usada para o parágrafo inteiro.

Ao usar o Uniscribe para exibição de texto, um aplicativo deve passar por um processo de formatação ("layout"), normalmente usando o Uniscribe. O aplicativo divide um parágrafo de texto em cadeias de caracteres com o mesmo estilo, chamado "execuções". O estilo é determinado pela implementação específica, mas normalmente inclui atributos como fonte, tamanho e cor. Ao definir execuções, o aplicativo também pode aplicar outras informações, como os dados de idioma e localidade mantidos para uso com ferramentas lexicais. Por exemplo, um aplicativo pode tratar como uma passagem de execução separada em um texto essencialmente em inglês que é renderizado em francês.

Depois de determinar as execuções para todos os parágrafos, o aplicativo divide cada parágrafo em cadeias de caracteres que têm o mesmo script e direção ("itens"). O aplicativo aplica as informações do item para produzir execuções que são exclusivas no script e na direção e ficam totalmente dentro de um único item ("Ranges").

A divisão de um item em intervalos é um pouco arbitrária, embora um intervalo deva consistir em um ou mais agrupamentos de caracteres de indivisível, definidos por script consecutivos, chamados de "clusters". Para idiomas europeus, um cluster geralmente corresponde a um único caractere de página de código ou ponto de código Unicode e consiste em um único [glifo](uniscribe-glossary.md). No entanto, em idiomas como o tailandês, um cluster é um agrupamento de glifos e corresponde a vários caracteres consecutivos ou pontos de código. Por exemplo, um cluster tailandês pode conter uma consoante, uma vogal e uma marca de Tom. Para que ele não interrompa os clusters, o aplicativo normalmente deve usar os intervalos mais longos que ele pode ou usar suas próprias informações léxicas para quebrar entre intervalos em locais que não estão no meio de um cluster.

Quando ele identificou os clusters em cada intervalo, o aplicativo deve determinar o tamanho de cada cluster. Ele usa o Uniscribe para somar os clusters para determinar o tamanho de cada intervalo. Em seguida, o aplicativo soma os tamanhos dos intervalos até que eles ultrapassem uma linha, ou seja, atinjam a margem. O intervalo que estoura a linha é dividido entre a linha atual e a próxima linha. Para cada linha, o aplicativo cria um mapa da posição Visual para a posição lógica de cada intervalo. Em seguida, o aplicativo aponta os pontos de código para cada intervalo em glifos, que podem ser subsequentemente posicionados e renderizados.

Um aplicativo faz o layout de texto apenas uma vez. Depois disso, ele salva os glifos e as posições para fins de exibição ou os gera sempre que exibe o texto, com a compensação em velocidade versus memória. Um aplicativo típico implementa o processo de layout uma vez e, em seguida, gera os glifos e posições cada vez que exibe o texto.

Um aplicativo que usa [scripts complexos](uniscribe-glossary.md) tem os seguintes problemas com uma abordagem simples para layout e exibição.

-   A largura de um caractere de script complexo depende de seu contexto. Não é possível salvar as larguras em tabelas simples.
-   A quebra entre palavras em scripts como o tailandês requer suporte a dicionário. Por exemplo, nenhum caractere separador é usado entre as palavras em tailandês.
-   Árabe, Hebraico, persa, urdu e outras linguagens de [texto bidirecionais](uniscribe-glossary.md) exigem reordenação antes da exibição.
-   Muitas formas de associação de fontes geralmente são necessárias para o uso fácil de scripts complexos.

O fato de o Uniscribe usar o parágrafo como a unidade de exibição ajuda o aplicativo a lidar adequadamente com esses problemas complexos de script.

> [!Note]  
> O Uniscribe deve ser usado para um parágrafo inteiro, mesmo que as seções do parágrafo não sejam scripts complexos.

 

Conforme mostrado na tabela a seguir, o Uniscribe versão 1,6 ou superior dá suporte a várias funções que aproveitam as marcas OpenType. Eles podem ser substituídos pelas funções regulares de Uniscribe correspondentes. Em geral, seus aplicativos devem funcionar inteiramente com funções de um conjunto ou outro e não devem tentar "misturar e combinar" funções.



| Função de Uniscribe regular             | Função OpenType equivalente                           |
|----------------------------------------|--------------------------------------------------------|
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) | [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     | [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)     |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)     | [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)     |



 

## <a name="lay-out-text-using-uniscribe"></a>Dispor texto usando o Uniscribe

Seu aplicativo pode usar as etapas a seguir para fazer o layout de um parágrafo de texto com o Uniscribe. Este procedimento pressupõe que o aplicativo já tenha dividido o parágrafo em execuções.

1.  Chame [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) somente ao iniciar ou ao receber uma mensagem do [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) .
2.  Adicional Chame [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex) para determinar se o parágrafo requer processamento complexo.
3.  Adicional Se estiver usando o Uniscribe para manipular a substituição de texto bidirecional e/ou dígito, chame [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) para preparar o [**\_ controle de script**](/windows/win32/api/usp10/ns-usp10-script_control) e as estruturas de [**\_ estado do script**](/windows/win32/api/usp10/ns-usp10-script_state) como entradas para [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). Se você ignorar esta etapa, mas ainda precisar de substituição de dígitos, substitua os dígitos nacionais para Unicode U + 0030 por U + 0039 (dígitos europeus). Para obter informações sobre substituição de dígitos, consulte [formas de dígitos](digit-shapes.md).
4.  Chame [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) para dividir o parágrafo em itens. Se não estiver usando o Uniscribe para substituição de dígitos e a ordem bidirecional for conhecida, por exemplo, devido ao layout do teclado usado para inserir o caractere, chame **ScriptItemize**. Na chamada, forneça ponteiros nulos para [**o \_ controle de script**](/windows/win32/api/usp10/ns-usp10-script_control) e estruturas de [**\_ estado de script**](/windows/win32/api/usp10/ns-usp10-script_state) . Essa técnica gera itens pelo uso somente do mecanismo de Shaping, e os itens podem ser reordenados usando as informações do mecanismo.
    > [!Note]  
    > Normalmente, os aplicativos que funcionam apenas com scripts da esquerda para a direita e sem nenhuma substituição de dígito devem passar por ponteiros nulos para o [**\_ controle de script**](/windows/win32/api/usp10/ns-usp10-script_control) e estruturas de [**\_ estado de script**](/windows/win32/api/usp10/ns-usp10-script_state) .

     

5.  Mescle as informações do item com as informações de execução para produzir intervalos.
6.  Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para identificar clusters e gerar glifos.
7.  Se [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) retornar o código \_ E o \_ script USP não estiver \_ \_ em \_ Font ou S \_ OK com a saída que contém os glifos ausentes, selecione os caracteres de uma fonte diferente. Substitua outra fonte ou desabilite a formatação definindo o membro **eScript** da estrutura [**de \_ análise de script**](/windows/win32/api/usp10/ns-usp10-script_analysis) passada para **ScriptShape** para script \_ indefinido. Para obter mais informações, consulte [usando o fallback de fonte](using-font-fallback.md).
8.  Chame [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para gerar [larguras avançadas](uniscribe-glossary.md) e posições x e y para os glifos em cada intervalo sucessivo. Esta é a primeira etapa para qual o tamanho do texto se torna uma consideração.
9.  Some os tamanhos de intervalo até que a linha fique estourada.
10. Quebre o intervalo em um limite de palavra usando os membros **fSoftBreak** e **fWhiteSpace** nos atributos lógicos. Para interromper um único cluster de caracteres de execução, use as informações retornadas chamando [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).
    > [!Note]  
    > Decida se o primeiro ponto de código de um intervalo deve ser um ponto de quebra de palavra porque o último caractere do intervalo anterior exige. Por exemplo, se um intervalo terminar em uma vírgula, considere o primeiro caractere do próximo intervalo como um ponto de quebra de palavra.

     

11. Repita as etapas de 6 a 10 para cada linha no parágrafo. No entanto, se a última execução for interrompida na linha, chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para remodelar a parte restante da execução como a primeira execução na próxima linha.

## <a name="display-text-using-uniscribe"></a>Exibir texto usando o Uniscribe

Seu aplicativo pode usar as etapas a seguir para exibir um parágrafo de texto. Este procedimento pressupõe que o aplicativo já tenha definido o texto e não salvou os glifos e as posições do processo de layout. Se a velocidade for uma preocupação, o aplicativo poderá salvar os glifos e as posições do procedimento de layout e começar na etapa 2 no procedimento de exibição.

> [!Note]  
> O aplicativo poderá omitir a etapa 2 se o texto não contiver caracteres de scripts da direita para a esquerda, não contiver nenhum caractere de controle bidirecional e usar um nível de incorporação de base da esquerda para a direita.

 

1.  Para cada execução, faça o seguinte:
    1.  Se o estilo tiver sido alterado desde a última execução, atualize o identificador para o contexto do dispositivo, liberando-o e obtendo-o novamente.
    2.  Chame [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) para gerar glifos para a execução.
    3.  Chame [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) para gerar uma largura de avanço e um deslocamento x, y para cada glifo.
2.  Faça o seguinte para estabelecer a ordem visual correta para as execuções na linha:
    1.  Extraia uma matriz de [níveis de incorporação](uniscribe-glossary.md)bidirecional, uma por intervalo. O nível de incorporação é fornecido pelo si (item de SCRIPT \_ ) si. ( \_Análise de script) a. (SCRIPT \_ STATE) s. uBidiLevel.
    2.  Passe essa matriz para [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout) para gerar um mapa de posições visuais para posições lógicas.
3.  Adicional Para justificar o texto, chame [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) ou use o conhecimento especializado do texto.
4.  Use o mapa de Visual para lógico para exibir as execuções em ordem visual. Começando na extremidade esquerda da linha, chame [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) para exibir a execução fornecida pela primeira entrada no mapa. Para cada entrada subsequente no mapa, chame **ScriptTextOut** para exibir a execução indicada à direita da execução exibida anteriormente.

    Se omitir a etapa 2, comece na extremidade esquerda da linha e chame [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) para exibir a primeira execução lógica e, em seguida, para exibir cada execução lógica à direita da execução anterior.

5.  Repita as etapas acima para todas as linhas do parágrafo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 
