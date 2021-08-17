---
description: Em cada versão principal do Windows, há fontes adicionadas para dar suporte a scripts e linguagens internacionais.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Enumeração e seleção de fontes internacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b28e2dca3937f3513a930f157a364d466f761ed54a53d09c3e2b8b1c89bb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146879"
---
# <a name="international-font-enumeration-and-selection"></a>Enumeração e seleção de fontes internacionais

Em cada versão principal do Windows, há fontes adicionadas para dar suporte a scripts e linguagens internacionais. Consulte Suporte a [scripts](https://msdn.microsoft.com/globalization/mt791278) e fontes no Windows para as fontes que foram adicionadas em cada versão do Windows desde o Windows 2000, bem como seus scripts, regiões e idiomas com suporte.

## <a name="enumfontfamiliesex"></a>Enumfontfamiliesex

Para enumerar fontes internacionais em seu aplicativo, você pode usar a [**função EnumFontFamiliesEx.**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) **EnumFontFamiliesEx** permite enumerar fontes com base no nome da face de tipo e no charset passando um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém o nome da face de tipo e as informações do charset. Para chamar **EnumFontFamiliesEx,** você pode especificar um nome de face de tipo ou um charset ou solicitar o que está disponível. Definir o nome da face de tipo do **LOGFONT** como **NULL** enumera todos os nomes de face de tipo. Definir o campo charset como **DEFAULT \_ CHARSET** enumera todos os conjuntos de caracteres.

Observe que conjuntos de caracteres são uma noção herdda correspondente a conjuntos de caracteres pré-Unicode. No momento, não há nenhum mecanismo para enumerar fontes que suportam scripts arbitrários ou intervalos de caracteres em Unicode. A estrutura [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) passada por [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) inclui a estrutura [**FONTSIGNATURE,**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) que inclui declarações mais detalhadas fornecidas pelo desenvolvedor de fontes sobre quais páginas de código e quais intervalos Unicode a fonte dá suporte. Para determinar com mais precisão quais intervalos de caracteres uma determinada fonte dá suporte, selecione a fonte em um contexto de dispositivo e chame [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Observe que essa API não dá suporte a planos suplementares Unicode.

## <a name="choosefont"></a>Choosefont

Você pode usar a [**função ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) para exibir uma caixa de diálogo comum que permite que o usuário selecione fontes internacionais com base no charset. Você pode especificar um dos três sinalizadores para determinar, com base no charset, quais fontes são exibidas na caixa de diálogo ChooseFont: **CF \_ SCRIPTSONLY,** **CF \_ SELECTSCRIPT** ou **CF \_ NOSCRIPTSEL.**

O **sinalizador \_ CF SCRIPTSONLY** informa à API para listar fontes para todos os conjuntos de caracteres que não são Symbol ou OEM.

Se você quiser exibir apenas fontes que abrangem um determinado charset, precisará especificar o sinalizador **CF \_ SELECTSCRIPT.** Antes de [**chamar ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), inicialize o *campo lfCharSet* da [**estrutura LOGFONT.**](/windows/win32/api/wingdi/ns-wingdi-logfonta) Se você estiver interessado em especificar apenas o conjunto de caracteres, de definir os outros campos da estrutura **LOGFONT** como **NULL.** Para que **ChooseFont** veja a estrutura **LOGFONT,** você também precisa especificar o **sinalizador CF \_ INITTOLOGFONTSTRUCT.**

Por fim, assim como com qualquer outro campo na caixa de diálogo Fonte, você pode optar por exibir uma caixa de listagem de script em branco. Essa funcionalidade é útil se o usuário realça várias fontes diferentes que abrangem vários conjuntos de caracteres. Nesse caso, você chamaria [**ChooseFont com**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) o **sinalizador CF \_ NOSCRIPTSEL.**

Começando com Windows 7, [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) implementa suporte para ocultar fontes de listas de seleção de fontes. **ChooseFont** listará apenas as fontes mostradas e filtrará as fontes ocultas ao exibir fontes na caixa de listagem. O sinalizador adicional (**CF \_ INACTIVEFONTS**) no membro de sinalizadores da estrutura [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) é adicionado para permitir que você ex exibir todas as fontes instaladas na lista de fontes, o mesmo que **ChooseFont** se comportou antes Windows 7. Para obter os detalhes das diferenças de comportamento no Windows 7 para a função **ChooseFont,** consulte Caixa de diálogo comum [**ChooseFont() Win32**](../win7appqual/choosefont-win32-common-dialog.md) no Guia de Qualidade do Aplicativo [Windows 7](../win7appqual/windows-7-application-quality-cookbook.md). Consulte a **função ChooseFont** e a **estrutura CHOOSEFONT** para ver as diferenças de experiência do usuário final Windows 7.

Observe que conjuntos de caracteres são uma noção herdda correspondente a conjuntos de caracteres pré-Unicode. No momento, não há nenhum mecanismo para filtrar fontes com base em scripts Unicode ou intervalos de caracteres.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Controles de fonte na faixa Windows faixa de opções Ribbon

Windows 7 apresenta o Windows faixa de opções Ribbon, que vem com um conjunto de controles direcionados à seleção de fonte. Esses controles de fonte suportam o novo comportamento Windows ocultação de fonte 7. Você pode usar esses controles de fonte para listar apenas as fontes mostradas e permitir que o usuário selecione a fonte.

> [!Note]  
> O suporte para ocultar fontes não está disponível quando a faixa de opções Windows faixa de opções Ribbon está em execução em qualquer plataforma antes Windows 7.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Enumfontfamiliesex**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**Choosefont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**Estrutura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Controles de fonte na faixa Windows faixa de opções Ribbon**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**Caixa de diálogo Comum ChooseFont() Win32**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
