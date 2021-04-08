---
title: Apresentando o DirectWrite
description: As pessoas se comunicam com o texto o tempo todo em suas vidas diárias.
ms.assetid: ec7cc4a3-b925-48dc-920f-fd293b4c69f0
keywords:
- DirectWrite, sobre
- DirectWrite, recursos tipográficos
- tipografia
- DirectWrite, texto internacional
- DirectWrite, fontes OpenType
- Fontes OpenType
- DirectWrite, ClearType
- ClearType
- DirectWrite, visão geral da API
- DirectWrite, IDWriteFontFace
- IDWriteFontFace
- DirectWrite, renderização de texto
- DirectWrite, modos de renderização
- Interoperação DirectWrite, GDI
- DirectWrite, interoperabilidade
- interoperabilidade, DirectWrite
- interoperabilidade, Graphics Device Interface (GDI)
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4064feccbdbc03f4b2e4d0118e5ab704013d314e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823960"
---
# <a name="introducing-directwrite"></a>Apresentando o DirectWrite

As pessoas se comunicam com o texto o tempo todo em suas vidas diárias. É a principal maneira para as pessoas consumirem um volume cada vez maior de informações. Antigamente, costumava ser por meio de conteúdo impresso, principalmente documentos, jornais, livros e assim por diante. Cada vez mais, é conteúdo online em seu computador Windows. Um usuário típico do Windows gasta muito tempo lendo na tela do computador. Eles podem estar navegando na Web, verificando emails, compondo um relatório, preenchendo uma planilha ou escrevendo software, mas o que eles estão realmente fazendo é ler. Embora o texto e as fontes percarnem praticamente todas as partes da experiência do usuário no Windows, para a maioria dos usuários, a leitura na tela não é tão agradável quanto a leitura da saída impressa.

Para desenvolvedores de aplicativos Windows, escrever código de manipulação de texto é um desafio devido aos maiores requisitos para melhor legibilidade, formatação sofisticada e controle de layout e suporte para os vários idiomas que o aplicativo deve exibir. Até mesmo o sistema de manipulação de texto mais básico deve permitir entrada de texto, layout, exibição, edição e cópia e colagem. Os usuários do Windows normalmente esperam ainda mais do que esses recursos básicos, exigindo até mesmo editores simples para dar suporte a várias fontes, vários estilos de parágrafo, imagens inseridas, verificação ortográfica e outros recursos. O design da interface do usuário moderna também não é mais refinado para formato único, texto sem formatação, mas precisa apresentar uma experiência melhor com fontes avançadas e layouts de texto.

Esta é uma introdução ao modo como o [DirectWrite](direct-write-portal.md) permite que os aplicativos do Windows aprimorem a experiência de texto para a interface do usuário e documentos.

## <a name="improving-the-text-experience"></a>Melhorando a experiência de texto

Os aplicativos modernos do Windows têm requisitos sofisticados de texto em sua interface do usuário e documentos. Isso inclui melhor legibilidade, suporte para uma grande variedade de linguagens e scripts e desempenho de renderização superior. Além disso, a maioria dos aplicativos existentes exige uma maneira de postergar os investimentos existentes na base de código WindowsWin32.

O [DirectWrite](direct-write-portal.md) fornece os três recursos a seguir que permitem que os desenvolvedores de aplicativos do Windows aprimorem a experiência de texto em seus aplicativos: independência do sistema de renderização, tipografia de alta qualidade e várias camadas de funcionalidade.

## <a name="rendering-system-independence"></a>Independência de Rendering-System

O [DirectWrite](direct-write-portal.md) é independente de qualquer tecnologia gráfica específica. Os aplicativos são livres para usar a tecnologia de renderização mais adequada às suas necessidades. Isso dá aos aplicativos a flexibilidade para continuar renderizando algumas partes de seu aplicativo por meio do GDI e de outras partes por meio do Direct3D ou do [Direct2D](../direct2d/direct2d-portal.md). Na verdade, um aplicativo poderia optar por renderizar DirectWrite por meio de uma pilha de renderização proprietária.

## <a name="high-quality-typography"></a>Tipografia de High-Quality

O [DirectWrite](direct-write-portal.md) aproveita os avanços na tecnologia de fonte [OpenType](../intl/opentype-font-format.md) para habilitar a tipografia de alta qualidade em um aplicativo do Windows. O sistema de fontes DirectWrite fornece serviços para lidar com a enumeração de fontes, o fallback de fontes e o cache de fontes, que são todos necessários por aplicativos para lidar com fontes.

O suporte a [OpenType](../intl/opentype-font-format.md) fornecido pelo [DirectWrite](direct-write-portal.md) permite que os desenvolvedores adicionem aos seus aplicativos recursos tipográficos avançados e suporte para texto internacional.

## <a name="support-for-advanced-typographic-features"></a>Suporte para recursos tipográficos avançados

O [DirectWrite](direct-write-portal.md) permite que os desenvolvedores de aplicativos desbloqueiem os recursos das fontes OpenType que não podiam usar em WinForms ou GDI. O objeto DirectWrite [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) expõe muitos dos recursos avançados das fontes OpenType, como alternativas estilísticos e traços violentos. O SDK (Software Development Kit) do Microsoft Windows fornece um conjunto de fontes [OpenType](../intl/opentype-font-format.md) de exemplo projetadas com recursos avançados, como as fontes Pericles e Pescadero. Para obter mais detalhes sobre os recursos do OpenType, consulte [recursos de fonte OpenType](/previous-versions/dotnet/netframework-3.0/ms745109(v=vs.85)).

## <a name="support-for-international-text"></a>Suporte para texto internacional

O [DirectWrite](direct-write-portal.md) usa fontes [OpenType](../intl/opentype-font-format.md) para habilitar amplo suporte para texto internacional. Há suporte para recursos Unicode, como substitutos, BIDI, quebra de linha e UVS. A discriminação de script guiada por idioma, a substituição de números e a modelagem de glifo garantem que o texto em qualquer script tenha o layout e a renderização corretos.

Os scripts a seguir tem suporte atualmente:

> [!Note]  
> Para scripts marcados com um \* , não há nenhuma fonte de sistema padrão. Os aplicativos devem instalar fontes que dão suporte a esses scripts.

 

-   Árabe
-   Armênia
-   Bengala
-   Bopomofo
-   Braille\*
-   Silábico canadense Aboriginal
-   Cherokee
-   Chinês (simplificado & tradicional)
-   Cirílico
-   Copta\*
-   Devanagari
-   Etíope
-   Georgiano
-   Letra\*
-   Grego
-   Guzerate
-   Gurmukhi
-   Hebraico
-   Japonês
-   canarim
-   Khmer
-   Coreano
-   Lao
-   Latim
-   Malaiala
-   Mongol
-   Myanmar
-   Tai Lue Novo
-   Ogham\*
-   Oriá
-   ' Phags-pa
-   Rúnica\*
-   Sinhala
-   Siríaco
-   Tai Le
-   Tâmil
-   Télugo
-   Thaana
-   Tailandês
-   Tibetano
-   Yi

## <a name="multiple-layers-of-functionality"></a>Várias camadas de funcionalidade

O [DirectWrite](direct-write-portal.md) fornece camadas fatoradas de funcionalidade, com cada camada interagindo sem problemas com o próximo. O design de API oferece aos desenvolvedores de aplicativos a liberdade e a flexibilidade para adotar camadas individuais dependendo de suas necessidades e agendas. O diagrama a seguir mostra a relação entre essas camadas.

![diagrama de camadas DirectWrite e como eles se comunicam com um aplicativo ou estrutura de interface do usuário e a API de gráficos](images/intro-01.png)

A API de layout de texto fornece a funcionalidade de nível mais alto disponível em [DirectWrite](direct-write-portal.md). Ele fornece serviços para que o aplicativo meça, exiba e interaja com cadeias de caracteres de texto formatadas de formato avançado. Essa API de texto pode ser usada em aplicativos que atualmente usam o DrawText Win32's para criar uma interface do usuário moderna com texto formatado de formato rico.

Aplicativos com uso intensivo de texto que implementam seu próprio mecanismo de layout podem usar a próxima camada abaixo: o processador de script. O processador de script divide uma parte do texto em blocos de script e manipula o mapeamento entre representações Unicode para a representação de glifo apropriada na fonte, de modo que o texto do script possa ser exibido corretamente no idioma correto. O sistema de layout usado pela camada de API de layout de texto baseia-se na fonte e no sistema de processamento de scripts.

A camada de renderização de glifo é a camada mais baixa de funcionalidade e fornece a funcionalidade de renderização de glifo para aplicativos que implementam seu próprio mecanismo de layout de texto. A camada de renderização de glifo também é útil para aplicativos que implementam um renderizador personalizado para modificar o comportamento de desenho de glifo por meio da função de retorno de chamada na API de formatação de texto [DirectWrite](direct-write-portal.md) .

O sistema de fontes [DirectWrite](direct-write-portal.md) está disponível para todas as camadas funcionais do DirectWrite e permite que um aplicativo acesse informações de fonte e glifo. Ele foi projetado para lidar com tecnologias de fonte e formatos de dados comuns. O modelo de fonte DirectWrite segue a prática tipográfica comum de dar suporte a qualquer número de pesos, estilos e ampliações na mesma família de fontes. Esse modelo, o mesmo modelo seguido pelo WPF e o CSS, especifica que as fontes diferem apenas em peso (negrito, luz e assim por diante), estilo (vertical, itálico ou oblíquo) ou ampliação (estreito, condensada, largo e assim por diante) são considerados membros de uma única família de fontes.

### <a name="improved-text-rendering-with-cleartype"></a>Renderização de texto aprimorada com ClearType

Melhorar a legibilidade na tela é um requisito importante para todos os aplicativos do Windows. A evidência da pesquisa no cognitiva psicologia indica que precisamos ser capazes de reconhecer cada letra com precisão e que o espaçamento uniforme entre as letras é essencial para o processamento rápido. Letras e palavras que não são simétricas são percebidas como ruins e prejudicam a experiência de leitura. Kevin Larson, grupo de tecnologias de leitura avançada da Microsoft, escreveu um artigo sobre o assunto que foi publicado no espectro IEEE. O artigo é chamado "a tecnologia de texto" ( https://www.spectrum.ieee.org/print/5049) .

O texto em [DirectWrite](direct-write-portal.md) é renderizado usando o Microsoft ClearType, o que aumenta a clareza e a legibilidade do texto. O ClearType aproveita o fato de que monitores de LCD modernos têm faixas RGB para cada pixel que pode ser controlado individualmente. O DirectWrite usa os aprimoramentos mais recentes para o ClearType, primeiro incluído com o Windows Vista com Windows Presentation Foundation, que permite que ele avalie não apenas as letras individuais, mas também o espaçamento entre as letras. Antes desses aprimoramentos de ClearType, era difícil exibir um texto com um tamanho de "leitura" de 10 ou 12 pontos: poderíamos inserir 1 pixel entre letras, o que geralmente era muito pouco ou 2 pixels, o que geralmente era muito pequeno. O uso da resolução extra nos subpixels nos fornece espaçamento fracionário, o que melhora o uniformidade e a simetria da página inteira.

As duas ilustrações a seguir mostram como os glifos podem começar em qualquer limite de subpixel quando o posicionamento de subpixel é usado.

A ilustração a seguir é renderizada usando a versão GDI do renderizador ClearType, que não emprega o posicionamento de sub-pixel.

![ilustração de "tecnologia" renderizada sem posicionamento de sub-pixel](images/intro-03.png)

A ilustração a seguir é renderizada usando a versão [DirectWrite](direct-write-portal.md) do renderizador ClearType, que usa o posicionamento de sub-pixel.

![ilustração de "tecnologia" renderizada com posicionamento de subpixel](images/intro-04.png)

Observe que o espaçamento entre as letras h e n é mais uniforme na segunda imagem e a letra o é espaçada além da letra n, mais, mesmo com a letra l. Observe também como as hastes das letras l são mais naturais.

O posicionamento de ClearType em subpixel oferece o espaçamento mais preciso de caracteres na tela, especialmente em tamanhos pequenos, em que a diferença entre um sub-pixel e um pixel inteiro representa uma proporção significativa da largura do glifo. Ele permite que o texto seja medido no espaço de resolução ideal e renderizado em sua posição natural na faixa de cores do LCD, com granularidade de subpixel. O texto medido e renderizado usando essa tecnologia é, por definição, independente de resolução, o que significa que exatamente o mesmo layout de texto é obtido na faixa de várias resoluções de vídeo.

Ao contrário de qualquer tipo de renderização de ClearType do GDI, o recurso ClearType de sub-pixel oferece a largura de caracteres mais precisa.

A API de cadeia de caracteres de texto adota a renderização de texto sub-pixel por padrão, o que significa que ele mede o texto em sua resolução ideal, independentemente da resolução de vídeo atual, e produz o resultado de posicionamento de glifo com base nas larguras de adiantamento de glifos e deslocamentos de posicionamento verdadeiramente dimensionados.

Para texto de tamanho grande, o [DirectWrite](direct-write-portal.md) também permite suavização de serrilhado ao longo do eixo y para tornar as bordas mais suaves e renderizar as letras como o designer de fonte pretendido. A ilustração a seguir mostra a suavização de direção y.

![ilustração de "ClearType" renderizado como texto GDI e como texto DirectWrite com anti-aliasing na direção y](images/intro-05.png)

Embora o texto [DirectWrite](direct-write-portal.md) seja posicionado e processado usando o ClearType de sub-pixel por padrão, outras opções de renderização estão disponíveis. Muitos aplicativos existentes usam o GDI para renderizar a maior parte de sua interface do usuário e alguns aplicativos usam controles de edição do sistema que continuam a usar o GDI para a renderização de texto. Ao adicionar texto DirectWrite a esses aplicativos, pode ser necessário sacrificar os aprimoramentos da experiência de leitura fornecidos pelo ClearType em subpixel para que o texto tenha uma aparência consistente em todo o aplicativo.

Para atender a esses requisitos, o [DirectWrite](direct-write-portal.md) também dá suporte às seguintes opções de renderização:

-   ClearType de sub-pixel (padrão).
-   Subpixel ClearType com suavização de serrilhado nas dimensões horizontal e vertical.
-   Texto com alias.
-   Largura natural GDI (usada pelo Microsoft Word Modo de Exibição de Leitura, por exemplo).
-   Compatível com GDI-largura (incluindo bitmap do leste asiático Embedded).

Cada um desses modos de renderização pode ser ajustado por meio da API DirectWrite e do novo sintonizador ClearType da caixa de entrada do Windows 7.

> [!Note]  
> A partir do Windows 8, você deve usar a suavização de texto em escala de cinza na maioria dos casos. Para obter mais informações, confira a próxima seção.

 

### <a name="support-for-natural-layout"></a>Suporte para layout natural

O layout natural é independente de resolução, portanto, o espaçamento de caracteres não muda à medida que você amplia ou reduz, ou dependendo do DPI da tela. Uma vantagem secundária é que o espaçamento é verdadeiro para o design da fonte. O layout natural é possibilitado pelo suporte do DirectWrite para a renderização natural, o que significa que os glifos individuais podem ser posicionados em uma fração de um pixel.

Embora o layout natural seja o padrão, alguns aplicativos precisam renderizar texto com o mesmo espaçamento e aparência que o GDI. Para tais aplicativos, o DirectWrite fornece modos de medição natural do GDI e GDI clássico e modos de renderização correspondentes.

Qualquer um dos modos de renderização acima pode ser combinado com um dos dois modos de suavização: ClearType ou tons de cinza. As simulações de suavização ClearType têm uma resolução mais alta, manipulando individualmente os valores de cor vermelho, verde e azul de cada pixel. A suavização de escala de cinza computa apenas um valor de cobertura (ou alfa) para cada pixel. ClearType é o padrão, mas a suavização de tons de cinza é recomendada para aplicativos da Windows Store porque é mais rápida e é compatível com anti-aliasing padrão, ainda sendo altamente legível.

## <a name="api-overview"></a>Visão geral da API

A interface [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) é o ponto de partida para usar a funcionalidade DirectWrite. A fábrica é o objeto raiz que cria um conjunto de objetos que podem ser usados juntos.

A operação de formatação e layout é um pré-requisito para as operações, uma vez que o texto precisa ser formatado corretamente e disposto em um conjunto especificado de restrições antes que possa ser desenhado ou testado com sucesso. Dois objetos principais que você pode criar com um [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) para essa finalidade são [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). Um objeto **IDWriteTextFormat** representa as informações de formatação para um parágrafo de texto. A função [**IDWriteFactory:: CreateTextLayout**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout) usa a cadeia de caracteres de entrada, as restrições associadas, como a dimensão do espaço a ser preenchido e o objeto **IDWriteTextFormat** , e coloca o resultado totalmente analisado e formatado em **IDWriteTextLayout** para uso em operações subsequentes.

O aplicativo pode renderizar o texto usando a função [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) fornecida pelo [Direct2D](../direct2d/direct2d-portal.md) ou implementando uma função de retorno de chamada que pode usar GDI, Direct2D ou outros sistemas gráficos para renderizar os glifos. Para um único texto de formato, a função [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) no Direct2D fornece uma maneira mais simples de desenhar texto sem precisar primeiro criar um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) .

## <a name="formatting-and-drawing-hello-world-using-directwrite"></a>Formatando e desenhando "Olá, Mundo" usando DirectWrite

O exemplo de código a seguir mostra como um aplicativo pode formatar um único parágrafo usando [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e desenhá-lo usando a função [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) [Direct2D](../direct2d/direct2d-portal.md).


```C++
HRESULT DemoApp::DrawHelloWorld(
    ID2D1HwndRenderTarget* pIRenderTarget
    )
{
    HRESULT hr = S_OK;
    ID2D1SolidColorBrush* pIRedBrush = NULL;
    IDWriteTextFormat* pITextFormat = NULL;
    IDWriteFactory* pIDWriteFactory = NULL;

    if (SUCCEEDED(hr))
    {
        hr = DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED,
                __uuidof(IDWriteFactory),
                reinterpret_cast<IUnknown**>(&pIDWriteFactory));
    }

    if(SUCCEEDED(hr))
    {
        hr = pIDWriteFactory->CreateTextFormat(
            L"Arial", 
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL, 
            DWRITE_FONT_STYLE_NORMAL, 
            DWRITE_FONT_STRETCH_NORMAL, 
            10.0f * 96.0f/72.0f, 
            L"en-US", 
            &pITextFormat
        );
    }

    if(SUCCEEDED(hr))
    {
        hr = pIRenderTarget->CreateSolidColorBrush(
            D2D1:: ColorF(D2D1::ColorF::Red),
            &pIRedBrush
        );
    }
    
   D2D1_RECT_F layoutRect = D2D1::RectF(0.f, 0.f, 100.f, 100.f);

    // Actually draw the text at the origin.
    if(SUCCEEDED(hr))
    {
        pIRenderTarget->DrawText(
            L"Hello World",
            wcslen(L"Hello World"),
            pITextFormat,
            layoutRect, 
            pIRedBrush
        );
    }

    // Clean up.
    SafeRelease(&pIRedBrush);
    SafeRelease(&pITextFormat);
    SafeRelease(&pIDWriteFactory);

    return hr;
}
```



## <a name="accessing-the-font-system"></a>Acessando o sistema de fontes

Além de especificar um nome de família de fontes para a cadeia de caracteres de texto usando a interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) no exemplo acima, o [DirectWrite](direct-write-portal.md) fornece aos aplicativos mais controle sobre a seleção de fontes por meio da enumeração de fontes e a capacidade de criar uma coleção de fontes personalizada com base em fontes de documento inseridas.

O objeto [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) é uma coleção de famílias de fontes. O DirectWrite fornece acesso ao conjunto de fontes instaladas no sistema por meio de uma coleção de fontes especial chamada coleção de fontes do sistema. Isso é obtido chamando o método [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) do objeto [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) . Um aplicativo também pode criar uma coleção de fontes personalizada de um conjunto de fontes enumeradas por um retorno de chamada definido pelo aplicativo, ou seja, fontes privadas instaladas por um aplicativo ou fontes inseridas em um documento.

O aplicativo pode chamar [**GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily) para obter um objeto FontFamily específico dentro da coleção e, em seguida, chamar [**IDWriteFontFamily:: GetFirstMatchingFont**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfirstmatchingfont) para obter um objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) específico. O objeto **IDWriteFont** representa uma fonte em uma coleção de fontes e expõe propriedades e algumas métricas de fontes básicas.

O [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) é outro objeto que representa uma fonte e expõe um conjunto completo de métricas em uma fonte. O **IDWriteFontFace** pode ser criado diretamente a partir de um nome de fonte; um aplicativo não precisa obter uma coleção de fontes para acessá-la. É útil para um aplicativo de layout de texto, como o Microsoft Word, que precisa consultar os detalhes de uma fonte específica.

O diagrama a seguir ilustra a relação entre esses objetos.

![diagrama da relação entre uma coleção de fontes, uma família de fontes e um tipo de fonte](images/fontcollection.png)

### <a name="idwritefontface"></a>IDWriteFontFace

O objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) representa uma fonte e fornece informações mais detalhadas sobre a fonte do que o objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) . As métricas de fonte e glifo do **IDWriteFontFace** são úteis para aplicativos que implementam o layout de texto.

A maioria dos aplicativos principais não usará essas APIs diretamente e, em vez disso, usará [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) ou especificará o nome da família de fontes diretamente.

A tabela a seguir resume os cenários de uso para os dois objetos.



| Categoria                                                                                                         | [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------|
| APIs para dar suporte à interação do usuário, como uma interface do usuário do seletor de fonte: Descrição e outras APIs informativas | Sim                                        | Não                                                 |
| APIs para dar suporte ao mapeamento de fontes: família, estilo, peso, ampliação, cobertura de caracteres                                 | Sim                                        | Não                                                 |
| API DrawText                                                                                                     | Sim                                        | Não                                                 |
| APIs usadas para renderização                                                                                          | Não                                         | Sim                                                |
| APIs usadas para layout de texto: métricas de glifo e assim por diante                                                              | Não                                         | Sim                                                |
| APIs para controle de interface do usuário e layout de texto: métricas de toda a fonte                                                           | Sim                                        | Sim                                                |



 

Este é um aplicativo de exemplo que enumera as fontes na coleção de fontes do sistema.


```C++
#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

        IDWriteLocalizedStrings* pFamilyNames = NULL;
        
        // Get a list of localized strings for the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFontFamily->GetFamilyNames(&pFamilyNames);
        }

        UINT32 index = 0;
        BOOL exists = false;
        
        wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

        if (SUCCEEDED(hr))
        {
            // Get the default locale for this user.
            int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

            // If the default locale is returned, find that locale name, otherwise use "en-us".
            if (defaultLocaleSuccess)
            {
                hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
            }
            if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
            {
                hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
            }
        }
        
        // If the specified locale doesn't exist, select the first on the list.
        if (!exists)
            index = 0;

        UINT32 length = 0;

        // Get the string length.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetStringLength(index, &length);
        }

        // Allocate a string big enough to hold the name.
        wchar_t* name = new (std::nothrow) wchar_t[length+1];
        if (name == NULL)
        {
            hr = E_OUTOFMEMORY;
        }

        // Get the family name.
        if (SUCCEEDED(hr))
        {
            hr = pFamilyNames->GetString(index, name, length+1);
        }
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}

```



## <a name="text-rendering"></a>Renderização de texto

As APIs de renderização de texto permitem que os glifos em uma fonte [DirectWrite](direct-write-portal.md) sejam renderizados em uma superfície [Direct2D](../direct2d/direct2d-portal.md) ou em um bitmap independente de dispositivo GDI ou sejam convertidos em contornos ou bitmaps. A renderização de ClearType no DirectWrite dá suporte ao posicionamento de subpixel com nitidez aprimorada e contraste em comparação com as implementações anteriores no Windows. O DirectWrite também dá suporte a texto em preto e branco com alias para dar suporte a cenários que envolvem fontes do leste asiático com bitmaps inseridos ou onde o usuário desabilitou a suavização de fontes de qualquer tipo.

Todas as opções são ajustáveis por todos os botões de ClearType disponíveis acessíveis por meio das APIs do [DirectWrite](direct-write-portal.md) e também expostas por meio do novo miniaplicativo do painel de controle de sintonizador do Windows 7 ClearType.

Há duas APIs disponíveis para renderizar glifos, uma fornecendo renderização acelerada por hardware por meio de [Direct2D](../direct2d/direct2d-portal.md) e a outra fornecendo renderização de software para um bitmap GDI. Um aplicativo usando [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) e implementando o retorno de chamada [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) pode chamar qualquer uma dessas funções em resposta a um retorno de chamada [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) . Além disso, os aplicativos que implementam seu próprio layout ou lidam com dados em nível de glifo podem usar essas APIs.

1.  [**ID2DRenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)

    Os aplicativos podem usar a API do [Direct2D](../direct2d/direct2d-portal.md) [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) para fornecer aceleração de hardware para a renderização de texto usando a GPU. A aceleração de hardware afeta todas as fases do pipeline de renderização de texto — de Mesclar glifos em execuções de glifos e filtrar o bitmap de execução de glifos, para aplicar o algoritmo de mesclagem ClearType à saída final exibida. Essa é a API recomendada para obter o melhor desempenho de renderização.

2.  [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun)

    Os aplicativos podem usar o método [**IDWriteBitmapRenderTarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) para executar um processamento de software de uma execução de glifos em um bitmap 32-bpp. O objeto [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) encapsula um bitmap e um contexto de dispositivo de memória que pode ser usado para renderizar glifos. Essa API será útil se você quiser se manter com o GDI porque você tem uma base de código existente que é renderizada em GDI.

Se você tiver um aplicativo que tenha código de layout de texto existente que usa GDI e desejar preservar seu código de layout existente, mas usar [DirectWrite](direct-write-portal.md) apenas para a etapa final de processamento de glifos, [**IDWriteGdiInterop:: CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc) fornecerá a ponte entre as duas APIs. Antes de chamar essa função, o aplicativo usará a função **IDWriteGdiInterop:: CreateFontFaceFromHdc** para obter uma referência de face de fonte de um contexto de dispositivo.

> [!Note]  
> Na maioria dos cenários, os aplicativos podem não precisar usar essas APIs de renderização de glifo. Depois que um aplicativo cria um objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) , ele pode usar o método [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) para renderizar o texto.

 

## <a name="custom-rendering-modes"></a>Modos de renderização personalizados

Vários parâmetros afetam A renderização de texto, como gama, nível de ClearType, geometria de pixel e contraste aprimorado. Os parâmetros de renderização são encapsulados por um objeto, que implementa a interface [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) pública. O objeto de parâmetros de renderização é inicializado automaticamente com base nas propriedades de hardware e/ou nas preferências do usuário especificadas por meio do miniaplicativo do painel de controle ClearType no Windows 7. Em geral, se um cliente usar a API de layout [DirectWrite](direct-write-portal.md) , o DirectWrite selecionará automaticamente um modo de renderização que corresponda ao modo de medição especificado.

Os aplicativos que desejam mais controle podem usar [**IDWriteFactory:: CreateCustomRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomrenderingparams) para implementar as diferentes opções de renderização. Essa função também pode ser usada para definir o gama, a geometria de pixel e o contraste avançado.

A seguir estão as várias opções de renderização disponíveis:

-   Suavização de subconjunto de pixel

    O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ natural para especificar o processamento com suavização de serrilhado somente na dimensão horizontal.

-   Suavização de subconjuntos de subpixel nas dimensões horizontal e vertical.

    O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ \_ simétrico natural para especificar a renderização com suavização de serrilhado nas dimensões horizontal e vertical. Isso faz com que as curvas e as linhas diagonais pareçam mais suaves às custas de alguma suavidade e normalmente são usadas em tamanhos acima de 16 ppem.

-   Texto com alias

    O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ com alias para especificar o texto com alias.

-   Texto em escala de cinza

    O aplicativo define o parâmetro *pixelGeometry* como DWRITE de \_ geometria de pixel \_ \_ plano para especificar texto em escala de cinza.

-   Compatível com GDI-largura (incluindo bitmap do leste asiático Embedded)

    O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ GDI \_ clássico para especificar a suavização de largura compatível com GDI.

-   Largura natural GDI

    O aplicativo define o parâmetro *RenderingMode* para o \_ modo de renderização DWRITE \_ \_ GDI \_ natural para especificar a suavização de serrilhado compatível com a largura natural do GDI.

-   Texto de contorno

    Para renderização em tamanhos grandes, um desenvolvedor de aplicativos pode preferir renderizar usando a estrutura de tópicos da fonte em vez de rasterizar em um bitmap. O aplicativo define o parâmetro *RenderingMode* para **a \_ estrutura \_ de \_ Tópicos do modo de renderização DWRITE** para especificar que a renderização deve ignorar o rasterizador e usar os contornos diretamente.

## <a name="gdi-interoperability"></a>Interoperabilidade GDI

A interface [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) fornece interoperabilidade com GDI. Isso permite que os aplicativos continuem seus investimentos existentes em bases de código GDI e usem seletivamente o [DirectWrite](direct-write-portal.md) para renderização ou layout.

A seguir estão as APIs que permitem que um aplicativo migre para ou do sistema de fontes GDI:

-   [**CreateFontFromLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)

    Cria um objeto [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) que corresponde às propriedades especificadas pela estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

-   [**ConvertFontToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont)

    Inicializa uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) com base nas propriedades compatíveis com GDI do [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)especificado.

-   [**ConvertFontFaceToLOGFONT**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)

    Inicializa uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) com base nas propriedades compatíveis com GDI do [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)especificado.

-   [**CreateFontFaceFromHdc**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc)

    Cria um objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) que corresponde ao **HFONT** selecionado no momento.

## <a name="conclusion"></a>Conclusão

Melhorar a experiência de leitura é de grande valor para os usuários, seja na tela ou em papel. O [DirectWrite](direct-write-portal.md) fornece a facilidade de uso e o modelo de programação em camadas para que os desenvolvedores de aplicativos aprimorem a experiência de texto para seus aplicativos do Windows. Os aplicativos podem usar DirectWrite para renderizar texto formatado de formato rico para sua interface do usuário e documentos com a API de layout. Para cenários mais complexos, um aplicativo pode trabalhar diretamente com glifos, fontes de acesso e assim por diante e aproveitar a potência do DirectWrite para fornecer uma tipografia de alta qualidade.

Os recursos de interoperabilidade do [DirectWrite](direct-write-portal.md) permitem que os desenvolvedores de aplicativos encaminhem suas bases de código Win32 existentes e adotem DirectWrite seletivamente dentro de seus aplicativos.

 

 