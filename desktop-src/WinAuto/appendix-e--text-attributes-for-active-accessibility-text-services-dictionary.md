---
title: Atributos do Apêndice E de texto para Acessibilidade Ativa dicionário de serviços de texto
description: Este apêndice fornece informações sobre atributos de texto que são definidos em IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588c827764d17c2576efaa5e3117527e23d1da26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008312"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Apêndice E: atributos de texto para Acessibilidade Ativa dicionário de serviços de texto

Este apêndice fornece informações sobre atributos de texto que são definidos em [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary). Ele é organizado como uma série de tabelas. Cada tabela inclui informações sobre uma categoria específica de atributos. Essas categorias são realmente aninhadas, mas são separadas abaixo para que você possa ver os atributos.

> [!Note]  
> Os serviços de texto Acessibilidade Ativa são preteridos. Consulte a [estrutura de serviços de texto do Microsoft Windows](../tsf/text-services-framework.md) para obter mais informações sobre as tecnologias avançadas de entrada de texto e linguagem natural.

 

Cada entrada em uma tabela fornece um nome de atributo e nome amigável, tipo, folhas de estilos em cascata (CSS) equivalente, equivalente a TOM (modelo de objeto de texto) e quaisquer comentários adicionais, quando apropriado. A coluna TOM equivalente fornece informações sobre o método TOM usado com o atributo (parte das interfaces [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont), [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)ou [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) ). As informações antes de cada tabela indicam qual interface oferece suporte aos atributos; as informações na tabela TOM equivalente indicam o nome do método. Cada entrada na coluna equivalente de TOM é associada a dois métodos. Por exemplo, a entrada de nome está associada aos métodos **GetName** e **SetName** .

Para obter mais informações sobre essas interfaces, consulte a documentação do [modelo de objeto de texto](../controls/text-object-model.md) no SDK (Software Development Kit) do Windows.

## <a name="font"></a>Fonte

Os atributos na tabela a seguir são associados a atributos de fonte geral. O TOM equivalente é a interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome do atributo, nome amigável       | Tipo     | Equivalente de CSS       | TOM equivalente | Comentário           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Face da fonte \_ , facename<br/> | VT \_ BSTR | Fonte-família: Verdana | Name           |                   |
| Fonte \_ SizePts, SizePts<br/>   | \_I4 VT   | Fonte-tamanho: xpt       | Tamanho           | O tamanho está em pontos |



 

## <a name="font_style"></a>Estilo da fonte \_

Os atributos nos atributos de estilo da fonte de endereço da tabela a seguir (por exemplo, se o texto está definido em negrito ou itálico). O TOM equivalente é a interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome do atributo, nome amigável                             | Tipo     | Equivalente de CSS              | TOM equivalente                                            | Comentário                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Estilo da fonte em \_ \_ negrito, negrito<br/>                        | BOOL do VT \_ | Fonte-peso: negrito           | Negrito                                                      |                           |
| Estilo da fonte \_ \_ itálico, itálico<br/>                    | BOOL do VT \_ | Fonte-estilo: itálico          | Itálico                                                    |                           |
| Estilo da fonte \_ \_ SmallCaps, SmallCaps<br/>              | BOOL do VT \_ | Font-variant: versalete    | SmallCaps                                                 |                           |
| Estilo da fonte \_ \_ capitalizar, colocar em maiúsculas<br/>             | BOOL do VT \_ | Transformação de texto: colocar em maiúsculas  | Sem suporte                                             |                           |
| Estilo da fonte \_ \_ maiúsculo, maiúsculo<br/>               | BOOL do VT \_ | Texto-transformação: maiúsculas   | AllCaps                                                   |                           |
| Estilo da fonte em \_ \_ minúsculas, minúsculas<br/>               | BOOL do VT \_ | Texto-transformação: minúsculas   | Sem suporte                                             |                           |
| Estilo da fonte \_ \_ entalhe, entalhe<br/>                     | BOOL do VT \_ | Sem suporte               | Emboss                                                    |                           |
| Estilo da fonte \_ \_ engrave, baixo que<br/>                   | BOOL do VT \_ | Sem suporte               | Baixo relevo                                                   |                           |
| Estilo de fonte \_ \_ oculto                                       | BOOL do VT \_ | Sem suporte               | Hidden                                                    |                           |
| \_ \_ Kerning de estilo de fonte, kerning<br/>                   | VT \_ R4   | Sem suporte               | Kerning                                                   | Mesmos valores que o getkerning |
| Estilo da fonte \_ \_ destacado, contornado<br/>                 | BOOL do VT \_ | Sem suporte               | Descritas                                                  |                           |
| Posição do estilo da fonte \_ \_ , posição<br/>                 | VT \_ R4   | Sem suporte               | Posição                                                  |                           |
| Estilo de fonte \_ \_ protegido                                    | BOOL do VT \_ | Sem suporte               | Protegido                                                 |                           |
| Sombra do estilo da fonte \_ \_ , sombra<br/>                     | BOOL do VT \_ | Altura da linha (menos números) | Shadow                                                    |                           |
| \_Espaçamento do estilo da fonte \_ , espaçamento<br/>                   | VT \_ R4   | Espaçamento de letras              | Espaçamento                                                   | Em pontos                 |
| Peso do estilo da fonte \_ \_ , peso<br/>                     | \_I4 VT   | Espessura da fonte                 | Valores de WeightSame como font-weight e getweight<br/> |                           |
| Altura do estilo da fonte \_ \_ , altura<br/>                     | VT \_ R4   | Line-height                 | Sem suporte                                             | Em pontos                 |
| Estilo da fonte \_ \_ piscando, piscando<br/>                       | BOOL do VT \_ | Decoração de texto: piscar      | Sem suporte                                             |                           |
| Subscript \_ \_ de estilo de fonte, subscrito<br/>               | BOOL do VT \_ | Vertical-align: sub         | Subscrito (também posição)                                 |                           |
| \_Sobrescript \_ de estilo de fonte, sobrescrito<br/>           | BOOL do VT \_ | Vertical-align: super       | Sobrescrito (também posição)                               |                           |
| Cor do estilo da fonte \_ \_ , cor<br/>                       | \_I4 VT   | Cor                       | ForeColor                                                 | Estilo RGB COLORREF        |
| Estilo da fonte \_ \_ BackgroundColor, cor do plano de fundo \_<br/> | \_I4 VT   | Plano de fundo-cor            | BackColor                                                 | Estilo RGB COLORREF        |



 

## <a name="font_style_animation"></a>\_Animação de estilo da fonte \_

Os atributos na seguinte animação de fonte de endereço de tabela. O TOM equivalente é a interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome do atributo, nome amigável                                              | Tipo     | Equivalente de CSS | TOM equivalente |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| \_ \_ Animação de estilo \_ de fonte LasVegasLights, \_ luzes LasVegas<br/>         | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ \_ BlinkingBackground de animação de estilo de fonte, plano de fundo piscando \_<br/> | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ Animação de estilo \_ de fonte SparkleText, \_ texto Sparkle<br/>               | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ \_ MarchingBlackAnts de animação de estilo de fonte, \_ Ants em preto de março \_<br/> | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ Animação de estilo \_ de fonte MarchingRedAnts, Ants de março em \_ vermelho \_<br/>     | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ Animação de estilo \_ de fonte shimmer, shimmer<br/>                         | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ Animação de estilo \_ de fonte WipeDown, WipeDown<br/>                       | BOOL do VT \_ | Sem suporte  | Animação      |
| \_ \_ Animação de estilo \_ de fonte WipeRight, WipeRight<br/>                     | BOOL do VT \_ | Sem suporte  | Animação      |



 

## <a name="font_style_underline"></a>Sublinhado do estilo da fonte \_ \_

Os atributos na tabela a seguir abordam os estilos de sublinhado para fontes. O TOM equivalente é a interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nome do atributo, nome amigável                     | Tipo     | Equivalente de CSS                | TOM equivalente |
|---------------------------------------------------|----------|-------------------------------|----------------|
| Estilo da fonte \_ \_ sublinhado \_ simples, único<br/>  | BOOL do VT \_ | Decoração de texto: sublinhado    | Underline      |
| Estilo da fonte \_ \_ sublinhado \_ duplo, duplo<br/> | BOOL do VT \_ | Decoração de texto: linha | StrikeThrough  |



 

## <a name="font_style_strikethrough"></a>Estilo de fonte \_ \_ tachado

Os atributos na tabela a seguir abordam os estilos de tachado das fontes.



| Nome do atributo, nome amigável                                         | Tipo     | Equivalente de CSS | TOM equivalente |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| \_Estilo \_ de fonte tachado \_ único, tachado \_ \_ único<br/> | BOOL do VT \_ | Sem suporte  | Sem suporte  |
| Estilo da fonte \_ \_ tachado \_ duplo, tachado \_ \_ duplo<br/> | BOOL do VT \_ | Sem suporte  | Sem suporte  |



 

## <a name="font_style_overline"></a>Estilo da fonte \_ \_ sobreposta

Os atributos na tabela a seguir redirecionam os estilos de linha para as fontes.



| Nome do atributo, nome amigável                             | Tipo     | Equivalente de CSS            | TOM equivalente |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| Estilo da fonte \_ \_ linha sobreposta \_ única, linha sobreposta \_ única<br/> | BOOL do VT \_ | Decoração de texto: linha sobreposta | Sem suporte  |
| Estilo da fonte \_ \_ sobreposta \_ dupla, linha sobreposta \_ dupla<br/> | BOOL do VT \_ | Decoração de texto: linha sobreposta | Sem suporte  |



 

## <a name="text"></a>Texto

Os atributos na tabela a seguir abordam os atributos gerais de formatação de texto.



| Nome do atributo, nome amigável                     | Tipo        | Equivalente de CSS | TOM equivalente                                       | Comentário                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Texto \_ VerticalWriting, escrita vertical<br/> | BOOL do VT \_    | Sem suporte  | sem suporte                                        | Conforme usado por chinês/japonês                                                           |
| \_RightToLeft de texto, RightToLeft<br/>          | BOOL do VT \_    | Direção      | Sem suporte                                        |                                                                                       |
| Texto \_ ReadOnly, somente leitura<br/>               | BOOL do VT \_    | Sem suporte  | ITextFont:: canchange, ITextRange:: CanEdit            | A propriedade editável do documento tem precedência                                     |
| Idioma do texto \_ , idioma<br/>                | \_I4 VT      | Sem suporte  | ITextFont:: getlanguageid, ITextFont:: setlanguageid   | LANGID                                                                                |
| Orientação do texto \_ , orientação<br/>          | \_I4 VT      | Sem suporte  | Sem suporte                                        | 10??? de um grau                                                                     |
| Text \_ incorporadoobject, \_ objeto inserido<br/>  | BOOL do VT \_    | Sem suporte  | Sem suporte                                        | Permite pesquisar objetos inseridos                                                 |
| \_Link de texto, link<br/>                        | VT \_ desconhecido | Link           | Sem suporte                                        | Um ponteiro de interface para o objeto; chamar QueryInterface para qualquer interface de interesse |
| \_Hifenização de texto, hifenização<br/>          | BOOL do VT \_    | Sem suporte  | ITextPara:: gethifenization, ITextPara:: sethifenization |                                                                                       |



 

## <a name="text_alignment"></a>Alinhamento de texto \_

Os atributos na tabela a seguir estão no alinhamento de texto do endereço. O TOM equivalente é a interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome do atributo, nome amigável               | Tipo     | Equivalente de CSS | TOM equivalente |
|---------------------------------------------|----------|----------------|----------------|
| \_Alinhamento \_ de texto à esquerda, à esquerda<br/>       | BOOL do VT \_ | Alinhamento de texto     | Alinhamento      |
| \_Alinhamento \_ de texto à direita, à direita<br/>     | BOOL do VT \_ | Alinhamento de texto     | Alinhamento      |
| \_ \_ Centro de alinhamento de texto, centro<br/>   | BOOL do VT \_ | Alinhamento de texto     | Alinhamento      |
| \_Justificar alinhamento \_ de texto, justificar<br/> | BOOL do VT \_ | Alinhamento de texto     | Alinhamento      |



 

## <a name="text_para"></a>Texto \_ para

Os atributos na seguinte formatação de endereço de tabela para parágrafos. O TOM equivalente é a interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome do atributo, nome amigável                              | Tipo   | Equivalente de CSS | TOM equivalente  | Comentário |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Texto \_ para \_ FirstLineIndent, recuo da primeira \_ linha \_<br/> | VT \_ R4 | Sem suporte  | FirstLineIndent | Em pts  |
| Texto \_ para \_ LeftIndent, recuo à esquerda \_<br/>             | VT \_ R4 | Sem suporte  | LeftIndent      | Em pts  |
| Texto \_ para \_ RightIndent, recuo à direita \_<br/>           | VT \_ R4 | Sem suporte  | RightIndent     | Em pts  |
| Texto \_ para \_ SpaceAfter, espaço \_ após<br/>             | VT \_ R4 | Sem suporte  | SpaceAfter      | Em pts  |
| Texto \_ para \_ SpaceBefore, espaço \_ após<br/>            | VT \_ R4 | Sem suporte  | SpaceAfter      | Em pts  |



 

## <a name="text_para_linespacing"></a>Texto \_ para \_ lineSpacing

Os atributos na tabela a seguir espaçamento de linha de endereço em parágrafos. O TOM equivalente é a interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome do atributo, nome amigável                               | Tipo     | Equivalente de CSS | TOM equivalente | Comentário  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Texto \_ para \_ lineSpacing \_ única, única<br/>           | BOOL do VT \_ | Sem suporte  | LineSpacing    |          |
| Text \_ para \_ lineSpacing \_ OnePtFive, um \_ pt \_ cinco<br/> | BOOL do VT \_ | Sem suporte  | LineSpacing    |          |
| Texto \_ para \_ lineSpacing \_ duplo, duplo<br/>           | BOOL do VT \_ | Sem suporte  | LineSpacing    |          |
| Text \_ para \_ lineSpacing \_ pelo menos, \_ no mínimo<br/>       | VT \_ R4   | Sem suporte  | LineSpacing    | Em linhas |
| Text \_ para \_ lineSpacing \_ exatamente, exatamente<br/>         | VT \_ R4   | Sem suporte  | LineSpacing    | Em linhas |
| Text \_ para \_ lineSpacing \_ vários, Multiple<br/>        | VT \_ R4   | Sem suporte  | LineSpacing    | Em linhas |



 

## <a name="text_list"></a>Lista de texto \_

Os atributos nas seguintes listas de endereços de tabela e níveis de listas de texto. O TOM equivalente é a interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome do atributo, nome amigável | Tipo   | Equivalente de CSS | TOM equivalente | Comentário                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| \_LevelIndex da lista \_ de texto,       | \_I4 VT | Sem suporte  | ListLevelIndex | Onde 1 é a lista mais externa, 2 é o próximo nível e assim por diante |



 

## <a name="text_list_type"></a>\_Tipo de lista de texto \_

Os atributos nos seguintes estilos de lista de endereços de tabela para texto. O TOM equivalente é a interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nome do atributo, nome amigável                          | Tipo     | Equivalente de CSS  | TOM equivalente |
|--------------------------------------------------------|----------|-----------------|----------------|
| \_ \_ \_ Marcador de tipo de lista de texto, marcador<br/>             | BOOL do VT \_ | Tipo de lista       | ListType       |
| \_ \_ Tipo de lista \_ de texto árabe, árabe<br/>             | BOOL do VT \_ | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto LowerLetter, \_ letra minúscula<br/> | BOOL do VT \_ | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto UpperLetter, \_ letra superior<br/> | BOOL do VT \_ | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto LowerRoman, \_ Roman inferior<br/>   | BOOL do VT \_ | Tipo de estilo de lista | ListType       |
| \_ \_ Tipo de lista \_ de texto UpperRoman, Upper \_ Roman<br/>   | BOOL do VT \_ | Tipo de estilo de lista | ListType       |



 

## <a name="app"></a>Aplicativo



| Nome do atributo, nome amigável                         | Tipo     | Equivalente de CSS | TOM equivalente |
|-------------------------------------------------------|----------|----------------|----------------|
| IncorrectSpelling do aplicativo \_ , \_ ortografia incorreta<br/> | BOOL do VT \_ |                | Sem suporte  |
| IncorrectGrammar do aplicativo \_ , \_ gramática incorreta<br/>   | BOOL do VT \_ |                | Sem suporte  |



 

 

