---
title: Métricas de texto e fontes
description: Este tópico discute as fontes de estrutura de tópicos fornecidas pelo Windows, valores de métricas de fonte que podem ser alterados entre versões do Windows e orientações sobre como usar métricas de fonte em seus aplicativos de área de trabalho.
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27d4eb5f34f5a88e4a0e3e866f9a14784c3895
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917294"
---
# <a name="fonts-and-text-metrics"></a>Métricas de texto e fontes

Este tópico discute as fontes de estrutura de tópicos fornecidas pelo Windows, valores de métricas de fonte que podem ser alterados entre versões do Windows e orientações sobre como usar métricas de fonte em seus aplicativos de área de trabalho.

-   Para obter informações específicas sobre as métricas de fonte em DirectWrite, consulte [métricas de texto](/windows/desktop/DirectWrite/text-metrics).
-   Para obter detalhes sobre como gerenciar o texto em aplicativos usando o GDI, consulte os tópicos em [fontes e texto](/windows/desktop/gdi/fonts-and-text).

Para obter informações mais detalhadas sobre o uso de fontes e especificações de tipo, consulte o [site de tipografia da Microsoft](https://www.microsoft.com/typography/default.mspx).

## <a name="available-fonts"></a>Fontes disponíveis

As fontes de estrutura de tópicos fornecidas com o Windows são entregues como fontes OpenType com contornos TrueType (o Windows também oferece suporte a fontes OpenType no formato CFF). Para obter listas de todas as fontes fornecidas pelo Windows, consulte [Microsoft Typography: fontes por produto ou família](https://www.microsoft.com/typography/fonts/default.aspx). Todas as fontes de estrutura de tópicos do Windows estão em conformidade com a versão mais recente da [especificação OpenType](https://www.microsoft.com/typography/otspec/).

Para obter uma lista de todas as fontes de interface do usuário atuais e herdadas, confira [métricas de fontes bloqueadas](#locked-font-metrics) abaixo.

## <a name="font-modifications"></a>Modificações de fontes

Para garantir a compatibilidade com versões anteriores, as fontes raramente são removidas do Windows. No entanto, as fontes são frequentemente modificadas. As modificações podem incluir a adição de caracteres, redesenho de caracteres existentes, modificação de dicas ou adição ou modificação de suporte para recursos de OpenType avançados e formatação de script complexo.

### <a name="locked-font-metrics"></a>Métricas de fontes bloqueadas

Observe que alguns valores associados às fontes da interface do usuário e fontes padrão usadas em aplicativos Microsoft estão bloqueados. As fontes da interface do usuário são usadas para renderizar elementos da interface do usuário, como legendas, caixas de diálogo e menus. Poucas alterações são feitas nessas fontes, considerando sua alta visibilidade e uso frequente. No entanto, como os valores relatados associados a essas fontes estão bloqueados, pode haver discrepâncias entre os valores de fonte relatados e reais.

Os seguintes valores relatados são bloqueados para a interface do usuário e para as fontes padrão e podem ser relatados incorretamente:

-   Esses valores da [tabela do sistema operacional/2](https://www.microsoft.com/typography/otspec/os2.htm)da fonte:
    -   xAvgCharWidth
    -   sTypoLineGap
    -   sTypoAscender
    -   sTypoDescender
    -   usWinAscent
    -   usWinDescent
-   O valor [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) definido no cabeçalho da fonte
-   Valores da [tabela vertical de métricas de dispositivo (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   As larguras antecipadas para glifos individuais

Aqui está uma lista das fontes de interface do usuário fornecidas com Windows 8.1 (afetadas por valores bloqueados):

| Nome do script                   | Fonte da interface do usuário               |
|-------------------------------|-----------------------|
| Árabe                        | Interface do Usuário Segoe              |
| Armênia                      | Interface do Usuário Segoe              |
| Bengali (anteriormente Bengali)     | Nirmala UI            |
| Bopomofo                      | Microsoft JhengHei UI |
| Braille                       | Segoe UI Symbol       |
| Bugi                      | Leelawadee UI         |
| Silábico canadense Aboriginal | Gadugi                |
| Cherokee                      | Gadugi                |
| Copta                        | Segoe UI Symbol       |
| Chinês (Simplificado)          | Microsoft YaHei UI    |
| Chinês (Tradicional)         | Microsoft JhengHei UI |
| Cirílico                      | Interface do Usuário Segoe              |
| Devanagari                    | Nirmala UI            |
| Deseret                       | Segoe UI Symbol       |
| Etíope                      | Ebrima                |
| Georgiano                      | Interface do Usuário Segoe              |
| Letra                    | Segoe UI Symbol       |
| Gothic                        | Segoe UI Symbol       |
| Grego                         | Interface do Usuário Segoe              |
| Guzerate                      | Nirmala UI            |
| Gurmukhi                      | Nirmala UI            |
| Hebraico                        | Interface do Usuário Segoe              |
| Itálico antigo                    | Segoe UI Symbol       |
| Javanês                      | Texto do javanês         |
| Japonês                      | Interface do usuário do amMeiryo             |
| canarim                       | Interface do usuário do amMirmala            |
| Khmer                         | Leelawadee UI         |
| Coreano                        | Malgun Gothic         |
| Lao                           | Leelawadee UI         |
| Latim                         | Interface do Usuário Segoe              |
| Malaiala                     | Nirmala UI            |
| Mongol                     | Mongolian Baiti       |
| Myanmar                       | Myanmar Text          |
| N' Ko                          | Ebrima                |
| Ogham                         | Segoe UI Symbol       |
| Ol Chiki                      | Nirmala UI            |
| Turco antigo                    | Segoe UI Symbol       |
| Odia (anteriormente, odia)         | Nirmala UI            |
| Osmanya                       | Ebrima                |
| Phags-Pa                      | Microsoft PhagsPa     |
| Rúnica                         | Segoe UI Symbol       |
| Sora Sompeng                  | Nirmala UI            |
| Sinhala                       | Nirmala UI            |
| Siríaco                        | Estrangelo Edessa     |
| Tai Le                        | Microsoft Tai Le      |
| Tai Lue Novo                   | Microsoft New Tai Lue |
| Tâmil                         | Nirmala UI            |
| Télugo                        | Nirmala UI            |
| Tifinagh                      | Ebrima                |
| Thaana                        | MV Boli               |
| Tailandês                          | Leelawadee UI         |
| Tibetano                       | Microsoft Himalaya    |
| Vai                           | Ebrima                |
| Yi                            | Microsoft Yi Baiti    |



 

Aqui está uma lista das fontes herdadas da interface do usuário que também são afetadas por valores bloqueados:

| Nome do script (Herdado)          | Fonte da interface do usuário (herdada)               |
|-------------------------------|--------------------------------|
| Bengali (anteriormente Bengali)     | Vrinda                         |
| Silábico canadense Aboriginal | Euphemia                       |
| Cherokee                      | Plantagenet                    |
| Chinês (Simplificado)          | Microsoft YaHei e SimSun     |
| Chinês (Tradicional)         | MingLiU e Microsoft JhengHei |
| Devanagari                    | Mangal                         |
| Idiomas europeus            | Tahoma                         |
| Guzerate                      | Shruti                         |
| Gurmukhi                      | Raavi                          |
| Japonês                      | Interface do usuário do Meiryo e MS Gothic        |
| canarim                       | Tunga                          |
| Khmer                         | Khmer                          |
| Coreano                        | Gulim                          |
| Lao                           | Interface do usuário do laosiano                         |
| Malaiala                     | Kartika                        |
| Idiomas do Oriente Médio      | Tahoma                         |
| Odia (anteriormente, odia)         | Kalinga                        |
| Sinhala                     | Iskoola Pota                   |
| Tâmil                         | Latha e Vijaya               |
| Télugo                        | Gautami                        |
| Tailandês                          | Leelawadee e Tahoma          |



 

Essas fontes são usadas como padrões nos aplicativos da Microsoft e também são afetadas por valores bloqueados:

-   Arial
-   Calibri
-   Cambria
-   Consolas
-   Courier New
-   MS Mincho
-   Times New Roman
-   Verdana

### <a name="dynamic-font-metrics"></a>Métricas de fontes dinâmicas

Além das métricas bloqueadas listadas acima, os valores de fonte são relatados com precisão. Se uma fonte for alterada em uma nova versão do Windows, os valores de fontes dinâmicas serão diferentes entre o novo e o antigo. Por exemplo, quando um glifo é adicionado a uma fonte, os valores no cabeçalho da fonte podem ser alterados. O recorte pode resultar se esses valores (que incluem xMin, xMax, yMin e yMax e relatar a caixa delimitadora mínima e máxima para glifos na fonte) foram bloqueados e não relataram valores verdadeiros.

> [!IMPORTANT]
> Se você usar valores de fontes dinâmicas em seu aplicativo (como aqueles em [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)), esses valores serão alterados se as fontes forem modificadas em versões futuras do Windows. Não use esses valores reais em situações em que o texto deve permanecer estático.

 

## <a name="guidelines-for-using-font-metrics"></a>Diretrizes para usar métricas de fonte

-   Métricas de tela de computação e métricas de fonte (por exemplo, largura média) quando um aplicativo é iniciado e usam esses valores para definir o layout de seu aplicativo. Isso fornecerá processamento consistentemente preciso e seu layout responderá às alterações nas fontes ou acomodará o fallback de fonte. Para obter uma visão geral do fallback de fontes e da vinculação de fontes, confira [a globalização passo a passo: fontes](https://msdn.microsoft.com/goglobal/bb688134.aspx). Consulte [usando o fallback de fonte](/windows/desktop/Intl/using-font-fallback) para informações específicas do Uniscribe.
    -   Para calcular uma métrica base, renderize o texto representativo para seu idioma/script pretendido.
    -   Para controles que contenham apenas uma única linha de texto não encapsulado, deite-os para se ajustarem à largura total do texto não cortado.
    -   Para controles com várias linhas, obtenha o comprimento total, divida pelo comprimento do caractere e você tem uma largura sólida com a qual trabalhar. Observe que isso é mais complicado para scripts complexos em que um único "caractere" para o leitor pode ser vários pontos de código.
-   Use sTypoAscender, sTypoDescender e unitsPerEm (da tabela do [sistema operacional/2](https://www.microsoft.com/typography/otspec/os2.htm)) para calcular o espaçamento vertical. sTypoAscender é usado para determinar o deslocamento ideal da parte superior de um quadro de texto para a primeira linha de base e sTypoDescender determina o deslocamento ideal da parte inferior de um quadro de texto para a última linha de base.
-   Se você estiver usando DirectWrite, crie um layout usando [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextLayout** fornece lineGap descendente **ascendente**  +    +   no layout natural. Você pode acessar esses valores específicos com [**\_ \_ métricas de fonte DWRITE**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics). Para obter informações sobre essa interface, consulte [formatação de texto e layout](/windows/desktop/DirectWrite/text-formatting-and-layout).
-   Se você estiver usando GDI, renderizar a tela e, em seguida, inspecionar o layout (por exemplo, o comprimento da linha ou os caracteres por linha) e recalcular os parâmetros de layout final usados no processamento real.
-   Não crie layouts estaticamente com base em valores específicos para versões específicas de fontes. Os valores reais podem mudar de liberação para liberação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**\_métricas de fonte DWRITE \_**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[Tabela do sistema operacional/2](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[Tabela de métricas de dispositivo vertical (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Microsoft Typography: fontes por produto ou família](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Métricas de texto (DirectWrite)](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[Fontes e texto (GDI)](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Tipografia da Microsoft](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 