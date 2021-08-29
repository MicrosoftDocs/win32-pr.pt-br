---
title: Identificadores de propriedade do elemento automation (UIAutomationClient.h)
description: Este tópico descreve as constantes nomeadas que identificam as propriedades dos elementos Automação da Interface do Usuário Microsoft.
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f23198c149113caf4c7e22d9a7dbffc9bec91f4b25a4ca4b7c296516b39f30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052294"
---
# <a name="automation-element-property-identifiers"></a>Identificadores de propriedade do elemento automation

Este tópico descreve as constantes nomeadas que identificam as propriedades dos elementos Automação da Interface do Usuário Microsoft.



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
<td style="text-align: left;"><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>AcceleratorKey,</strong> que é uma cadeia de caracteres que contém as combinações de tecla de acelerador (também chamada de tecla de atalho) para o elemento de automação. <br/> As combinações de teclas de atalho invocam uma ação. Por exemplo, CTRL+O geralmente é usado para invocar a caixa de diálogo Abrir arquivo comum. Um elemento de automação que tem a <strong>propriedade AcceleratorKey</strong> pode implementar o padrão de controle <a href="uiauto-implementinginvoke.md">Invoke</a> para a ação equivalente ao comando de atalho.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>AccessKey,</strong> que é uma cadeia de caracteres que contém o caractere de chave de acesso para o elemento de automação.<br/> Uma chave de acesso (às vezes chamada de mnemônico) é um caractere no texto de um menu, item de menu ou rótulo de um controle, como um botão, que ativa a função de menu associada. Por exemplo, para abrir o menu Arquivo, para o qual a chave de acesso normalmente é F, o usuário pressionaria ALT+F.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade AnnotationObjects,</strong> que é uma lista de objetos de anotação em um documento, como comentário, header, rodapé e assim por diante.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade AnnotationTypes,</strong> que é uma lista dos tipos de anotações em um documento, como comentário, header, rodapé e assim por diante.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>AriaProperties,</strong> que é uma cadeia de caracteres formatada que contém as informações de propriedade ARIA (Accessible Rich Internet Application) para o elemento de automação. Para obter mais informações sobre como mapear estados e propriedades do ARIA para Automação da Interface do Usuário propriedades e funções, consulte Automação da Interface do Usuário especificação de aplicativos de Internet avançada acessíveis <a href="uiauto-ariaspecification.md">do W3C.</a><br/> <strong>AriaProperties</strong> é uma coleção de pares Nome/Valor com delimitadores de <strong>=</strong> (igual a) e <strong>;</strong> (ponto e vírgula), por exemplo, &quot; checked=true;disabled=false &quot; . A (faixa invertida) é usada como um caractere de escape quando esses <strong>\</strong> caracteres delimiter ou <strong>\</strong> aparecem nos valores. Por motivos de segurança e outros motivos, a implementação dessa propriedade pelo provedor pode tomar medidas para validar as propriedades originais do ARIA; no entanto, não é necessário.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>AriaRole,</strong> que é uma cadeia de caracteres que contém as informações de função ARIA (Accessible Rich Internet Application) para o elemento de automação. Para obter mais informações sobre como mapear funções do ARIA Automação da Interface do Usuário tipos de controle, consulte Automação da Interface do Usuário especificação de aplicativos de Internet acessíveis <a href="uiauto-ariaspecification.md">do W3C.</a><br/>
<blockquote>
[!Note]<br />
Como opção, o agente do usuário também pode oferecer uma descrição localizada da função ARIA do W3C na <strong>propriedade LocalizedControlType.</strong> Quando a cadeia de caracteres localizada não for especificada, o sistema fornecerá a cadeia de caracteres <strong>LocalizedControlType</strong> padrão para o elemento .
</blockquote>
<br/> <br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>AutomationId,</strong> que é uma cadeia de caracteres que contém o identificador Automação da Interface do Usuário (ID) do elemento de automação.<br/> Quando estiver disponível, a <strong>AutomationId</strong> de um elemento deve ser a mesma em qualquer instância do aplicativo, independentemente do idioma local. O valor deve ser exclusivo entre elementos irmãos, mas não necessariamente exclusivo em toda a área de trabalho. Por exemplo, várias instâncias de um aplicativo ou várias exibições de pasta no Microsoft Windows Explorer podem conter elementos com a mesma propriedade <strong>AutomationId,</strong> como &quot; SystemMenuBar &quot; .<br/> Embora o suporte para <strong>AutomationId</strong> seja sempre recomendado para melhor suporte a testes automatizados, essa propriedade não é obrigatória. Onde há suporte, <strong>AutomationId</strong> é útil para criar um script de automação de teste que é executado independentemente da linguagem de interface do usuário. Os clientes não devem fazer suposições sobre os valores <strong>AutomationId</strong> expostos por outros aplicativos. Não há garantia de que <strong>AutomationId</strong> seja estável em diferentes versões ou builds de um aplicativo.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade BoundingRectangle,</strong> que especifica as coordenadas do retângulo que inclui completamente o elemento de automação. O retângulo é expresso em coordenadas de tela físicas. Ele pode conter pontos que não são clicáveis se a forma ou a região clicável do item de interface do usuário for irregular ou se o item for obscurecido por outros elementos da interface do usuário.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: [0,0,0,0]<br/>
<blockquote>
[!Note]<br />
Essa propriedade será <strong>NULL</strong> se o item não estiver exibindo uma interface do usuário no momento.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>CenterPoint,</strong> que especifica as coordenadas de ponto X e Y do elemento de automação. O espaço de coordenadas é o que o provedor considera logicamente uma página.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>ClassName,</strong> que é uma cadeia de caracteres que contém o nome da classe para o elemento de automação atribuído pelo desenvolvedor de controle.<br/> O nome da classe depende da implementação do provedor Automação da Interface do Usuário e, portanto, nem sempre está em um formato padrão. No entanto, se o nome da classe for conhecido, ele poderá ser usado para verificar se um aplicativo está trabalhando com o elemento de automação esperado.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade ClickablePoint,</strong> que é um ponto no elemento de automação que pode ser clicado. Um elemento não poderá ser clicado se ele estiver completamente ou parcialmente obscurecido por outra janela.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>ControllerFor,</strong> que é uma matriz de elementos de automação que são manipulados pelo elemento de automação que dá suporte a essa propriedade.<br/> <strong>ControllerFor</strong> é usado quando um elemento de automação afeta um ou mais segmentos da interface do usuário do aplicativo ou da área de trabalho; caso contrário, será difícil associar o impacto da operação de controle aos elementos da interface do usuário.<br/> Esse identificador é comumente usado para <a href="/windows/uwp/design/accessibility/accessible-text-requirements">acessibilidade de sugestão automática.</a><br/> Tipo de variante para provedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo de variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade ControlType,</strong> que é uma classe que identifica o tipo do elemento de automação. <strong>ControlType</strong> define características dos elementos da interface do usuário por primitivos de controle de interface do usuário conhecidos, como botão ou caixa de seleção. <br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Use o valor padrão somente se o elemento de automação representar um tipo completamente novo de controle.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade Culture,</strong> que contém um identificador de localidade para o elemento de automação (por exemplo, <code>0x0409</code> para en-US ou inglês &quot; &quot; (Estados Unidos)).<br/> Cada localidade tem um identificador exclusivo, um valor de 32 bits que consiste em um identificador de idioma e um identificador de ordem de classificação. O identificador de localidade é uma abreviação numérica internacional padrão e tem os componentes necessários para identificar exclusivamente uma das localidades definidas pelo sistema operacional instaladas. Para obter mais informações, consulte <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">Constantes e cadeias de caracteres do identificador de idioma.</a><br/> Essa propriedade pode existir por controle, mas normalmente só está disponível em um nível de aplicativo.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>DescribedBy,</strong> que é uma matriz de elementos que fornecem mais informações sobre o elemento de automação.<br/> <strong>DescribedBy</strong> é usado quando um elemento de automação é explicado por outro segmento da interface do usuário do aplicativo. Por exemplo, a propriedade pode apontar para um elemento de texto de &quot; 2.529 itens em 85 grupos, 10 itens selecionados em um objeto de lista &quot; personalizada complexo. Em vez de usar o modelo de objeto para clientes para digerir informações semelhantes, a propriedade <strong>DescribedBy</strong> pode oferecer acesso rápido ao elemento de interface do usuário que já pode oferecer informações úteis do usuário final que descrevem o elemento de interface do usuário.<br/> Tipo de variante para provedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo de variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>FillColor,</strong> que especifica a cor usada para preencher o elemento de automação. Esse atributo é especificado como um COLORREF, um valor de 32 bits usado para especificar uma cor RGB ou RGBA.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade FillType,</strong> que especifica o padrão usado para preencher o elemento de automação, como nenhum, cor, gradiente, imagem, padrão e assim por diante.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>FlowsFrom,</strong> que é uma matriz de elementos de automação que sugere a ordem de leitura antes do elemento de automação atual. Suporte a partir do Windows 8.<br/> A <strong>propriedade FlowsFrom</strong> especifica a ordem de leitura quando os elementos de automação não são expostos ou estruturados na mesma ordem de leitura que o usuário percebe. Embora a <strong>propriedade FlowsFrom</strong> possa especificar vários elementos anteriores, ela normalmente contém apenas o elemento anterior na ordem de leitura.<br/> Tipo de variante para provedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo de variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>FlowsTo,</strong> que é uma matriz de elementos de automação que sugere a ordem de leitura após o elemento de automação atual.<br/> A <strong>propriedade FlowsTo</strong> especifica a ordem de leitura quando os elementos de automação não são expostos ou estruturados na mesma ordem de leitura que o usuário percebe. Embora a <strong>propriedade FlowsTo</strong> possa especificar vários elementos bem-sucedidos, ela normalmente contém apenas o próximo elemento na ordem de leitura.<br/> Tipo de variante para provedores: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo de variante para clientes: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valor padrão: matriz vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>FrameworkId,</strong> que é uma cadeia de caracteres que contém o nome da estrutura de interface do usuário subjacente à qual o elemento de automação pertence.<br/> O <strong>FrameworkId permite</strong> que os aplicativos cliente processem elementos de automação de maneira diferente, dependendo da estrutura de interface do usuário específica. Exemplos de valores de propriedade &quot; incluem Win32, &quot; &quot; WinForm &quot; e &quot; &quot; DirectUI.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td style="text-align: left;">A <strong>propriedade FullDescription expõe</strong> uma cadeia de caracteres localizada que pode conter texto de descrição estendida para um elemento. <strong>FullDescription pode</strong> conter uma descrição mais completa de um elemento do que pode ser apropriada para o elemento <strong>Name</strong>.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade HasKeyboardFocus,</strong> que é um valor booliana que indica se o elemento de automação tem o foco do teclado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>HeadingLevel,</strong> que indica o nível de título de um Automação da Interface do Usuário elemento.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>HelpText,</strong> que é uma cadeia de caracteres de texto de ajuda associada ao elemento de automação.<br/> A <strong>propriedade HelpText</strong> pode ser suportada com texto de espaço reservado que aparece em controles de edição ou lista. Por exemplo, Digite texto aqui para pesquisa é um bom candidato à propriedade HelpText para um controle de edição que coloca o texto antes da &quot; &quot; entrada real do usuário. <strong></strong> No entanto, ele não é adequado para a propriedade name do controle de edição.<br/> Quando <strong>Há suporte para HelpText,</strong> a cadeia de caracteres deve corresponder ao idioma da interface do usuário do aplicativo ou ao idioma de interface do usuário padrão do sistema operacional.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade IsContentElement,</strong> que é um valor booliana que especifica se o elemento aparece na exibição de conteúdo da árvore de elementos de automação. Para obter mais informações, consulte <a href="uiauto-treeoverview.md">Visão geral Automação da Interface do Usuário árvore.</a><br/>
<blockquote>
[!Note]<br />
Para que um elemento apareça na exibição de conteúdo, a propriedade <strong>IsContentElement</strong> e a propriedade <strong>IsControlElement</strong> devem ser <strong>TRUE.</strong>
</blockquote>
<br/> <br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>TRUE</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade IsControlElement,</strong> que é um valor booliana que especifica se o elemento aparece na exibição de controle da árvore de elementos de automação. Para obter mais informações, consulte <a href="uiauto-treeoverview.md">Visão geral Automação da Interface do Usuário árvore.</a><br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>TRUE</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade IsDataValidForForm,</strong> que é um valor booliana que indica se o valor inserido ou selecionado é válido para a regra de formulário associada ao elemento de automação. Por exemplo, se o usuário digitou &quot; 425-555-5555 para um campo de cep que exige 5 ou &quot; 9 dígitos, a propriedade <strong>IsDataValidForForm</strong> poderá ser definida como <strong>FALSE</strong> para indicar que os dados não são válidos.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>

<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>IsDialog,</strong> que é um valor booliana que indica se o elemento de automação é uma janela de diálogo. Por exemplo, tecnologia adaptativa, como leitores de tela normalmente falam o título da caixa de diálogo, o controle focalizado na caixa de diálogo e, em seguida, o conteúdo da caixa de diálogo até o controle focalizado ( Você deseja salvar suas alterações antes de &quot; fechar &quot; ). Para janelas padrão, um leitor de tela normalmente fala o título da janela seguido pelo controle focalizado. A <strong>propriedade IsDialog</strong> pode ser definida como <strong>TRUE</strong> para indicar que o aplicativo cliente deve tratar o elemento como uma janela de diálogo.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>

<tr class="even">
<td style="text-align: left;"><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade IsEnabled,</strong> que é um valor booliana que indica se o item de interface do usuário referenciado pelo elemento de automação está habilitado e pode ser interagido.<br/> Quando o estado habilitado de um controle é <strong>FALSE,</strong>supõe-se que os controles filho também não estão habilitados. Os clientes não devem esperar eventos alterados por propriedade de elementos filho quando o estado do controle pai for alterado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade IsKeyboardFocusable,</strong> que é um valor booliana que indica se o elemento de automação pode aceitar o foco do teclado.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>IsOffscreen,</strong> que é um valor booliana que indica se o elemento de automação é totalmente rolado para fora da exibição (por exemplo, um item em uma caixa de listagem que está fora do visualizador do objeto de contêiner) ou recolhido fora da exibição (por exemplo, um item em um menu ou exibição de árvore ou em uma janela minimizada). Se o elemento tiver um ponto clicável que possa fazer com que ele receba o foco, o elemento será considerado na tela enquanto uma parte do elemento está fora da tela.<br/> O valor da propriedade não é afetado pela oclusão por outras janelas ou se o elemento está visível em um monitor específico.<br/> Se a <strong>propriedade IsOffscreen</strong> for <strong>TRUE</strong>, o elemento da interface do usuário será rolado para fora da tela ou recolhido. O elemento está temporariamente oculto, mas permanece na percepção do usuário final e continua sendo incluído no modelo de interface do usuário. O objeto pode ser levado de volta à exibição rolando, clicando em uma lista de lista e assim por diante.<br/> Objetos que o usuário final não percebe ou que estão ocultos programaticamente (por exemplo, uma caixa de diálogo que foi descartada, mas o objeto subjacente ainda é armazenado em cache pelo aplicativo) não devem estar na árvore de elementos de automação em primeiro lugar (em vez de definir o estado de &quot; &quot; <strong>IsOffscreen</strong> como <strong>TRUE).</strong><br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>IsPassword</strong> , que é um valor booliano que indica se o elemento Automation contém conteúdo protegido ou uma senha.<br/> Quando a propriedade <strong>IsPassword</strong> é <strong>verdadeira</strong> e o elemento tem o foco do teclado, um aplicativo cliente deve desabilitar o eco do teclado ou os comentários de entrada do teclado que podem expor as informações protegidas do usuário. A tentativa de acessar a propriedade <strong>Value</strong> do elemento protegido (controle de edição) pode causar a ocorrência de um erro.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>isperiférica</strong> , que é um valor booliano que indica se o elemento Automation representa a interface do usuário periférica. A interface do usuário do periférico é exibida e dá suporte à interação de usuários, mas não assume o foco do teclado quando ele é exibido. Exemplos de interface do usuário de periféricos incluem pop-ups, submenus, menus de contexto ou notificações flutuantes. Com suporte a partir de Windows 8.1.<br/> Quando a propriedade <strong>isperipheral</strong> é <strong>true</strong>, um aplicativo cliente não pode assumir que o foco foi realizado pelo elemento, mesmo que ele esteja atualmente interativo no teclado.<br/> Essa propriedade é relevante para esses tipos de controle:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>IsRequiredForForm</strong> , que é um valor booliano que indica se o elemento de automação deve ser preenchido em um formulário.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>Propriedade ItemProperty</strong> , que é uma cadeia de caracteres de texto que descreve o status de um item do elemento Automation.<br/> O item de <strong>status</strong> permite que um cliente para verificar se um elemento está transmitindo o status de um item, bem como qual é o status. Por exemplo, um item associado a um contato em um aplicativo de mensagens pode estar &quot; ocupado &quot; ou &quot; conectado &quot; .<br/> Quando o <strong>objectstatus</strong> tem suporte, a cadeia de caracteres deve corresponder ao idioma da interface do usuário do aplicativo ou ao idioma da interface do usuário padrão do sistema operacional.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>ItemType</strong> , que é uma cadeia de caracteres de texto que descreve o tipo do elemento de automação.<br/> <strong>ItemType</strong> é usado para obter informações sobre itens em uma lista, exibição de árvore ou grade de dados. Por exemplo, um item em uma exibição de diretório de arquivo pode ser um &quot; arquivo de documento &quot; ou uma &quot; pasta &quot; .<br/> Quando <strong>ItemType</strong> tem suporte, a cadeia de caracteres deve corresponder ao idioma da interface do usuário do aplicativo ou ao idioma da interface do usuário padrão do sistema operacional.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>LabeledBy</strong> , que é um elemento de automação que contém o rótulo de texto para este elemento.<br/> Essa propriedade pode ser usada para recuperar, por exemplo, o rótulo de texto estático para uma caixa de combinação.<br/> Tipo de variante: <strong>VT_UNKNOWN</strong><br/> Valor padrão: <strong>nulo</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade de <strong>ponto</strong> de referência, que é um <a href="landmark-type-identifiers.md"><strong>identificador de tipo de ponto de referência</strong></a> associado a um elemento.<br/> A propriedade de <strong>ponto de referência</strong> descreve um elemento que representa um grupo de elementos. Por exemplo, um ponto de referência de pesquisa pode representar um conjunto de controles relacionados para pesquisa.<br/> Se <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> for usado, <strong>UIA_LocalizedLandmarkTypePropertyId</strong> será necessário para descrever o ponto de referência personalizado.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>Level</strong> , que é um inteiro baseado em 1 associado a um elemento Automation.<br/> A propriedade <strong>Level</strong> descreve o local de um elemento dentro de uma estrutura hierárquica hierárquica ou quebrada. Por exemplo, uma lista com marcadores/numerada, títulos ou outros itens de dados estruturados podem ter várias relações pai/filho. <strong>Nível</strong> descreve em que local na estrutura o item está localizado.<br/> É recomendável usar o <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">padrão de controle CustomNavigation</a> em tandem com <strong>Level</strong>.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>LiveSetting</strong> , que é suportada por um elemento Automation que representa uma região dinâmica. A propriedade <strong>LiveSetting</strong> indica o &quot; nível de educador &quot; que um cliente deve usar para notificar o usuário sobre as alterações na região dinâmica. Essa propriedade pode ser um dos valores da enumeração <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting</strong></a> . Com suporte a partir de Windows 8.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>LocalizedControlType</strong> , que é uma cadeia de caracteres de texto que descreve o tipo de controle que o elemento Automation representa. A cadeia de caracteres deve conter apenas caracteres minúsculos:
<ul>
<li>Correto: &quot; botão&quot;</li>
<li>Incorreto: &quot; botão&quot;</li>
</ul>
<br/> Quando <strong>LocalizedControlType</strong> não é especificado pelo provedor de elemento, a cadeia de caracteres localizada padrão é fornecida pela estrutura, de acordo com o tipo de controle do elemento (por exemplo, &quot; botão &quot; para o tipo de controle de <a href="uiauto-supportbuttoncontroltype.md">botão</a> ). Um elemento Automation com o tipo de controle <strong>personalizado</strong> deve oferecer suporte a uma cadeia de caracteres de tipo de controle localizado que representa a função do elemento (por exemplo, &quot; seletor de cor &quot; para um controle personalizado que permite aos usuários escolher e especificar cores).<br/> Quando um valor personalizado é fornecido, a cadeia de caracteres deve corresponder ao idioma da interface do usuário do aplicativo ou ao idioma da interface do usuário padrão do sistema operacional.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td style="text-align: left;">Identifica o <strong>LocalizedLandmarkType</strong>, que é uma cadeia de caracteres de texto que descreve o tipo de ponto de referência que o elemento Automation representa.<br/> Isso deve ser usado em conjunto com <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> no entanto, <strong>LocalizedLandmarkType</strong> deve sempre ter precedência sobre o <strong>ponto de referência</strong> e ser usado para descrever o ponto de referência antes de o <strong>ponto</strong>de entrada.<br/> A cadeia de caracteres deve corresponder ao idioma da interface do usuário do aplicativo ou ao idioma da interface do usuário padrão do sistema operacional.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>Name</strong> , que é uma cadeia de caracteres que contém o nome do elemento Automation.<br/> A propriedade <strong>Name</strong> deve ser igual ao texto do rótulo na tela. Por exemplo, o <strong>nome</strong> deve &quot; procurar &quot; um elemento de botão com o rótulo &quot; procurar &quot; . A propriedade <strong>Name</strong> não deve incluir o caractere mnemônico para as chaves de acesso (ou seja, &quot; & &quot; ), que é sublinhada na apresentação de texto da interface do usuário. Além disso, a propriedade <strong>Name</strong> não deve ser uma versão estendida ou modificada do rótulo na tela porque a inconsistência entre o nome e o rótulo pode causar confusão entre os aplicativos cliente e os usuários.<br/> Quando o texto do rótulo correspondente não é visível na tela, ou quando é substituído por gráficos, um texto alternativo deve ser escolhido. O texto alternativo deve ser conciso, intuitivo e localizado para o idioma da interface do usuário do aplicativo ou para o idioma da interface do usuário padrão do sistema operacional. O texto alternativo não deve ser uma descrição detalhada dos detalhes visuais, mas uma descrição concisa da função ou do recurso da interface do usuário como se fosse rotulada por texto simples. por exemplo, o botão de menu Iniciar Windows é denominado &quot; Start &quot; (botão) em vez de &quot; Windows logotipo em gráficos de esfera redonda azul &quot; (botão). Para obter mais informações, consulte <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">criando equivalentes de texto para imagens</a>.<br/> Quando um rótulo de interface do usuário usa gráficos de texto (por exemplo, usando &quot; >> &quot; para um botão que adiciona um item da esquerda para a direita), a propriedade <strong>Name</strong> deve ser substituída por uma alternativa de texto apropriada (por exemplo, &quot; Add &quot; ). No entanto, a prática de usar gráficos de texto como um rótulo de interface do usuário não é recomendada devido a questões de localização e de acessibilidade.<br/> A propriedade <strong>Name</strong> não deve incluir as informações de tipo ou função de controle, como &quot; Button &quot; ou &quot; List &quot; ; caso contrário, ela entrará em conflito com o texto da propriedade <strong>LocalizedControlType</strong> quando essas duas propriedades forem acrescentadas (muitas tecnologias assistenciais existentes fazem isso).<br/> A propriedade <strong>Name</strong> não pode ser usada como um identificador exclusivo entre irmãos. No entanto, desde que seja consistente com a apresentação da interface do usuário, o mesmo valor de <strong>nome</strong> pode ter suporte entre os pares. Para a automação de teste, os clientes devem considerar o uso da propriedade <strong>AutomationId</strong> ou <strong>runtimeId</strong> .<br/> Os controles de texto nem sempre precisam ter a propriedade <strong>Name</strong> idêntica ao texto exibido no controle, contanto que o padrão de <strong>texto</strong> também tenha suporte.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade NativeWindowHandle,</strong> que é um inteiro que representa o identificador (<strong>HWND</strong>) da janela do elemento de automação, se existir; caso contrário, essa propriedade será 0.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade OptimizeForVisualContent,</strong> que é um valor booliana que indica se o provedor expõe apenas elementos visíveis. Um provedor pode usar essa propriedade para otimizar o desempenho ao trabalhar com partes muito grandes de conteúdo. Por exemplo, como o usuário pagina por meio de uma grande parte do conteúdo, o provedor pode destruir elementos de conteúdo que não estão mais visíveis. Quando um elemento de conteúdo é destruído, o provedor deve retornar o <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> código de erro. Suporte a partir do Windows 8.<br/> Tipo de variante: <strong>VT_BOOL</strong><br/> Valor padrão: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>Orientation,</strong> que indica a orientação do controle representado pelo elemento de automação. A propriedade é expressa como um valor do tipo enumerado <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType.</strong></a><br/> A <strong>propriedade Orientation</strong> é suportada por controles, como barras de rolagem e controles deslizantes, que podem ter uma orientação vertical ou horizontal. Caso contrário, ele sempre poderá <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>ser OrientationType_None</strong></a>, o que significa que o controle não tem nenhuma orientação.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>OutlineColor,</strong> que especifica a cor usada para o contorno do elemento de automação. Esse atributo é especificado como <strong>um COLORREF</strong>, um valor de 32 bits usado para especificar uma cor RGB ou RGBA.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>OutlineThickness,</strong> que especifica a largura do contorno do elemento de automação.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade PositionInSet,</strong> que é um inteiro baseado em 1 associado a um elemento de automação. <strong>PositionInSet</strong> descreve o local ordinal do elemento dentro de um conjunto de elementos que são considerados irmãos.<br/> <strong>PositionInSet</strong> funciona em coordenação com a <strong>propriedade SizeOfSet</strong> para descrever o local ordinal no conjunto.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade ProcessId,</strong> que é um inteiro que representa o identificador de processo (ID) do elemento de automação.<br/> O ID (identificador de processo) é atribuído pelo sistema operacional. Ele pode ser visto na <strong>coluna PID</strong> da <strong>guia Processos</strong> no Gerenciador de Tarefas.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade ProviderDescription,</strong> que é uma cadeia de caracteres formatada que contém as informações de origem do provedor Automação da Interface do Usuário para o elemento de automação, incluindo informações de proxy.<br/> Tipo de variante: <strong>VT_BSTR</strong><br/> Valor padrão: cadeia de caracteres vazia<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>Rotation,</strong> que especifica o ângulo de rotação em unidades não especificadas.<br/> Tipo de variante: <strong>VT_R8</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>RuntimeId,</strong> que é uma matriz de inteiros que representa o identificador de um elemento de automação.<br/> O identificador é exclusivo na área de trabalho, mas tem a garantia de ser exclusivo somente na interface do usuário da área de trabalho na qual ele foi gerado. Os identificadores podem ser reutilizados ao longo do tempo.<br/> O formato de <strong>RuntimeId</strong> pode mudar. O identificador retornado deve ser tratado como um valor opaco e usado somente para comparação; por exemplo, para determinar se um elemento de automação está no cache.<br/> Tipo de variante: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td style="text-align: left;">Identifica a propriedade <strong>Size,</strong> que especifica a largura e a altura do elemento de automação.<br/> Tipo de variante: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valor padrão: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade SizeOfSet,</strong> que é um inteiro baseado em 1 associado a um elemento de automação. <strong>SizeOfSet</strong> descreve a contagem de elementos de automação em um grupo ou conjunto que são considerados irmãos.<br/> <strong>SizeOfSet</strong> funciona em coordenação com a <strong>propriedade PositionInSet</strong> para descrever a contagem de itens no conjunto.<br/> Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td style="text-align: left;">Identifica a <strong>propriedade VisualEffects,</strong> que é um campo de bits que especifica efeitos no elemento de automação, como sombra, reflexão, brilho, bordas suaves ou bevel.<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Tipo de variante: <strong>VT_I4</strong><br/> Valor padrão: 0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho XP\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2003 \|\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Recuperando propriedades de elementos Automação da Interface do Usuário dados](uiauto-propertiesforclients.md)
</dt> </dl>
