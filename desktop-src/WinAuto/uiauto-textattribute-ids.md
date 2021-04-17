---
title: Identificadores de atributo de texto (UIAutomationClient. h)
description: Este tópico descreve as constantes nomeadas usadas para identificar atributos de texto de um intervalo de texto de automação da interface do usuário da Microsoft.
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b81c1829c36501b7c0ba4f3862dd9617acfea9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369550"
---
# <a name="text-attribute-identifiers"></a>Identificadores de atributo de texto

Este tópico descreve as constantes nomeadas usadas para identificar atributos de texto de um intervalo de texto de automação da interface do usuário da Microsoft. Essas constantes são usadas com os seguintes métodos:

-   [**ITextRangeProvider:: FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt> <dt>40042</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>AfterParagraphSpacing</strong> , que especifica o tamanho do espaçamento após o parágrafo.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_AnimationStyleAttributeId</strong></dt> <dt>40000</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>AnimationStyle</strong> , que especifica o tipo de animação aplicado ao texto. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>AnimationStyle</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl> <dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt> <dt>40032</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>AnnotationObjects</strong> , que mantém uma matriz de interfaces <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2</strong></a> , uma para cada elemento no intervalo de texto atual que implementa o padrão de controle de <a href="uiauto-implementingannotation.md">anotação</a> . Cada elemento também pode implementar outros padrões de controle conforme necessário para descrever a anotação. Por exemplo, uma anotação que é um comentário também ofereceria suporte ao padrão de controle de <a href="uiauto-implementingtextandtextrange.md">texto</a> . Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor padrão: matriz vazia <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl> <dt><strong>UIA_AnnotationTypesAttributeId</strong></dt> <dt>40031</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>AnnotationTypes</strong> , que mantém uma lista de identificadores de tipo de anotação para um intervalo de texto. Para obter uma lista de valores possíveis, consulte <a href="uiauto-annotation-type-identifiers.md"><strong>identificadores de tipo de anotação</strong></a>. Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_ARRAY</strong>  |  <strong>VT_I4</strong><br/> Valor padrão: matriz vazia <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_BackgroundColorAttributeId</strong></dt> <dt>40001</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>backgroundColor</strong> , que especifica a cor do plano de fundo do texto. Esse atributo é especificado como um <a href="/windows/win32/gdi/colorref">COLORREF</a>; um valor de 32 bits usado para especificar uma cor RGB ou RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt> <dt>40041</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>BeforeParagraphSpacing</strong> , que especifica o tamanho do espaçamento antes do parágrafo.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_BulletStyleAttributeId</strong></dt> <dt>40002</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>BulletStyle</strong> , que especifica o estilo dos marcadores usados no intervalo de texto. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>com marcador</strong></a> .<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_CapStyleAttributeId</strong></dt> <dt>40003</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>CapStyle</strong> , que especifica o estilo de capitalização para o texto. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>CapStyle</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl> <dt><strong>UIA_CaretBidiModeAttributeId</strong></dt> <dt>40039</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>CaretBidiMode</strong> , que indica a direção do fluxo de texto no intervalo de texto. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode</strong></a> . Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl> <dt><strong>UIA_CaretPositionAttributeId</strong></dt> <dt>40038</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>CaretPosition</strong> , que indica se o cursor está no início ou no final de uma linha de texto no intervalo de texto. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>CaretPosition</strong></a> . Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl> <dt><strong>UIA_CultureAttributeId</strong></dt> <dt>40004</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto de <strong>cultura</strong> , que especifica a localidade do texto por LCID (identificador de localidade). <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: localidade da interface do usuário do aplicativo<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl> <dt><strong>UIA_FontNameAttributeId</strong></dt> <dt>40005</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>NomeDaFonte</strong> , que especifica o nome da fonte. Exemplos: &quot; Arial Black &quot; ; &quot; Arial estreito &quot; . A cadeia de caracteres do nome da fonte não está localizada. <br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl> <dt><strong>UIA_FontSizeAttributeId</strong></dt> <dt>40006</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>FontSize</strong> , que especifica o tamanho do ponto da fonte. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl> <dt><strong>UIA_FontWeightAttributeId</strong></dt> <dt>40007</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>EspessuraDaFonte</strong> , que especifica o traço relativo, a espessura ou a boldness da fonte. O atributo <strong>EspessuraDaFonte</strong> é modelado após o membro <strong>LfWeight</strong> da estrutura <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> do GDI e os padrões relacionados, e pode ser um dos seguintes valores:
<ul>
<li>0 = <strong>DontCare</strong></li>
<li>100 = <strong>fino</strong></li>
<li>200 = <strong>ExtraLight</strong> ou <strong>UltraLight</strong></li>
<li>300 = <strong>claro</strong></li>
<li>400 = <strong>normal</strong> ou <strong>regular</strong></li>
<li>500 = <strong>médio</strong></li>
<li>600 = <strong>seminegrito</strong></li>
<li>700 = <strong>negrito</strong></li>
<li>800 = <strong>ExtraBold</strong> ou <strong>UltraBold</strong></li>
<li>900 = <strong>pesado</strong> ou <strong>preto</strong></li>
</ul>
<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_ForegroundColorAttributeId</strong></dt> <dt>40008</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>ForegroundColor</strong> , que especifica a cor de primeiro plano do texto. Esse atributo é especificado como um <a href="/windows/win32/gdi/colorref">COLORREF</a>, um valor de 32 bits usado para especificar uma cor RGB ou RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl> <dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt> <dt>40009</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>HorizontalTextAlignment</strong> , que especifica como o texto é alinhado horizontalmente. Esse atributo é especificado como um valor do tipo enumerado <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>HorizontalTextAlignmentEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt> <dt>40010</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IndentationFirstLine</strong> , que especifica a distância, em pontos, para recuar a primeira linha de um parágrafo. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationLeadingAttributeId</strong></dt> <dt>40011</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IndentationLeading</strong> , que especifica o recuo à esquerda, em pontos. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationTrailingAttributeId</strong></dt> <dt>40012</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IndentationTrailing</strong> , que especifica o recuo à direita, em pontos. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl> <dt><strong>UIA_IsActiveAttributeId</strong></dt> <dt>40036</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IsActive</strong> , que indica se o controle que contém o intervalo de texto tem o foco do teclado (<strong>true</strong>) ou não (<strong>false</strong>). Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl> <dt><strong>UIA_IsHiddenAttributeId</strong></dt> <dt>40013</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IsHidden</strong> , que indica se o texto está oculto (<strong>true</strong>) ou Visible (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl> <dt><strong>UIA_IsItalicAttributeId</strong></dt> <dt>40014</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>isitálico</strong> , que indica se o texto é itálico (<strong>true</strong>) ou não (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl> <dt><strong>UIA_IsReadOnlyAttributeId</strong></dt> <dt>40015</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IsReadOnly</strong> , que indica se o texto é somente leitura (<strong>true</strong>) ou pode ser modificado (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl> <dt><strong>UIA_IsSubscriptAttributeId</strong></dt> <dt>40016</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IsSubscript</strong> , que indica se o texto é subscrito (<strong>true</strong>) ou não (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl> <dt><strong>UIA_IsSuperscriptAttributeId</strong></dt> <dt>40017</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>IsSuperscript</strong> , que indica se o texto é subscrito (<strong>true</strong>) ou não (<strong>false</strong>). <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_LineSpacingAttributeId</strong></dt> <dt>40040</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>LineSpacing</strong> , que especifica o espaçamento entre as linhas de texto.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: &quot; LineSpacingAttributeDefault&quot;<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl> <dt><strong>UIA_LinkAttributeId</strong></dt> <dt>40035</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto de <strong>link</strong> , que contém a interface <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange</strong></a> do intervalo de texto que é o destino de um link interno em um documento. Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor padrão: <strong>nulo</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginBottomAttributeId</strong></dt> <dt>40018</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>MarginBottom</strong> , que especifica o tamanho, em pontos, da margem inferior aplicada à página associada ao intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginLeadingAttributeId</strong></dt> <dt>40019</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>MarginLeading</strong> , que especifica o tamanho, em pontos, da margem à esquerda aplicada à página associada ao intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginTopAttributeId</strong></dt> <dt>40020</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>MarginTop</strong> , que especifica o tamanho, em pontos, da margem superior aplicada à página associada ao intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor de Ddefault: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginTrailingAttributeId</strong></dt> <dt>40021</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>MarginTrailing</strong> , que especifica o tamanho, em pontos, da margem à direita aplicada à página associada ao intervalo de texto. <br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl> <dt><strong>UIA_OutlineStylesAttributeId</strong></dt> <dt>40022</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>OutlineStyles</strong> , que especifica o estilo do contorno do texto. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>OutlineStyles</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_OverlineColorAttributeId</strong></dt> <dt>40023</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>OverlineColor</strong> , que especifica a cor da decoração do texto da linha sobreposta. Esse atributo é especificado como um <a href="/windows/win32/gdi/colorref">COLORREF</a>, um valor de 32 bits usado para especificar uma cor RGB ou RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_OverlineStyleAttributeId</strong></dt> <dt>40024</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>OverlineStyle</strong> , que especifica o estilo da decoração do texto de linha sobreposta. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl> <dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt> <dt>40037</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>SelectionActiveEnd</strong> , que indica o local do cursor relativo a um intervalo de texto que representa o texto atualmente selecionado. Esse atributo é especificado como um valor da enumeração <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>ActiveEnd</strong></a> . Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_StrikethroughColorAttributeId</strong></dt> <dt>40025</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>StrikethroughColor</strong> , que especifica a cor da decoração do texto tachado. Esse atributo é especificado como um <a href="/windows/win32/gdi/colorref">COLORREF</a>, um valor de 32 bits usado para especificar uma cor RGB ou RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt> <dt>40026</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto de <strong>tachado</strong> , que especifica o estilo da decoração de texto tachado. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl> <dt><strong>UIA_StyleIdAttributeId</strong></dt> <dt>40034</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>StyleID</strong> , que indica os estilos de texto em uso para um intervalo de texto. Para obter uma lista de valores possíveis, consulte <a href="uiauto-style-identifiers.md"><strong>identificadores de estilo</strong></a>. Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl> <dt><strong>UIA_StyleNameAttributeId</strong></dt> <dt>40033</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>styleName</strong> , que identifica o nome localizado do estilo de texto em uso para um intervalo de texto. Com suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl> <dt><strong>UIA_TabsAttributeId</strong></dt> <dt>40027</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto de <strong>guias</strong> , que é uma matriz que especifica as paradas de tabulação para o intervalo de texto. Cada elemento da matriz Especifica uma distância, em pontos, da margem à esquerda. <br/> Tipo de variante: <strong>VT_ARRAY | VT_R8</strong><br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl> <dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt> <dt>40028</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>TextFlowDirections</strong> , que especifica a direção do fluxo de texto. Esse atributo é especificado como uma combinação de valores do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>FlowDirections</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_UnderlineColorAttributeId</strong></dt> <dt>40029</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>UnderlineColor</strong> , que especifica a cor da decoração de texto sublinhado. Esse atributo é especificado como um <a href="/windows/win32/gdi/colorref">COLORREF</a>, um valor de 32 bits usado para especificar uma cor RGB ou RGBA. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_UnderlineStyleAttributeId</strong></dt> <dt>40030</dt> </dl></td>
<td style="text-align: left;">Identifica o atributo de texto <strong>sublinestyle</strong> , que especifica o estilo da decoração de texto sublinhado. Esse atributo é especificado como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ITextRangeProvider:: FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
