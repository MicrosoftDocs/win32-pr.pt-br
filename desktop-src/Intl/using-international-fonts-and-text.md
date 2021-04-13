---
description: Em cada versão principal do Windows, há fontes adicionadas para dar suporte a scripts e idiomas internacionais.
ms.assetid: 77b8c200-2682-4651-855a-602f768edc9b
title: Seleção e enumeração de fontes internacionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e5d0d07a0953f72f097f8578f5e32b3ee49093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297704"
---
# <a name="international-font-enumeration-and-selection"></a>Seleção e enumeração de fontes internacionais

Em cada versão principal do Windows, há fontes adicionadas para dar suporte a scripts e idiomas internacionais. Consulte o [suporte de scripts e fontes no Windows](https://msdn.microsoft.com/globalization/mt791278) para as fontes que foram adicionadas em cada versão do Windows desde o Windows 2000, bem como seus scripts, regiões e idiomas com suporte.

## <a name="enumfontfamiliesex"></a>EnumFontFamiliesEx

Para enumerar fontes internacionais em seu aplicativo, você pode usar a função [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa) . **EnumFontFamiliesEx** permite enumerar fontes com base no nome de tipo e conjunto de caracteres, passando um ponteiro para uma estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) que contém as informações de nome de tipo e conjunto de caracteres. Para chamar **EnumFontFamiliesEx**, você pode especificar um nome de tipo de letra ou um conjunto de caracteres, ou você pode solicitar que o esteja disponível. A definição do nome de tipo de fonte de **LOGFONT** como **NULL** enumera todos os nomes de tipos. A definição do campo CharSet **como \_ charset padrão** enumera todos os conjuntos de caracteres.

Observe que charsets são uma noção herdada correspondente a conjuntos de caracteres predefinidos por Unicode. Neste momento, não há nenhum mecanismo para enumerar fontes que dão suporte a scripts arbitrários ou intervalos de caracteres em Unicode. A estrutura [**NEWTEXTMETRICEX**](/windows/win32/api/wingdi/ns-wingdi-newtextmetricexa) passada por [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85)) inclui a estrutura [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) , que inclui declarações mais detalhadas fornecidas pelo desenvolvedor de fontes em quais páginas de código e quais intervalos Unicode são compatíveis com a fonte. Para determinar mais precisamente a quais intervalos de caracteres uma determinada fonte dá suporte, selecione a fonte em um contexto de dispositivo e chame [**GetFontUnicodeRanges**](/windows/win32/api/wingdi/nf-wingdi-getfontunicoderanges). Observe que essa API não dá suporte a planos suplementares Unicode.

## <a name="choosefont"></a>ChooseFont

Você pode usar a função [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) para exibir uma caixa de diálogo comum que permite ao usuário selecionar fontes internacionais com base em CharSet. Você pode especificar um dos três sinalizadores para determinar, com base em charset, quais fontes são exibidas na caixa de diálogo ChooseFont: **CF \_ SCRIPTSONLY**, **CF \_ SELECTSCRIPT** ou **CF \_ NOSCRIPTSEL**.

O **sinalizador \_ SCRIPTSONLY do CF** informa à API para listar fontes para todos os conjuntos de caracteres que não são símbolos ou OEM.

Se você quiser exibir apenas as fontes que abrangem um conjunto de caracteres específico, será necessário especificar o sinalizador **CF \_ SELECTSCRIPT**. Antes de chamar [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)), inicialize o campo *LfCharSet* da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) . Se você estiver interessado em especificar apenas o conjunto de caracteres, defina os outros campos da estrutura **LOGFONT** como **NULL**. Para que o **ChooseFont** Observe a estrutura **LOGFONT** , você também precisa especificar o sinalizador **\_ INITTOLOGFONTSTRUCT do CF** .

Por fim, como com qualquer outro campo na caixa de diálogo fonte, você pode optar por exibir uma caixa de listagem de script em branco. Esse recurso será útil se o usuário tiver realçado várias fontes diferentes abrangendo vários conjuntos de caracteres. Nesse caso, você chamaria [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) com o sinalizador **\_ NOSCRIPTSEL do CF** .

A partir do Windows 7, o [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) implementa o suporte para ocultar as fontes das listas de seleção de fontes. **ChooseFont** listará apenas as fontes mostradas e filtrará as fontes ocultas ao exibir fontes na caixa de listagem. O sinalizador adicional (**CF \_ INACTIVEFONTS**) no membro flags da estrutura [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) é adicionado para permitir que você exiba todas as fontes instaladas na lista de fontes, o mesmo que o **ChooseFont** se comparado antes do Windows 7. Para obter os detalhes das diferenças de comportamento no Windows 7 para a função **ChooseFont** , consulte a [**caixa de diálogo comum do Win32 CHOOSEFONT ()**](../win7appqual/choosefont-win32-common-dialog.md) no [Windows 7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md). Consulte a função **ChooseFont** e a estrutura **ChooseFont** para obter as diferenças da experiência do usuário final no Windows 7.

Observe que charsets são uma noção herdada correspondente a conjuntos de caracteres predefinidos por Unicode. Neste momento, não há nenhum mecanismo para filtrar fontes com base em scripts ou intervalos de caracteres Unicode.

## <a name="font-controls-in-windows-scenic-ribbon"></a>Controles de fonte na faixa de Cenários do Windows

O Windows 7 apresenta a faixa de opção Cenários do Windows, que vem com um conjunto de controles direcionados à seleção de fontes. Esses controles de fonte dão suporte ao novo comportamento de ocultação de fontes do Windows 7. Você pode usar esses controles de fonte para listar apenas as fontes mostradas e permitir que o usuário selecione a fonte.

> [!Note]  
> O suporte para ocultar fontes não está disponível quando a faixa de Cenários do Windows está em execução em qualquer plataforma anterior ao Windows 7.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)
</dt> <dt>

[**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85))
</dt> <dt>

[**Estrutura CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
</dt> <dt>

[**Controles de fonte na faixa de Cenários do Windows**](../windowsribbon/windowsribbon-element-fontcontrol.md)
</dt> <dt>

[**ChooseFont () caixa de diálogo comum do Win32**](../win7appqual/choosefont-win32-common-dialog.md)
</dt> </dl>

 

 
