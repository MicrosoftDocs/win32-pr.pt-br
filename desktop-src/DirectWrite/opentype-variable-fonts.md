---
title: Fontes variáveis OpenType
description: Este tópico descreve as fontes de variáveis OpenType, seu suporte no DirectWrite e Direct2D e como usá-las em seu aplicativo. .
ms.assetid: 788558a7-efe7-b075-942f-ac75a5b86b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a9e6bdf27da0d70841973515636736859294dd
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2021
ms.locfileid: "103837554"
---
# <a name="opentype-variable-fonts"></a>Fontes variáveis OpenType

Este tópico descreve as fontes de variáveis OpenType, seu suporte no DirectWrite e Direct2D e como usá-las em seu aplicativo. 

-   [O que são fontes de variáveis OpenType?](#what-are-opentype-variable-fonts)
-   [Suporte à fonte de variáveis OpenType em DirectWrite](#opentype-variable-font-support-in-directwrite)
-   [Usando fontes de variáveis OpenType](#using-opentype-variable-fonts)

## <a name="what-are-opentype-variable-fonts"></a>O que são fontes de variáveis OpenType?

A versão 1,8 da [especificação de formato de fonte OpenType](https://www.microsoft.com/typography/otspec/) introduziu uma nova extensão para o formato conhecido como [variações de fontes OpenType](/typography/opentype/spec/otvaroverview). As fontes que usam essas extensões são conhecidas como fontes de variáveis OpenType. Uma fonte de variável OpenType é uma fonte única que pode se comportar como várias fontes usando a interpolação contínua entre diferentes designs, todas definidas dentro da única fonte.

Uma fonte de variável OpenType pode definir a variação contínua de seu design ao longo de um ou mais eixos independentes, como peso ou largura: 

 

![Mostra uma fonte de variável OpenType usando a letra "G" e mostrando diferentes variações ao longo de um eixo de largura horizontal e um eixo de peso vertical.](images/opentype-width-weight.png)

Um desenvolvedor de fontes determina um conjunto de eixos de variação a ser usado em uma determinada fonte. Esses eixos podem incluir um conjunto de eixos bem conhecidos (ou "registrados") de variação, como peso e largura, mas também podem incluir eixos personalizados e arbitrários de variação definidos pelo desenvolvedor de fontes.  

Ao selecionar um conjunto de eixos de variação para uma fonte, o desenvolvedor de fontes define um espaço n-dimensional abstrato de variação de design para a fonte. Os mecanismos de texto podem especificar potencialmente qualquer posição, ou "instância", dentro desse espaço contínuo para dispor e renderizar texto. 

O desenvolvedor de fontes também pode selecionar e atribuir nomes a instâncias específicas dentro do espaço de variação de design; Eles são chamados de "instâncias nomeadas". Por exemplo, uma fonte com variação de peso pode dar suporte à variação contínua entre traços muito leves e muito pesados, enquanto o desenvolvedor de fontes selecionou pesos específicos ao longo da continuidade e atribuiu nomes a eles, como "Light", "regular" e "seminegrito". 

O formato de fonte da variável OpenType usa tabelas de dados encontradas em fontes OpenType tradicionais, além de determinadas tabelas adicionais que descrevem como os valores de vários itens de dados são alterados para diferentes instâncias. O formato designa uma instância de variação como uma "instância padrão", que usa tabelas tradicionais para obter valores padrão. Todas as outras instâncias dependem dos dados padrão e outros dados Delta. Por exemplo, uma tabela ' glyf ' pode ter uma descrição de curva de Bézier de uma forma de glifo nominal, que é a forma usada para a instância padrão, enquanto uma tabela ' GVAR ' descreverá como os pontos de controle de Bézier para o glifo são ajustados para outras instâncias. Da mesma forma, outros valores de fonte podem ter um valor nominal mais dados Delta que descrevem como esses valores são alterados para diferentes instâncias; por exemplo, altura x e outras métricas de toda a fonte, ou posições de marca de ancoragem específicas de glifo e ajustes de kerning. 

Como as fontes de variáveis podem dar suporte a um conjunto arbitrário de eixos de variação, elas exigem um modelo extensível de famílias de fontes que refletem mais diretamente como os designers de fontes criam famílias de fontes: uma família de fontes é definida por um nome de família e determinadas características de design que são constantes, com um número arbitrário (determinado pelo desenvolvedor de fontes) de maneiras em que o design Uma família de fontes pode ser criada com variantes para peso, mas uma família de fontes diferente pode ser criada com variantes para x-height, serif, tamanho, "funkiness" ou qualquer que seja o desenvolvedor da fonte. Nesse modelo, uma seleção de face de fonte é melhor descrita usando o geral, ou "preferencial" ou "tipográfico", o nome da família, além de um conjunto de pares chave-valor, cada um representando um tipo de variação e valor específico, com os tipos de variação em geral sendo um conjunto extensível. Essa noção geral de uma família de fontes pode se aplicar a fontes tradicionais e não variáveis, bem como a fontes variáveis. Por exemplo, neste geral, o modelo de família tipográfica, uma família "Selawik VF" pode ter variações de peso, tamanho óptico e design de serif, com instâncias como "SANs de faixa Semilight". 

No entanto, algumas implementações de software existentes, incluindo APIs DirectWrite existentes, podem ser projetadas supondo-se um modelo mais limitado de famílias de fontes. Por exemplo, alguns aplicativos podem assumir que uma família de fontes pode ter, no máximo, as variantes comuns, em negrito, itálico e negrito em itálico. As interfaces [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) existentes pressupõem um modelo de família de peso/Stretch/estilo ("WSS"), permitindo que as variantes dentro de uma família sejam especificadas usando o [**\_ \_ peso da fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), DWRITE as enumerações de [**fonte de \_ \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) ou DWRITE como parâmetros. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) Ao fazer o exemplo anterior, os eixos de tamanho óptico e de serifa não seriam tratados como eixos internos da família de variação no modelo do WSS. 

O suporte completo para fontes variáveis exigiria APIs que permitissem que um membro da família fosse especificado com potencialmente vários parâmetros, conforme determinado pela fonte. Mas os designs de API existentes podem ser capazes de fornecer suporte parcial para fontes variáveis projetando as instâncias nomeadas definidas em uma fonte variável nos modelos mais limitados da família de fontes. No exemplo anterior, "Selawik VF Semilight Banner" Sans "poderia ser projetado para o modelo do WSS como uma família" Selawik VF banner Sans "com" Semilight "como uma variante de peso. 

Para outro exemplo, considere uma família de fontes tipográficas, como Sitka, com variantes de tamanho óptico e peso. As variantes nomeadas na família incluem texto Sitka regular e Sitka banner em negrito (além de muitos outros). O nome da família tipográfica é "Sitka", enquanto os nomes de face para essas variantes no modelo de família tipográfica seriam "Text regular" e "Banner bold". Os modelos de quatro membros e da família WSS não permitem variantes de tamanho óptico dentro de uma família e, portanto, distinções de tamanho óptico devem ser tratadas como distinções de nível de família. A tabela a seguir ilustra como uma seleção de fontes da família tipográfica Sitka seria tratada no modelo da família WSS: 



Modelo de família tipográfica

Modelo da família WSS

Família

Detecção Facial

Família

Detecção Facial

Sitka

Texto regular

Texto Sitka

Regular

Sitka

Faixa em negrito

Faixa Sitka

Negrito

Sitka

Legenda em itálico

Legenda Sitka

Itálico



 

A projeção de nomes de um modelo de família tipográfica para o modelo de família do WSS pode ser aplicada a fontes não variáveis e às instâncias nomeadas de fontes de variáveis. No entanto, isso não pode ser feito para outras instâncias não nomeadas do espaço de variação de design contínuo de uma fonte variável. Por esse motivo, o suporte para a funcionalidade completa de fontes variáveis exigirá que as APIs sejam criadas para referenciar rostos em uma família tipográfica em termos de um conjunto irrestrito de eixos de variação e valores de eixo. 

## <a name="opentype-variable-font-support-in-directwrite"></a>Suporte à fonte de variáveis OpenType em DirectWrite

No lançamento da atualização do Windows 10 para criadores, o formato de fonte da variável OpenType ainda é muito novo, e fornecedores de fontes, plataformas e aplicativos ainda estão no processo de implementação do novo formato. Esta atualização fornece a implementação inicial para esse formato no DirectWrite. 

Os internos do DirectWrite foram atualizados para dar suporte a fontes de variáveis OpenType. Usando as APIs atuais, isso fornece suporte para quaisquer instâncias nomeadas de uma fonte variável. Esse suporte pode ser usado para fluxos de trabalho completos — da enumeração das instâncias nomeadas, da seleção de uma instância nomeada, do uso em layout e formatação, à renderização e à impressão. Para o benefício dos aplicativos que também usam a interoperabilidade de texto GDI para determinadas operações, o suporte semelhante também foi adicionado em APIs GDI existentes. 

Na atualização do Windows 10 para criadores, o DirectWrite não oferece suporte a instâncias arbitrárias que utilizam o recurso de variação contínua de fontes de variáveis.

Em muitas operações, o comportamento em DirectWrite de instâncias nomeadas de uma fonte de variável não pode ser diferenciado do comportamento de fontes não variáveis. E como o suporte é fornecido usando APIs DirectWrite existentes, as instâncias nomeadas de fontes de variáveis podem até mesmo trabalhar em muitos aplicativos DirectWrite existentes sem nenhuma alteração. No entanto, as exceções podem ser aplicadas em determinadas situações:  

-   Se um aplicativo processar dados de fonte diretamente para determinadas operações. Por exemplo, se um aplicativo lê dados de estrutura de tópicos de glifo diretamente do arquivo de fonte para criar determinados efeitos visuais.
-   Se um aplicativo usar uma biblioteca de terceiros para determinadas operações. Por exemplo, se um aplicativo usa DirectWrite para layout, para obter os índices de glifo e as posições finais, mas usa uma biblioteca de terceiros para renderização.
-   Se um aplicativo inserir dados de fonte em um documento ou de alguma outra maneira passar os dados da fonte para um processo downstream.

Se as operações forem executadas usando implementações que não dão suporte a fontes variáveis, essas operações poderão não produzir os resultados esperados. Por exemplo, as posições de glifo podem ser calculadas para uma instância nomeada da fonte variável, mas os glifos podem ser renderizados supondo uma instância nomeada diferente. Dependendo da implementação do aplicativo, os resultados podem funcionar em alguns contextos, mas não em outros contextos nos quais outras bibliotecas podem ser usadas. Por exemplo, o texto pode ser exibido corretamente na tela, mas não quando impresso. Se os fluxos de trabalho de ponta a ponta forem implementados usando apenas DirectWrite, o comportamento correto para instâncias nomeadas de uma fonte variável poderá ser esperado. 

Como as APIs DirectWrite existentes dão suporte à seleção de face usando o modelo de peso/Stretch/estilo, as instâncias nomeadas de fontes que usam outros eixos de variação serão projetadas do modelo de família tipográfica geral para o modelo do WSS, conforme descrito acima. Isso depende de uma fonte variável, incluindo uma tabela "atributos de estilo" (' STAT ') com subtabelas de valor de eixo, que o DWrite usa para distinguir tokens de nome de face que designam atributos de peso, ampliação ou estilo de tokens que pertencem a outros eixos de variação.  

Se uma fonte de variável não incluir uma tabela ' STAT ', conforme necessário para fontes de variáveis pela especificação OpenType, DirectWrite tratará a fonte como uma fonte não variável contendo apenas a instância padrão.  

Se uma fonte contiver uma tabela ' STAT ', mas não incluir subtabelas de valor do eixo apropriado, isso poderá levar a resultados inesperados, como ter várias faces que têm nomes de face idênticos. Essas fontes não têm suporte no momento. 

A especificação OpenType permite que os dados de estrutura de tópicos de glifo sejam representados em um dos dois formatos: usando uma tabela ' glyf ', que usa a estrutura de tópicos TrueType e o formato de dica, ou usando uma tabela ' CFF ', que usa a representação de formato de fonte compacto ("CFF"). Em uma fonte variável com contornos TrueType, a tabela ' glyf ' continua sendo usada e é complementada com uma tabela ' GVAR ' que fornece os dados de variação para os contornos. Isso significa que a instância padrão de uma fonte variável com contornos TrueType usa apenas tabelas OpenType tradicionais que terão suporte em softwares mais antigos que não têm suporte à fonte variável. No entanto, em uma fonte variável com contornos CFF, a tabela ' CFF ' é substituída pela tabela ' CFF2 ', que encapsula os dados de estrutura de tópicos padrão e os dados de variação associados em uma tabela. Os dados CFF são processados por um rasterizador separado do usado para dados TrueType, e uma tabela ' CFF2 ' requer um rasterizador CFF atualizado com suporte a ' CFF2 '. Uma tabela ' CFF2 ' não pode ser processada por rasterizadores CFF mais antigos. Para uma fonte variável com dados de estrutura de tópicos CFF, isso significa que até mesmo a instância padrão não funcionará em software mais antigo. 

Na atualização do Windows 10 para criadores, o DirectWrite não oferece suporte a fontes variáveis com dados de estrutura de tópicos CFF usando a tabela ' CFF2 '. 

## <a name="using-opentype-variable-fonts"></a>Usando fontes de variáveis OpenType

As fontes de variáveis OpenType podem ser fáceis de usar, tendo em mente as limitações atuais indicadas acima: 

-   No momento, só há suporte para instâncias nomeadas de uma fonte variável.
-   Somente as fontes variáveis que usam dados de estrutura de tópicos de glifo TrueType (não contornos CFF) têm suporte no momento. 
-   Para fontes que usam eixos de variação de design diferentes de peso, ampliação ou estilo, as instâncias nomeadas serão projetadas no modelo da família WSS, o que pode resultar em algumas instâncias nomeadas aparecendo como famílias separadas (como ocorreria no passado para fontes não variáveis). Para dar suporte a isso, as fontes de variáveis devem ter uma tabela ' STAT ' que inclua subtabelas de valor de eixo apropriadas.
-   Há suporte para instâncias nomeadas de fontes de variáveis em APIs DirectWrite, mas se determinadas operações forem executadas em implementações mais antigas que não dão suporte a fontes variáveis, elas poderão produzir resultados incorretos. 
-   Determinadas APIs DirectWrite usam as enumerações de [**\_ \_ espessura de fonte DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight), DWRITE de fonte e DWRITE para especificar os atributos de peso, ampliação e estilo ao selecionar faces. [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) [**\_ \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style) Se uma fonte de variável usar eixos de variação correspondentes, mas tiver muitas instâncias nomeadas que exigem granularidade mais fina, nem todas as instâncias nomeadas serão selecionáveis nessas APIs.

As fontes de variáveis OpenType que estão em conformidade com esses requisitos podem ser instaladas a partir do shell do Windows, assim como outras fontes OpenType, e também podem ser usadas em conjuntos de fontes personalizados criados por um aplicativo.  

Quando instalado no sistema, todas as instâncias nomeadas de uma fonte de variável serão incluídas no conjunto de fontes retornado chamando o método IDWriteFontFamily3::[**GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) . Observe que um conjunto de fontes é uma lista simples sem uma hierarquia de agrupamento de família, mas cada item no conjunto tem uma propriedade Family-Name baseada no modelo da família WSS. O conjunto de fontes pode ser filtrado para uma determinada instância denominada de fonte de variável usando os métodos [**IDWriteFontSet:: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) . Se estiver usando a sobrecarga **GetMatchingFonts** que usa um familyName, o familyName especificado deve usar o nome que está de acordo com o modelo da família de fontes do WSS. A lista completa de nomes de família compatíveis com o WSS que ocorre em um conjunto de fontes pode ser obtida usando os métodos [**IDWriteFontSet:: Getvalordapropriedades**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) usando o \_ \_ \_ \_ nome da família da ID de propriedade da fonte DWRITE \_ .  

Da mesma forma, todas as instâncias nomeadas de uma fonte de variável serão representadas na coleção de fontes retornada pelo método IDWriteFactory::[**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Como os elementos de uma coleção de fontes são famílias de fontes baseadas no modelo do WSS, as instâncias nomeadas de uma fonte de variável podem ser representadas em uma coleção como membros de duas ou mais famílias de fontes. Se o método [**IDWriteFontCollection:: FindFamilyName**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-findfamilyname) for usado, o parâmetro familyName deverá ser um nome de família compatível com o WSS. Para localizar todos os nomes de família compatíveis com o WSS de uma coleção de fontes, um aplicativo pode executar um loop em cada família e chamar [**IDWriteFontFamily:: Getfamilynames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames), embora possa ser mais fácil obter um conjunto de fontes correspondente e usar o método [**getvalordapropriedades**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist)) , conforme descrito acima. 

Ao trabalhar com fontes personalizadas, várias abordagens descritas no tópico [conjuntos de fontes personalizadas](custom-font-sets-win10.md) podem ser usadas para criar um conjunto de fontes. Para adicionar uma fonte variável a um conjunto de fontes personalizadas, o método [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) é recomendado, pois oferece suporte a fontes variáveis e adicionará todas as instâncias nomeadas de uma fonte variável em uma única chamada. No momento, não há como adicionar instâncias nomeadas individuais de uma fonte de variável personalizada a um conjunto de fontes usando os métodos [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , uma vez que não há como criar uma referência de face de fonte especificando quais das instâncias nomeadas de um arquivo de fonte variável é pretendida. Isso significa que atualmente não há como adicionar instâncias nomeadas de uma fonte personalizada a um conjunto de fontes personalizadas com propriedades personalizadas atribuídas. Isso, por sua vez, significa que as fontes de variáveis personalizadas atualmente não podem ser usadas facilmente em conjunto com as APIs DirectWrite para fontes remotas. Se as instâncias nomeadas de uma fonte de variável forem incluídas em um conjunto de fontes do sistema, no entanto, as referências de face de fonte para cada instância nomeada já existirão e poderão ser adicionadas a conjuntos de fontes personalizados, incluindo com o uso de valores de propriedade personalizados. Consulte o tópico conjuntos de fontes personalizadas para obter mais detalhes. 

Ao trabalhar com fontes de variáveis, as enumerações de [**\_ \_ espessura**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight) de fonte DirectWrite DWRITE e [**DWRITE de \_ \_ Stretch de fonte**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch) estão diretamente conectadas aos eixos de variação de peso e largura definidos na especificação OpenType, mas não são as mesmas. Primeiro, a escala numérica para qualquer eixo de variação sempre dá suporte a valores fracionários, enquanto EspessuraDaFonte e fontStretch usam inteiros. A escala do eixo de peso OpenType usa valores variando de 1 a 1000, que também tem suporte em EspessuraDaFonte. Assim, a alteração de um valor de eixo de peso de variação para EspessuraDaFonte é relativamente pequena: a EspessuraDaFonte relatada para uma instância nomeada pode ser arredondada do valor exato usado para definir a instância nomeada dentro da fonte. A distinção entre DirectWrite fontStretch e a escala do eixo de largura OpenType é maior: DirectWrite usa valores de 1 a 9, seguindo os valores de [usWidthClass](/typography/opentype/spec/os2#uswidthclass) da tabela do sistema operacional OpenType/2, enquanto a escala do eixo de largura OpenType usa valores positivos que representam uma porcentagem da largura normal. A documentação do [usWidthClass](/typography/opentype/spec/os2#uswidthclass) na especificação de OpenType fornece um mapeamento entre os valores de 1 a 9 e a porcentagem de valores normais. O valor fontStretch relatado para uma instância nomeada pode envolver arredondamento ao converter de valores de eixo de largura. 

Ao criar um [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat), uma coleção de fontes e as propriedades de fonte compatíveis com o WSS (nome da família, peso, ampliação e estilo) devem ser especificadas. Isso também se aplica ao definir propriedades de formatação de fonte em um intervalo de texto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . As propriedades podem ser obtidas de um objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) ou de objetos [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) e [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) que representam uma determinada instância nomeada. Como observado acima, os valores retornados pelos métodos getweight e getstretch podem ser aproximações arredondadas para os valores reais do eixo usados para definir a instância nomeada, mas DirectWrite mapeará a combinação de propriedades de volta para a instância nomeada desejada. 

Da mesma forma, se um aplicativo usar [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) para criar dados de fallback de fonte personalizada, as famílias serão especificadas para mapeamentos de intervalo de caracteres usando nomes de família compatíveis com o WSS. O fallback de fonte no DirectWrite é baseado em famílias com DirectWrite selecionando uma variante em uma família de fallback que é uma correspondência mais próxima para a variante da família inicial. Para variantes que envolvem dimensões que não sejam peso, Stretch e Style, DirectWrite atualmente não conseguiria selecionar essas variantes em uma família de fallback, a menos que os dados de fallback personalizados fossem criados especificamente para fornecer mapeamentos de fallback para famílias que têm atributos não WSS específicos, como variantes de tamanho óptico de "Caption".

 

 