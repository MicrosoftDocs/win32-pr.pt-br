---
title: Apêndice E Atributos de Texto Acessibilidade Ativa Dicionário de Serviços de Texto
description: Este apêndice fornece informações sobre atributos de texto definidos em IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539583f05e5140d96594490b0038b1a629f7760b13e4de223f6a8a3304c3901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134059"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Apêndice E: Atributos de texto para Acessibilidade Ativa dicionário de serviços de texto

Este apêndice fornece informações sobre atributos de texto definidos [**em IAccDictionary.**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary) Ele é organizado como uma série de tabelas. Cada tabela inclui informações sobre uma categoria específica de atributos. Essas categorias são realmente aninhadas, mas são separadas abaixo para que você possa ver os atributos.

> [!Note]  
> Acessibilidade Ativa Text Services foi preterido. Consulte [Microsoft Windows Estrutura de Serviços de Texto](../tsf/text-services-framework.md) para obter mais informações sobre a entrada de texto avançada e as tecnologias de linguagem natural.

 

Cada entrada em uma tabela fornece um nome de atributo e um nome amigável, tipo, folhas de estilos em cascata (CSS) equivalente, equivalente a TOM (Modelo de Objeto de Texto) e quaisquer comentários adicionais quando apropriado. A coluna equivalente tom fornece informações sobre o método TOM usado com o atributo (parte das interfaces [**ITextFont,**](/windows/desktop/api/tom/nn-tom-itextfont) [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)ou [**ITextPara).**](/windows/desktop/api/tom/nn-tom-itextpara) As informações anteriores a cada tabela indicam qual interface dá suporte aos atributos; as informações na tabela equivalente do TOM indicam o nome do método. Cada entrada na coluna equivalente tom é associada a dois métodos. Por exemplo, a entrada Name está associada aos métodos **GetName** e **SetName.**

Para obter mais informações sobre essas interfaces, consulte a [documentação](../controls/text-object-model.md) do Modelo de Objeto de Texto no SDK (Software Development Kit) do Windows.

## <a name="font"></a>Fonte

Os atributos na tabela a seguir são associados a atributos de fonte gerais. O equivalente tom é a interface [**ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome do atributo, Nome amigável       | Tipo     | Equivalente de CSS       | Equivalente a TOM | Comentário           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| Font \_ FaceName, facename<br/> | VT \_ BSTR | Família de fontes: Verdana | Nome           |                   |
| Font \_ SizePts, sizePts<br/>   | VT \_ I4   | Tamanho da fonte: Xpt       | Tamanho           | O tamanho está em pontos |



 

## <a name="font_style"></a>Estilo da \_ fonte

Os atributos na tabela a seguir abordam atributos de estilo de fonte (por exemplo, se o texto está definido em negrito ou em itálico). O equivalente tom é a interface [**ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome do atributo, Nome amigável                             | Tipo     | Equivalente de CSS              | Equivalente a TOM                                            | Comentário                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| Estilo \_ da fonte \_ negrito, negrito<br/>                        | BOOL da VT \_ | Peso da fonte: negrito           | Negrito                                                      |                           |
| Itálico \_ \_ de estilo de fonte, itálico<br/>                    | BOOL da VT \_ | Estilo de fonte: itálico          | Itálico                                                    |                           |
| \_SmallCaps de estilo de \_ fonte, smallcaps<br/>              | BOOL da VT \_ | Variante de fonte: small-caps    | SmallCaps                                                 |                           |
| Maiúsculas \_ e \_ maiúsculas de estilo da fonte, maiúsculas<br/>             | BOOL da VT \_ | Transformação de texto: capitalizar  | Sem suporte                                             |                           |
| Letras \_ \_ maiúsculas e maiúsculas do estilo da fonte<br/>               | BOOL da VT \_ | Transformação de texto: maiúsculas   | AllCaps                                                   |                           |
| Estilo \_ da \_ fonte minúscula, minúscula<br/>               | BOOL da VT \_ | Transformação de texto: minúsculas   | Sem suporte                                             |                           |
| \_ \_ Emboss de estilo de fonte, emboss<br/>                     | BOOL da VT \_ | Sem suporte               | Emboss                                                    |                           |
| Font \_ Style \_ Desaqueia,<br/>                   | BOOL da VT \_ | Sem suporte               | Gravar                                                   |                           |
| Estilo \_ de fonte \_ oculto                                       | BOOL da VT \_ | Sem suporte               | Hidden                                                    |                           |
| Coloração \_ \_ de estilo de fonte, com a coloração<br/>                   | VT \_ R4   | Sem suporte               | Kerning                                                   | Mesmos valores que GetKerning |
| Estilo \_ de \_ fonte descrito, descrito<br/>                 | BOOL da VT \_ | Sem suporte               | Descrito                                                  |                           |
| Posição \_ do estilo da \_ fonte, posição<br/>                 | VT \_ R4   | Sem suporte               | Posição                                                  |                           |
| Estilo \_ de \_ fonte protegido                                    | BOOL da VT \_ | Sem suporte               | Protegido                                                 |                           |
| Sombra \_ de estilo de \_ fonte, sombra<br/>                     | BOOL da VT \_ | Altura da linha (números de menos) | Shadow                                                    |                           |
| \_Espaçamento de estilo de \_ fonte, espaçamento<br/>                   | VT \_ R4   | Espaçamento de letra              | Espaçamento                                                   | Em pontos                 |
| Peso \_ do estilo da \_ fonte, peso<br/>                     | VT \_ I4   | Peso da fonte                 | Valores weightSame como font-weight e GetWeight<br/> |                           |
| Altura \_ do estilo da \_ fonte, altura<br/>                     | VT \_ R4   | Line-height                 | Sem suporte                                             | Em pontos                 |
| Estilo \_ da \_ fonte Piscar, piscar<br/>                       | BOOL da VT \_ | Decoração de texto: piscar      | Sem suporte                                             |                           |
| \_ \_ Subscrito de estilo de fonte, subscrito<br/>               | BOOL da VT \_ | Alinhamento vertical: sub         | Subscrito (também Posição)                                 |                           |
| Superscript \_ de estilo de \_ fonte, superscrito<br/>           | BOOL da VT \_ | Alinhamento vertical: super       | Sobrescrito (também Posição)                               |                           |
| Cor \_ do estilo da \_ fonte, cor<br/>                       | VT \_ I4   | Color                       | ForeColor                                                 | Estilo COLORREF do RBG        |
| BackgroundColor \_ do \_ Estilo da Fonte, cor da tela de \_ fundo<br/> | VT \_ I4   | Cor da tela de fundo            | BackColor                                                 | Estilo COLORREF do RBG        |



 

## <a name="font_style_animation"></a>Animação \_ de estilo \_ de fonte

Os atributos na seguinte animação de fonte de endereço de tabela. O equivalente tom é a interface [**ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome do atributo, Nome amigável                                              | Tipo     | Equivalente de CSS | Equivalente a TOM |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| Animação \_ de estilo de fonte \_ \_ LasVegaLights, luzes LasVega \_<br/>         | BOOL da VT \_ | Sem suporte  | Animação      |
| Animação \_ de estilo de fonte \_ \_ BlinkingBackground, plano de fundo \_ piscando<br/> | BOOL da VT \_ | Sem suporte  | Animação      |
| Animação \_ de \_ estilo de \_ fonteTextotexto de \_ texto de texto de texto<br/>               | BOOL da VT \_ | Sem suporte  | Animação      |
| Animação \_ de \_ estilo de \_ fonte, AnimationBlackAnts, \_ 400000001 \_<br/> | BOOL da VT \_ | Sem suporte  | Animação      |
| Animação \_ de estilo de fonte \_ \_ AnimationRedAnts, vermelho \_ vermelho \_ retrito<br/>     | BOOL da VT \_ | Sem suporte  | Animação      |
| Animação \_ \_ de estilo de \_ fonte, Gaemmer<br/>                         | BOOL da VT \_ | Sem suporte  | Animação      |
| Apagamento \_ de \_ \_ animação de estilo de fonte, wipeDown<br/>                       | BOOL da VT \_ | Sem suporte  | Animação      |
| Animação \_ de estilo de fonte \_ \_ WipeRight,wipeRight<br/>                     | BOOL da VT \_ | Sem suporte  | Animação      |



 

## <a name="font_style_underline"></a>\_ \_ Sublinhado de estilo de fonte

Os atributos na tabela a seguir abordam estilos sublinhados para fontes. O equivalente tom é a interface [**ITextFont.**](/windows/desktop/api/tom/nn-tom-itextfont)



| Nome do atributo, Nome amigável                     | Tipo     | Equivalente de CSS                | Equivalente a TOM |
|---------------------------------------------------|----------|-------------------------------|----------------|
| \_ \_ Sublinhado de \_ estilo de fonte único, único<br/>  | BOOL da VT \_ | Decoração de texto: sublinhado    | Underline      |
| \_ \_ Sublinhado de estilo \_ de fonte double, double<br/> | BOOL da VT \_ | Decoração de texto: passagem de linha | StrikeThrough  |



 

## <a name="font_style_strikethrough"></a>\_Tachado de estilo de \_ fonte

Os atributos na tabela a seguir abordam estilos tachados para fontes.



| Nome do atributo, Nome amigável                                         | Tipo     | Equivalente de CSS | Equivalente a TOM |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| Estilo \_ de \_ fonte \_ tachado único, \_ tachado \_ por meio de um único<br/> | BOOL da VT \_ | Sem suporte  | Sem suporte  |
| Estilo \_ de \_ fonte tachado \_ double, \_ tachado \_ em double<br/> | BOOL da VT \_ | Sem suporte  | Sem suporte  |



 

## <a name="font_style_overline"></a>\_Sobrelinhado \_ de estilo de fonte

Os atributos na tabela a seguir abordam estilos sobrelinhados para fontes.



| Nome do atributo, Nome amigável                             | Tipo     | Equivalente de CSS            | Equivalente a TOM |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| \_ \_ Sobrelinhado \_ de estilo de fonte único, sobrelinhado \_ único<br/> | BOOL da VT \_ | Decoração de texto: sobrelinhado | Sem suporte  |
| Estilo \_ de fonte Duplo \_ \_ sobrelinhado, duplo \_ sobrelinhado<br/> | BOOL da VT \_ | Decoração de texto: sobrelinhado | Sem suporte  |



 

## <a name="text"></a>Texto

Os atributos na tabela a seguir abordam atributos gerais de formatação de texto.



| Nome do atributo, Nome amigável                     | Tipo        | Equivalente de CSS | Equivalente a TOM                                       | Comentário                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| \_VerticalEscrita de texto, escrita vertical<br/> | BOOL da VT \_    | Sem suporte  | sem suporte                                        | Conforme usado por chinês/japonês                                                           |
| Text \_ RightToLeft, righttoleft<br/>          | BOOL da VT \_    | Direção      | Sem suporte                                        |                                                                                       |
| Somente \_ leitura de texto, somente leitura<br/>               | BOOL da VT \_    | Sem suporte  | ITextFont::CanChange, ITextRange::CanEdit            | A propriedade editável do documento tem precedência                                     |
| Idioma \_ do Texto, idioma<br/>                | VT \_ I4      | Sem suporte  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | Langid                                                                                |
| Orientação \_ de texto, orientação<br/>          | VT \_ I4      | Sem suporte  | Sem suporte                                        | 10??? de um grau                                                                     |
| Text \_ EmbeddedObject, objeto \_ inserido<br/>  | BOOL da VT \_    | Sem suporte  | Sem suporte                                        | Permite pesquisar objetos inseridos                                                 |
| Link \_ de texto,link<br/>                        | VT \_ UNKNOWN | Link           | Sem suporte                                        | Um ponteiro de interface para o objeto ; chame QueryInterface para qualquer interface de interesse |
| \_Hifenização de texto, hifenização<br/>          | BOOL da VT \_    | Sem suporte  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>Alinhamento \_ de texto

Os atributos no alinhamento de texto de endereço da tabela a seguir. O equivalente tom é a interface [**ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome do atributo, Nome amigável               | Tipo     | Equivalente de CSS | Equivalente a TOM |
|---------------------------------------------|----------|----------------|----------------|
| Alinhamento \_ de texto à \_ esquerda, à esquerda<br/>       | BOOL da VT \_ | Alinhamento de texto     | Alinhamento      |
| Alinhamento \_ de texto à \_ direita, direita<br/>     | BOOL da VT \_ | Alinhamento de texto     | Alinhamento      |
| Centro \_ de Alinhamento de \_ Texto, centro<br/>   | BOOL da VT \_ | Alinhamento de texto     | Alinhamento      |
| Justificativa \_ de alinhamento de \_ texto,justificativa<br/> | BOOL da VT \_ | Alinhamento de texto     | Alinhamento      |



 

## <a name="text_para"></a>Para \_ texto

Os atributos na seguinte formatação de endereço de tabela para parágrafos. O equivalente tom é a interface [**ITextPara.**](/windows/desktop/api/tom/nn-tom-itextpara)



| Nome do atributo, Nome amigável                              | Tipo   | Equivalente de CSS | Equivalente a TOM  | Comentário |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| Texto \_ Para \_ FirstLineIndent, recuo \_ da primeira \_ linha<br/> | VT \_ R4 | Sem suporte  | FirstLineIndent | Em pts  |
| Texto \_ Para \_ LeftIndent, \_ recuo à esquerda<br/>             | VT \_ R4 | Sem suporte  | LeftIndent      | Em pts  |
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



| Nome do atributo, nome amigável                         | Tipo     | Equivalente de CSS | Equivalente a TOM |
|-------------------------------------------------------|----------|----------------|----------------|
| Erro \_ de ortografia do aplicativo, \_ ortografia incorreta<br/> | BOOL da VT \_ |                | Sem suporte  |
| Aplicativo \_ IncorrectGrammar, gramática \_ incorreta<br/>   | BOOL da VT \_ |                | Sem suporte  |



 

 

