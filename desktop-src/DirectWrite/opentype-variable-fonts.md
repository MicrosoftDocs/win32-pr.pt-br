---
title: Fontes variáveis OpenType
description: Este tópico descreve fontes de variável OpenType, seu suporte em DirectWrite e Direct2D e como usá-las em seu aplicativo. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c671bebce73cf3bdec42d1f7f570add914db7eb33b8a6bfd1b196d569b9975d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649384"
---
# <a name="opentype-variable-fonts"></a>Fontes variáveis OpenType

Este tópico descreve fontes de variável OpenType, seu suporte em DirectWrite e Direct2D e como usá-las em seu aplicativo. 

-   [O que são fontes de variável OpenType?](#what-are-opentype-variable-fonts)
-   [Suporte à fonte de variável OpenType DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Usando fontes de variável OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>O que são fontes de variável OpenType?

A versão 1.8 da [especificação](https://www.microsoft.com/typography/otspec/) de formato de fonte OpenType introduziu uma nova extensão para o formato conhecido como [Variações de Fonte OpenType.](/typography/opentype/spec/otvaroverview) As fontes que usam essas extensões são conhecidas como fontes de variável OpenType. Uma fonte de variável OpenType é uma única fonte que pode se comportar como várias fontes usando interpolação contínua entre designs diferentes, tudo definido dentro da fonte única.

Uma fonte de variável OpenType pode definir a variação contínua de seu design ao longo de um ou mais eixos independentes, como peso ou largura: 

 

![Mostra uma fonte de variável OpenType usando a letra 'G' e mostrando variações diferentes ao longo de um eixo de largura horizontal e um eixo de peso vertical.](images/opentype-width-weight.png)

Um desenvolvedor de fontes determina um conjunto de eixos de variação a ser usado em uma determinada fonte. Esses eixos podem incluir um conjunto de eixos de variação conhecidos (ou "registrados"), como peso e largura, mas também podem incluir eixos arbitrários e personalizados de variação definidos pelo desenvolvedor de fontes.  

Ao selecionar um conjunto de eixos de variação para uma fonte, o desenvolvedor de fontes define um espaço abstrato e ndimensional de variação de design para a fonte. Os mecanismos de texto podem especificar potencialmente qualquer posição, ou "instância", dentro desse espaço contínuo para definir e renderizar texto. 

O desenvolvedor de fontes também pode selecionar e atribuir nomes a instâncias específicas dentro do espaço de variação de design; eles são chamados de "instâncias nomeadas". Por exemplo, uma fonte com variação de peso pode dar suporte à variação contínua entre traços muito leves e muito pesados, enquanto o desenvolvedor da fonte selecionou pesos específicos ao longo desse continuum e atribuiu nomes a eles, como "Light", "Regular" e "Semiabold". 

O formato de fonte da variável OpenType usa tabelas de dados encontradas em fontes OpenType tradicionais, além de determinadas tabelas adicionais que descrevem como os valores de vários itens de dados mudam para instâncias diferentes. O formato designa uma instância de variação como uma "instância padrão", que usa tabelas tradicionais para obter valores padrão. Todas as outras instâncias dependem dos dados padrão mais de outros dados delta. Por exemplo, uma tabela 'glifo' pode ter uma descrição de curva de Bezier de uma forma de glifo nominal, que é a forma usada para a instância padrão, enquanto uma tabela 'gvar' descreverá como os pontos de controle Bezier para o glifo são ajustados para outras instâncias. Da mesma forma, outros valores de fonte podem ter um valor nominal mais dados delta que descrevem como esses valores mudam para instâncias diferentes; por exemplo, altura x e outras métricas de toda a fonte ou posições de ancoragem de marca e ajuste de glifo específicos. 

Como as fontes variáveis podem dar suporte a um conjunto arbitrário de eixos de variação, elas exigem um modelo extensível de famílias de fontes que reflete mais diretamente como os designers de fonte criam famílias de fontes: uma família de fontes é definida por um nome de família e determinadas características de design constantes, com um número arbitrário (determinado pelo desenvolvedor da fonte) de maneiras pelas quais o design pode variar. Uma família de fontes pode ser criada com variantes para peso, mas uma família de fontes diferente pode ser criada com variantes para altura x, tamanho de serif, "cuidado" ou o que o desenvolvedor da fonte desejar. Nesse modelo, uma seleção de face de fonte é melhor descrita usando o nome da família geral ou "preferencial" ou "tipográfico", além de um conjunto de pares chave-valor, cada um representando um tipo de variação e um valor específico, com os tipos de variação em geral sendo um conjunto extensível. Essa noção geral de uma família de fontes pode se aplicar a fontes tradicionais e não variáveis, bem como a fontes variáveis. Por exemplo, nesse modelo geral de família tipográfica, uma família "Selawik VF" pode ter variações de peso, tamanho óptico e design de serif, com instâncias como "Semlight Banner Sans". 

Algumas implementações de software existentes, no entanto, incluindo APIs de DirectWrite existentes, podem ser projetadas supondo um modelo mais limitado de famílias de fontes. Por exemplo, alguns aplicativos podem assumir que uma família de fontes pode ter, no máximo, variantes regulares, em negrito, itálico e negrito. As interfaces existentes [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) assumem um modelo de família de peso/stretch/style ("WSS"), permitindo que variantes em uma família sejam especificadas usando as enumerações [**DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) ou [**DWRITE \_ FONT \_ STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) como parâmetros. No exemplo anterior, os eixos de tamanho óptico e serif não seriam tratados como eixos de variação internos da família WSS modelo. 

O suporte completo para fontes variáveis exigiria APIs que permitem que um membro da família seja especificado com potencialmente vários parâmetros, conforme determinado pela fonte. Mas designs de API existentes podem ser capazes de fornecer suporte parcial para fontes variáveis projetando as instâncias nomeadas definidas em uma fonte variável nos modelos de família de fontes mais limitados. No exemplo anterior, "Serikik VF Semilight Banner Sans" poderia ser projetado no modelo WSS como uma família de "Sans de Faixa de VF senikik" com "Semilight" como uma variante de peso. 

Para outro exemplo, considere uma família de fontes tipográficas, como Sitka, com variantes de peso e tamanho óptico. As variantes nomeadas dentro da família incluem Sitka Text Regular e Sitka Banner Bold (além de muitos outros). O nome da família tipográfica é "Sitka", enquanto os nomes de rosto dessas variantes no modelo de família tipográfica seriam "Texto Regular" e "Banner Negrito". Os modelos de família de quatro membros e WSS não permitem variantes de tamanho óptico em uma família e, portanto, as distinções de tamanho óptico devem ser tratadas como distinções no nível da família. A tabela a seguir ilustra como uma seleção de fontes da família tipográfica Sitka seria tratada no modelo WSS família: 



Modelo de família tipográfica

WSS de família

Família

Face

Família

Face

Sitka

Texto Regular

Texto sitka

Regular

Sitka

Faixa em negrito

Faixa sitka

Negrito

Sitka

Legenda itálico

Legenda de Sitka

Itálico



 

A projeção de nomes de um modelo de família tipográfica para o modelo de família WSS pode ser aplicada a fontes não variáveis e às instâncias nomeadas de fontes variáveis. No entanto, isso não pode ser feito para outras instâncias não nomeadas do espaço de variação de design contínuo de uma fonte variável. Por esse motivo, o suporte para a funcionalidade completa de fontes variáveis exigirá APIs projetadas para referenciar rostos dentro de uma família tipográfica em termos de um conjunto irr pouco restrito de eixos de variação e valores de eixo. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Suporte à fonte de variável OpenType DirectWrite

A partir do lançamento do Atualização do Windows 10 para Criadores, o formato de fonte da variável OpenType ainda é muito novo e fornecedores de fontes, plataformas e aplicativos ainda estão em processo de implementação do novo formato. Essa atualização fornece a implementação inicial para esse formato DirectWrite. 

DirectWrite internos foram atualizados para dar suporte a fontes de variável OpenType. Usando APIs atuais, isso dá suporte a instâncias nomeadas de uma fonte variável. Esse suporte pode ser usado para fluxos de trabalho completos – desde a enumeração das instâncias nomeadas, a seleção de uma instância nomeada, o uso no layout e na formatação, até a renderização e impressão. Para o benefício de aplicativos que também usam a interop de texto GDI para determinadas operações, suporte semelhante também foi adicionado em APIs GDI existentes. 

No Atualização do Windows 10 para Criadores, DirectWrite dá suporte a instâncias arbitrárias que utilizam a funcionalidade de variação contínua de fontes variáveis.

Em muitas operações, o comportamento em DirectWrite instâncias nomeadas de uma fonte variável não pode ser diferenciado do comportamento de fontes não variáveis. E como o suporte é fornecido usando APIs DirectWrite existentes, as instâncias nomeadas de fontes variáveis podem até mesmo funcionar em muitos aplicativos DirectWrite existentes sem nenhuma alteração. No entanto, as exceções podem ser aplicadas em determinadas situações:  

-   Se um aplicativo processa dados de fonte diretamente para determinadas operações. Por exemplo, se um aplicativo ler dados de contorno de glifo diretamente do arquivo de fonte para criar determinados efeitos visuais.
-   Se um aplicativo usar uma biblioteca de terceiros para determinadas operações. Por exemplo, se um aplicativo usa DirectWrite para layout, para obter índices e posições de glifo finais, mas, em seguida, usa uma biblioteca de terceiros para renderização.
-   Se um aplicativo inserir dados de fonte em um documento ou de alguma outra maneira passar dados de fonte para um processo downstream.

Se as operações são executadas usando implementações que não suportam fontes variáveis, essas operações podem não produzir os resultados esperados. Por exemplo, as posições de glifo podem ser calculadas para uma instância nomeada da fonte variável, mas os glifos podem ser renderizados supondo uma instância nomeada diferente. Dependendo da implementação do aplicativo, os resultados podem funcionar em alguns contextos, mas não em outros contextos em que outras bibliotecas podem ser usadas. Por exemplo, o texto pode ser exibido corretamente na tela, mas não quando impresso. Se os fluxos de trabalho de ponta a ponta são implementados usando apenas DirectWrite, o comportamento correto para instâncias nomeadas de uma fonte variável pode ser esperado. 

Como as APIs de DirectWrite existentes suportam a seleção facial usando o modelo de peso/alongamento/estilo, as instâncias nomeadas de fontes que usam outros eixos de variação serão projetadas do modelo geral da família tipográfica para o modelo WSS, conforme descrito acima. Isso se baseia em uma fonte variável, incluindo uma tabela "atributos de estilo" ('STAT') com subtables de valor do eixo, que o DWrite usa para distinguir tokens de nome facial que designam atributos de peso, alongamento ou estilo de tokens que pertencem a outros eixos de variação.  

Se uma fonte variável não incluir uma tabela 'STAT', conforme necessário para fontes variáveis pela especificação OpenType, o DirectWrite tratará a fonte como uma fonte não variável que contém apenas a instância padrão.  

Se uma fonte contém uma tabela 'STAT', mas não inclui subtables de valor de eixo apropriadas, isso pode levar a resultados inesperados, como ter várias faces com nomes de rosto idênticos. Não há suporte para essas fontes no momento. 

A especificação OpenType permite que os dados de estrutura de contorno de glifo sejam representados em um dos dois formatos: usando uma tabela 'glifo', que usa o formato de estrutura e dica TrueType, ou usando uma tabela 'CFF', que usa a representação formato de fonte compacta ("CFF"). Em uma fonte variável com contornos trueType, a tabela 'glif' continua sendo usada e é complementada com uma tabela 'gvar' que fornece os dados de variação para os contornos. Isso significa que a instância padrão de uma fonte variável com contornos TrueType usa apenas tabelas OpenType tradicionais que terão suporte em softwares mais antigos que não têm suporte para fontes variáveis. No entanto, em uma fonte variável com contornos de CFF, a tabela 'CFF' é substituído pela tabela 'CFF2', que encapsula os dados de contorno padrão e os dados de variação associados em uma tabela. Os dados CFF são processados por um rasterizador separado do usado para dados TrueType, e uma tabela 'CFF2' requer um rasterizador CFF atualizado que tem suporte para 'CFF2'. Uma tabela 'CFF2' não pode ser processada por rasterizadores CFF mais antigos. Para uma fonte variável com dados de contorno CFF, isso significa que até mesmo a instância padrão não funcionará em softwares mais antigos. 

No Atualização do Windows 10 para Criadores, DirectWrite não dá suporte a fontes variáveis com dados de contorno CFF usando a tabela 'CFF2'. 

## <a name="using-opentype-variable-fonts"></a>Usando fontes de variável OpenType

As fontes de variável OpenType podem ser fáceis de usar, tendo em mente as limitações atuais mencionadas acima: 

-   Somente instâncias nomeadas de uma fonte variável têm suporte no momento.
-   Somente fontes variáveis que usam dados de contorno de glifo TrueType (não contornos de CFF) têm suporte no momento. 
-   para fontes que usam eixos de variação de design diferentes de peso, ampliação ou estilo, as instâncias nomeadas serão projetadas para o modelo de família de WSS, o que pode resultar em algumas instâncias nomeadas aparecendo como famílias separadas (como aconteceria no passado para fontes não variáveis). Para dar suporte a isso, as fontes de variáveis devem ter uma tabela ' STAT ' que inclua subtabelas de valor de eixo apropriadas.
-   as instâncias nomeadas de fontes de variáveis têm suporte em APIs DirectWrite, mas se determinadas operações forem executadas em implementações mais antigas que não dão suporte a fontes variáveis, elas poderão produzir resultados incorretos. 
-   determinadas APIs de DirectWrite usam as enumerações de [**\_ \_ espessura de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), [**DWRITE de \_ fonte \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) e DWRITE para especificar atributos de peso, ampliação e estilo ao selecionar faces. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) Se uma fonte de variável usar eixos de variação correspondentes, mas tiver muitas instâncias nomeadas que exigem granularidade mais fina, nem todas as instâncias nomeadas serão selecionáveis nessas APIs.

as fontes de variáveis opentype que estão em conformidade com esses requisitos podem ser instaladas do shell Windows assim como outras fontes OpenType e também podem ser usadas em conjuntos de fontes personalizados criados por um aplicativo.  

Quando instalado no sistema, todas as instâncias nomeadas de uma fonte de variável serão incluídas no conjunto de fontes retornado chamando o método IDWriteFontFamily3::[**GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) . observe que um conjunto de fontes é uma lista simples sem uma hierarquia de agrupamento de família, mas cada item no conjunto tem uma propriedade family-name baseada no modelo de família de WSS. O conjunto de fontes pode ser filtrado para uma determinada instância denominada de fonte de variável usando os métodos [**IDWriteFontSet:: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) . se estiver usando a sobrecarga **GetMatchingFonts** que usa um familyname, o familyname especificado deve usar o nome que está de acordo com o modelo de família de fontes WSS. a lista completa de nomes de família compatíveis com WSS que ocorrem em um conjunto de fontes pode ser obtida usando os métodos [**IDWriteFontSet:: getvalordapropriedades**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) usando o \_ \_ \_ \_ nome da família da ID de propriedade da fonte DWRITE \_ .  

Da mesma forma, todas as instâncias nomeadas de uma fonte de variável serão representadas na coleção de fontes retornada pelo método IDWriteFactory::[**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . como os elementos de uma coleção de fontes são famílias de fontes baseadas no modelo de WSS, as instâncias nomeadas de uma fonte de variável podem ser representadas em uma coleção como membros de duas ou mais famílias de fontes. se o método [**IDWriteFontCollection:: FindFamilyName**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) for usado, o parâmetro familyname deverá ser um nome de família compatível com WSS. para localizar todos os nomes de família compatíveis com WSS de uma coleção de fontes, um aplicativo pode executar um loop em cada família e chamar [**IDWriteFontFamily:: getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames), embora possa ser mais fácil obter um conjunto de fontes correspondente e usar o método [**getvalordapropriedades**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) , conforme descrito acima. 

Ao trabalhar com fontes personalizadas, várias abordagens descritas no tópico [conjuntos de fontes personalizadas](custom-font-sets-win10.md) podem ser usadas para criar um conjunto de fontes. Para adicionar uma fonte variável a um conjunto de fontes personalizadas, o método [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) é recomendado, pois oferece suporte a fontes variáveis e adicionará todas as instâncias nomeadas de uma fonte variável em uma única chamada. No momento, não há como adicionar instâncias nomeadas individuais de uma fonte de variável personalizada a um conjunto de fontes usando os métodos [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , uma vez que não há como criar uma referência de face de fonte especificando quais das instâncias nomeadas de um arquivo de fonte variável é pretendida. Isso significa que atualmente não há como adicionar instâncias nomeadas de uma fonte personalizada a um conjunto de fontes personalizadas com propriedades personalizadas atribuídas. isso, por sua vez, significa que as fontes de variáveis personalizadas atualmente não podem ser usadas facilmente em conjunto com as APIs DirectWrite para fontes remotas. Se as instâncias nomeadas de uma fonte de variável forem incluídas em um conjunto de fontes do sistema, no entanto, as referências de face de fonte para cada instância nomeada já existirão e poderão ser adicionadas a conjuntos de fontes personalizados, incluindo com o uso de valores de propriedade personalizados. Consulte o tópico conjuntos de fontes personalizadas para obter mais detalhes. 

ao trabalhar com fontes de variáveis, as enumerações de DWRITE de fontes e DWRITE de [**\_ \_ espessura**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) de fonte de subDirectWrites estão diretamente conectadas aos eixos de variação de peso e largura definidos na especificação OpenType, mas não são iguais. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) Primeiro, a escala numérica para qualquer eixo de variação sempre dá suporte a valores fracionários, enquanto EspessuraDaFonte e fontStretch usam inteiros. A escala do eixo de peso OpenType usa valores variando de 1 a 1000, que também tem suporte em EspessuraDaFonte. Assim, a alteração de um valor de eixo de peso de variação para EspessuraDaFonte é relativamente pequena: a EspessuraDaFonte relatada para uma instância nomeada pode ser arredondada do valor exato usado para definir a instância nomeada dentro da fonte. a distinção entre DirectWrite fontStretch e a escala do eixo de largura OpenType é maior: DirectWrite usa valores de 1 a 9, seguindo os valores de [usWidthClass](/typography/opentype/spec/os2#uswidthclass) da tabela do sistema operacional opentype/2, enquanto a escala do eixo de largura opentype usa valores positivos que representam uma porcentagem da largura normal. A documentação do [usWidthClass](/typography/opentype/spec/os2#uswidthclass) na especificação de OpenType fornece um mapeamento entre os valores de 1 a 9 e a porcentagem de valores normais. O valor fontStretch relatado para uma instância nomeada pode envolver arredondamento ao converter de valores de eixo de largura. 

ao criar um [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), uma coleção de fontes e propriedades de fonte compatíveis com WSS (nome de família, peso, ampliação e estilo) devem ser especificadas. Isso também se aplica ao definir propriedades de formatação de fonte em um intervalo de texto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . As propriedades podem ser obtidas de um objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) ou de objetos [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) que representam uma determinada instância nomeada. como observado acima, os valores retornados pelos métodos getweight e getstretch podem ser aproximações arredondadas para os valores reais do eixo usados para definir a instância nomeada, mas DirectWrite mapeará a combinação de propriedades de volta para a instância nomeada desejada. 

da mesma forma, se um aplicativo usar [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) para criar dados de fallback de fonte personalizada, as famílias serão especificadas para mapeamentos de intervalo de caracteres usando nomes de família compatíveis com WSS. o fallback de fonte dentro de DirectWrite baseia-se em famílias com DirectWrite selecionando uma variante em uma família de fallback que seja uma correspondência mais próxima para a variante da família inicial. para variantes que envolvem dimensões que não sejam peso, ampliação e estilo, DirectWrite no momento não seriam capazes de selecionar essas variantes em uma família de fallback, a menos que os dados de fallback personalizados tenham sido criados especificamente para fornecer mapeamentos de fallback para famílias que têm atributos não WSS específicos, como variantes de tamanho óptico "Caption".

 

 