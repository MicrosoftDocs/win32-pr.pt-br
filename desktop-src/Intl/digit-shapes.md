---
description: O árabe e muitos outros idiomas têm formas clássicas para números que são diferentes dos dígitos ocidentais convencionais mais frequentemente usados nos computadores.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formas de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756917"
---
# <a name="digit-shapes"></a>Formas de dígitos

O árabe e muitos outros idiomas têm formas clássicas para números que são diferentes dos dígitos ocidentais convencionais mais frequentemente usados nos computadores. Para evitar ambigüidade ao nomear essas formas, este documento usa os seguintes nomes do padrão Unicode.



| Nome Unicode dos dígitos                                     | País/região onde usado                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| Dígitos europeus                                                | Europa, Américas e muitos outros países/regiões       |
| Arabic-Indic dígitos                                            | Países/regiões árabes (embora muitos usem dígitos europeus) |
| Outros dígitos nacionais: dígitos índicos, dígitos tailandeses e semelhantes | Vários países/regiões                                    |



 

O Unicode fornece pontos de código separados para cada forma de dígito. Portanto, para acessar formas especiais de dígitos de idioma, seu aplicativo pode usar os códigos de caracteres Unicode relevantes para os dígitos acima, U + 0030 até U + 0039. Esses códigos são sempre exibidos com a forma apropriada, sujeito à disponibilidade da fonte.

Os códigos de caractere Unicode U + 0030 a U + 0039 representam nominalmente os dígitos europeus de 0 a 9, mas sua forma de dígito pode ser alterada. As APIs de texto GDI e DirectWrite fornecem mecanismos para que os aplicativos controlem esse comportamento. (Consulte, por exemplo, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) ou [**IDWriteTextAnalysisSink:: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) O comportamento em alguns controles do Shell e estruturas de interface do usuário pode responder às configurações de localidade do usuário para substituição de dígitos; a [localidade \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE pode ser usada para obter as configurações de substituição de dígitos padrão para localidades diferentes ou para as configurações de área de trabalho do usuário atual para substituição de dígitos.

## <a name="native-digits"></a>Dígitos nativos

Os dígitos nativos são as formas de dígitos escolhidas pelo usuário na folha de propriedades **número** na parte opções regionais e de idiomas do painel de controle. Para localizar a apresentação de dígitos preferida pelo usuário, seu aplicativo usa a função [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) com a constante de [localidade \_ SNATIVEDIGITS](locale-snative-constants.md) que representa as informações de localidade.

> [!Note]  
> Normalmente, os códigos de dígitos Unicode são gerados em rotinas do sistema operacional de tempo de execução. Portanto, os sistemas operacionais de tempo de execução comuns devem ser atualizados para que o aplicativo Inspecione a [localidade \_ SNATIVEDIGITS](locale-snative-constants.md) apropriadamente.

 

## <a name="digit-substitution"></a>Substituição de dígitos

O aplicativo pode usar a substituição de dígitos para informar ao sistema operacional como imprimir dígitos U + 0030 até U + 0039. A [constante \_ IDIGITSUBSTITUTION de localidade](locale-idigitsubstitution.md) controla essa operação.

## <a name="digit-shaping-for-a-single-function"></a>Formatação de dígitos para uma única função

As funções de [ \_ resultados](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)e GCP têm sinalizadores que regem a substituição de códigos Unicode U + 0030 por u + 0039 durante a chamada de função. Esses sinalizadores substituem as configurações regionais no painel de controle, mas não redefinem as configurações. Além disso, eles não substituem os códigos Unicode NADS e nós nesta. Os sinalizadores a seguir estão disponíveis.



| Flags                 | Dígitos usados                      | Usado em                   |
|-----------------------|----------------------------------|---------------------------|
| ETO \_ NUMERICSLATIN    | Dígitos europeus                  | **ExtTextOut**            |
| ETO \_ NUMERICSLOCAL    | Dígitos apropriados para a localidade | **ExtTextOut**            |
| GCP \_ NUMERICSLATIN    | Dígitos europeus                  | **GetCharacterPlacement** |
| GCP \_ NUMERICSLOCAL    | Dígitos apropriados para a localidade | **GetCharacterPlacement** |
| GCPCLASS \_ LATINNUMBER | Dígitos europeus                  | **resultados do GCP \_**          |
| GCPCLASS \_ LOCALNUMBER | Dígitos apropriados para a localidade | **resultados do GCP \_**          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o suporte ao idioma nacional](about-national-language-support.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
