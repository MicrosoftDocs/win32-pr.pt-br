---
title: Controle de fonte
description: para simplificar a integração e a configuração do suporte a fontes em aplicativos que exigem recursos de processamento de palavras e edição de texto, a estrutura da faixa de opções Windows fornece um controle de fonte especializado que expõe uma ampla gama de propriedades de fonte, como nome do tipo, estilo, tamanho do ponto e efeitos.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 106163c03c506e438ffcffa261ebd7e3a2115e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470722"
---
# <a name="font-control"></a>Controle de fonte

para simplificar a integração e a configuração do suporte a fontes em aplicativos que exigem recursos de processamento de palavras e edição de texto, a estrutura da faixa de opções Windows fornece um controle de fonte especializado que expõe uma ampla gama de propriedades de fonte, como nome do tipo, estilo, tamanho do ponto e efeitos.

-   [Introdução](#introduction)
-   [Uma experiência consistente](#a-consistent-experience)
-   [Integração e configuração fáceis](#easy-integration-and-configuration)
-   [Alinhamento com estruturas de texto GDI comuns](#alignment-with-common-gdi-text-structures)
-   [Adicionar um FontControl](#add-a-fontcontrol)
    -   [Declarando um FontControl na marcação](#declaring-a-fontcontrol-in-markup)
    -   [Propriedades de controle de fonte](#font-control-properties)
-   [Definir um manipulador de comando FontControl](#define-a-fontcontrol-command-handler)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O controle de fonte é um controle composto que consiste em botões, botões de alternância, caixas de listagem suspensas e caixas de combinação, todos usados para especificar uma determinada propriedade de fonte ou opção de formatação.

a captura de tela a seguir mostra o controle de fonte da faixa de opções no WordPad para Windows 7.

![captura de tela do elemento fontcontrol com o atributo richfont definido como true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Uma experiência consistente

Como um controle de faixa de opção interno, o controle de fonte melhora a funcionalidade geral de gerenciamento de fontes, seleção e formatação e fornece uma experiência de usuário sofisticada e consistente em todos os aplicativos de faixa de faixas.

Essa experiência consistente inclui

-   Formatação padronizada e seleção de fontes em aplicativos de faixa de opção.
-   Representação de fonte padronizada em aplicativos de faixa de faixas.
-   automático, no Windows 7, ativação de fonte baseada na configuração **mostrar** ou **ocultar** para cada fonte no painel de controle de **fontes** . O controle de fonte exibe apenas as fontes que estão definidas para **Mostrar**.
    > [!Note]  
    > no Windows Vista, o painel de controle de **fontes** não oferece a funcionalidade de **mostrar** ou **ocultar** , portanto, todas as fontes são ativadas.

     

-   Gerenciamento de fontes que está disponível diretamente do controle.

    A captura de tela a seguir mostra que o painel de controle de **fontes** pode ser acessado diretamente do controle de fonte.

    ![captura de tela da lista família de fontes no WordPad para Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Suporte para visualização automática.
-   Exposição de fontes que são mais relevantes para um usuário, como
    -   Listas de fontes localizadas para usuários internacionais.
    -   Listas de fontes com base no dispositivo de entrada.

    > [!Note]  
    > o suporte para essa funcionalidade não está disponível em nenhuma plataforma com mais de Windows 7.

     

## <a name="easy-integration-and-configuration"></a>Integração e configuração fáceis

Ao fornecer uma funcionalidade padrão, reutilizável e facilmente consumida, o controle de fonte da faixa de faixas alivia a carga da integração do suporte a fontes em um aplicativo.

Os detalhes da seleção e da formatação de fontes são encapsulados em um elemento lógico autocontido que

-   Elimina o gerenciamento complexo de interdependências de controle típicas de implementações de controle de fonte.
-   Requer um único manipulador de comando para todas as funcionalidades expostas pelos subcontroles de controles Font.

Esse manipulador de comando único permite que o controle de fonte gerencie a funcionalidade de vários subcontroles internamente; um subcontrole nunca interage diretamente com o aplicativo, independentemente de sua função.

Outros recursos do controle de fonte incluem

-   A geração automática de reconhecimento de DPI de um WYSIWYG (o que você vê é o que você obtém) representação de bitmap para cada fonte no menu **da família de fontes** .
-   integração [do Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .
-   Bitmaps e dicas de ferramentas localizadas da família de fontes.
-   Enumeração de fontes, agrupamento e metadados para gerenciar e apresentar fontes.
    > [!Note]  
    > o suporte para essa funcionalidade não está disponível em nenhuma plataforma com mais de Windows 7.

     

-   Os seletores de cor de cor do **texto** e de **realce de texto** que espelham o comportamento do [selecionador de cores suspenso](windowsribbon-controls-dropdowncolorpicker.md) da faixa de bits.
-   Suporte à visualização automática por todos os subcontroles baseados na Galeria de controles de fontes: **família de fontes**, **tamanho da fonte**, **cor do texto** e **cor de realce do texto**.

## <a name="alignment-with-common-gdi-text-structures"></a>Alinhamento com estruturas de texto GDI comuns

os componentes da pilha de texto [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) são usados para expor a seleção de fontes e a funcionalidade de formatação por meio do controle fonte da faixa de opção. Os vários recursos de fonte com suporte da estrutura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), da [estrutura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e da [estrutura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) são expostos por meio dos subcontroles incluídos no controle de fonte.

Os subcontroles exibidos no controle de fonte dependem do modelo *FontType* declarado na marcação da faixa de lista. os modelos *fonttype* (discutidos mais detalhadamente na seção a seguir) são projetados para alinhar-se com as estruturas de texto common [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .

## <a name="add-a-fontcontrol"></a>Adicionar um FontControl

Esta seção descreve as etapas básicas para adicionar um controle de fonte a um aplicativo da faixa de faixas.

### <a name="declaring-a-fontcontrol-in-markup"></a>Declarando um FontControl na marcação

Assim como outros controles de faixa de forma, o controle de fonte é declarado em marcação com um elemento [**FontControl**](windowsribbon-element-fontcontrol.md) e associado a uma declaração de comando por meio de uma ID de comando. Quando o aplicativo é compilado, a ID de comando é usada para associar o comando a um manipulador de comando no aplicativo host.

> [!Note]  
> Se nenhuma ID de comando for declarada com [**FontControl**](windowsribbon-element-fontcontrol.md) na marcação, então uma será gerada pela estrutura.

 

Como os subcontroles do controle de fonte não são expostos diretamente, a personalização do controle de fonte é limitada a três modelos de layout de *FontType* definidos pelo Framework.

A personalização adicional do controle de fonte pode ser realizada pela combinação do modelo de layout com atributos [**FontControl**](windowsribbon-element-fontcontrol.md) , como *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* e *IsUnderlineButtonVisible*.

> [!Note]  
> A funcionalidade de fonte além daquela exposta pelos modelos e atributos de controle de fonte padrão requer uma implementação de controle de fonte personalizada que está fora do escopo deste artigo.

 

A tabela a seguir lista os modelos de controle de fonte e o tipo de controle de edição com os quais cada modelo está alinhado.



| Modelo      | Suporta                                                                 |
|---------------|--------------------------------------------------------------------------|
| FontOnly      | [Estrutura LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| FontWithColor | [Estrutura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| RichFont      | [Estrutura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

A tabela a seguir lista os controles associados a cada modelo e identifica os controles que são opcionais para um modelo associado.



Controles

Modelos

**RichFont**

**FontWithColor**

**FontOnly**

Padrão

Opcional

Padrão

Opcional

Padrão

Opcional

Caixa de combinação de **tamanho da fonte**

Sim

Não

Sim

Não

Sim

Não

Caixa de combinação **da família de fontes**

Sim

Não

Sim

Não

Sim

Não

Botão **aumentar fonte**

Sim

Sim

Sim

Sim

\-

\-

Botão **reduzir fonte**

Sim

Sim

Sim

Sim

\-

\-

Botão **negrito**

Sim

Não

Sim

Não

Sim

Não

Botão **itálico**

Sim

Não

Sim

Não

Sim

Não

Botão **sublinhado**

Sim

Não

Sim

Sim

Sim

Sim

Botão **tachado**

Sim

Não

Sim

Sim

Sim

Sim

Botão **subscrito**

Sim

Não

\-

\-

\-

\-

Botão **sobrescrito**

Sim

Não

\-

\-

\-

\-

Botão de **cor de realce de texto**

Sim

Não

Sim

Sim

\-

\-

Botão de **cor do texto**

Sim

Não

Sim

Não

\-

\-



 

Quando o comportamento de layout de um controle de fonte é declarado, a estrutura da faixa de faixas fornece um modelo de layout *SizeDefinition* opcional, `OneFontControl` , que define duas configurações de subcontrole com base no tamanho da faixa de opção e no espaço disponível para o controle de fonte. Para obter mais informações, consulte [Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Adicionando um FontControl a uma faixa de faixas

Os exemplos de código a seguir demonstram os requisitos básicos de marcação para adicionar um controle de fonte a uma faixa de opções:

Esta seção de código mostra a marcação de declaração de comando [**FontControl**](windowsribbon-element-fontcontrol.md) , incluindo os comandos de [**guia**](windowsribbon-element-tab.md) e de [**grupo**](windowsribbon-element-group.md) que são necessários para exibir um controle na [**faixa de faixas**](windowsribbon-element-ribbon.md).


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



Esta seção de código mostra a marcação necessária para declarar e associar um [**FontControl**](windowsribbon-element-fontcontrol.md) a um [**comando**](windowsribbon-element-command.md) por meio de uma ID de comando. Esse exemplo específico inclui as declarações de [**guia**](windowsribbon-element-tab.md) e de [**grupo**](windowsribbon-element-group.md) , com preferências de dimensionamento.


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Adicionando um FontControl a um ContextPopup

A adição de um controle de fonte a um [pop-up de contexto](windowsribbon-controls-contextpopup.md) requer um procedimento semelhante ao da adição de um controle de fonte à faixa de tipos. No entanto, um controle de fonte em um [**Minibarra**](windowsribbon-element-minitoolbar.md) é restrito ao conjunto de subcontroles padrão que são comuns a todos os modelos de controle de fonte: **família de fontes**, **tamanho da fonte**, **negrito** e **itálico**.

Os exemplos de código a seguir demonstram os requisitos básicos de marcação para adicionar um controle de fonte a um [Popup de contexto](windowsribbon-controls-contextpopup.md):

Esta seção de código mostra a marcação de declaração de comando [**FontControl**](windowsribbon-element-fontcontrol.md) que é necessária para exibir um **FontControl** no [**ContextPopup**](windowsribbon-element-contextpopup.md).


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



Esta seção de código mostra a marcação necessária para declarar e associar um [**FontControl**](windowsribbon-element-fontcontrol.md) a um comando por meio de uma ID de comando.


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>Dicas de tecla

Cada subcontrole no controle de fonte da faixa de bits pode ser acessado por meio de um atalho de teclado ou KeyTip. Esse KeyTip é predefinido e atribuído a cada subcontrole da estrutura.

Se um valor de atributo *KeyTip* for atribuído ao elemento [**FontControl**](windowsribbon-element-fontcontrol.md) na marcação, esse valor será adicionado como um prefixo ao KeyTip definido pelo Framework.

> [!Note]  
> O aplicativo deve impor uma regra de caractere único para esse prefixo.

 

A tabela a seguir lista as keytips definidas pela estrutura. 


| Subcontrole | KeyTip | 
|-------------|--------|
| Família de fontes | F | 
| Estilo da fonte | T | 
| Tamanho da fonte | S | 
| Aumentar fonte | G | 
| Reduzir fonte | K | 
| Negrito | B | 
| Itálico | I | 
| Underline | U | 
| Tachado | X | 
| Sobrescrito | Y ou Z<blockquote>[!Note]<br />Se o atributo <em>KeyTip</em> não for declarado na marcação, o KeyTip padrão será Y; caso contrário, o KeyTip padrão será <em>KeyTip</em> + Z.</blockquote><br /> | 
| Subscrito | A | 
| Cor da fonte | C | 
| Realce de fonte | H | 




 

o prefixo recomendado para uma faixa de opções do Interface de Usuário Multilíngue (MUI) EN-US é ' F ', conforme mostrado no exemplo a seguir.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



A captura de tela a seguir ilustra as dicas de teclado do controle de fonte conforme elas são definidas no exemplo anterior.

![captura de tela das dicas de tecla fontcontrol no wordpad para windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>O arquivo de recurso da faixa de opções

Quando o arquivo de marcação é compilado, um arquivo de recurso que contém todas as referências de recurso para o aplicativo de Faixa de Opções é gerado.

Exemplo de um arquivo de recurso simples:


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>Propriedades do controle de fonte

A estrutura ribbon define uma coleção de chaves [de propriedade](windowsribbon-reference-properties.md) para o Controle de Fonte e seus subcontroles constituintes.

Normalmente, uma propriedade Controle de Fonte é atualizada na interface do usuário da faixa de opções invalidando o Comando associado ao controle por meio de uma chamada para o [**método IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) O evento de invalidação é tratado e as atualizações de propriedade definidas pelo método de retorno de chamada [**IUICommandHandler::UpdateProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)

O método de retorno de chamada [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consulta um valor de propriedade atualizado até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle é revelado na interface do usuário da faixa de opções ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o [**método IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)

 

A tabela a seguir lista as chaves de propriedade associadas ao Controle de Fonte.



| Chave de propriedade                                                                                                                  | Observações                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_FontProperties PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Expõe, em agregação como um [objeto IPropertyStore,](/windows/win32/api/propsys/nn-propsys-ipropertystore) todas as propriedades de subcontrole do Controle de Fonte.<br/> A estrutura consulta essa propriedade quando é passado como o valor de sinalizadores na chamada para `UI_INVALIDATIONS_VALUE` [**IUIFramework::InvalidateUICommand.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) <br/> |
| [Fonte \_ PKEY da \_ interface do usuárioPropriedades \_ AlteradasPropriedades](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Expõe, em agregação como um objeto [**IUISimplePropertySet,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) somente propriedades de subcontrole do Controle de Fonte que foram alteradas.<br/>                                                                                                                                                                                                        |
| [Dica de \_ tecla PKEY \_ da interface do usuário](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                                                                                                                                                                                      |
| [PKEY \_ da interface do usuário \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Dá [**suporte a IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) [**e IUIFramework::SetUICommandProperty.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)                                                                                                                                                                  |



 

Além das propriedades com suporte do próprio Controle de Fonte, [a](windowsribbon-reference-properties.md) estrutura de Faixa de Opções também define uma chave de propriedade para cada subcontrole do Controle de Fonte. Essas chaves de propriedade e seus valores são expostos pela estrutura por meio de uma implementação de interface [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) que define os métodos para gerenciar uma coleção, também chamada de conjunto de propriedades, de pares de nome e valor.

O aplicativo converte as estruturas de fonte em propriedades acessíveis por meio dos métodos de interface [IPropertyStore.](/windows/win32/api/propsys/nn-propsys-ipropertystore) Esse modelo enfatiza a distinção entre o Controle de Fonte e os componentes de pilha de texto Windows Graphics Device Interface (GDI) ( Estrutura[LOGFONT,](/windows/win32/api/wingdi/ns-wingdi-logfonta) [Estrutura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e [Estrutura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) que têm suporte na estrutura.

A tabela a seguir lista os controles individuais e suas chaves de propriedade associadas.



| Controles                 | Chave de propriedade                                                                                                                                                                                                                                                           | Observações                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tamanho da fonte**            | [Tamanho de \_ \_ FontProperties de PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Quando uma série de texto de tamanho heterogêneo é realçada, a estrutura de Faixa de Opções define o controle Tamanho da fonte como em branco e o valor de  [ \_ \_ FontProperties \_ PKEY](windowsribbon-reference-properties-uipkey-fontproperties-size.md) da interface do usuário como 0. Quando o **botão Aumentar fonte** **ou** Reduzir fonte é clicado, todo o texto realçado é resizado, mas a diferença relativa em tamanhos de texto é preservada.                                                                                                                                                    |
| **Família de fontes**          | [Família \_ \_ fontProperties PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | Os nomes de família de fontes GDI variam de acordo com a localidade do sistema. Dessa forma, se o valor da Família [ \_ \_ fontProperties \_ PKEY](windowsribbon-reference-properties-uipkey-fontproperties-family.md) da interface do usuário for preservado entre as sessões do aplicativo, esse valor deverá ser recuperado em cada nova sessão.                                                                                                                                                                                                                                                                            |
| **Aumentar fonte**            | [Tamanho de \_ \_ FontProperties de PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Consulte **Tamanho da fonte.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Reduzir fonte**          | [Tamanho de \_ \_ FontProperties de PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Consulte **Tamanho da fonte.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Negrito**                 | [\_ \_ FontProperties PKEY da interface do usuário em \_ negrito](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Itálico**               | [Fonte \_ de PKEY \_ da interface do \_ usuárioPropriedades itálico](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Underline**            | [\_Sublinhado FontProperties de PKEY \_ \_ da interface do usuário](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Tachado**        | [Tachado \_ de \_ FontProperties de PKEY da interface do \_ usuário](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Subscrito**            | [\_ \_ FontProperties \_ VerticalPositioning da interface do usuário PKEY](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Se o **botão Subscrito** estiver definido, o **Superscript** também não poderá ser definido.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Sobrescrito**          | [\_ \_ FontProperties \_ VerticalPositioning da interface do usuário PKEY](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Se o **botão Superscript** estiver definido, o **Subscrito** também não poderá ser definido.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Cor do realçando texto** | [Interface do usuário \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ PKEY \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Fornece a mesma funcionalidade que o `HighlightColors` modelo do [**elemento DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)<br/> É altamente recomendável que apenas um valor de cor **de realçamento** de texto inicial seja definido pelo aplicativo. O último valor selecionado deve ser preservado e não definido quando o cursor é reposicionado dentro de um documento. Isso permite acesso rápido à última seleção do usuário e o seletor de cores não precisa ser reaberto.<br/> As travas de cores não podem ser personalizadas.<br/> |
| **Cor do texto**           | [Interface do usuário \_ PKEY \_ FontProperties \_ ForegroundColor,](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) [UI \_ PKEY \_ FontProperties \_ ForegroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | Fornece a mesma funcionalidade que o `StandardColors` modelo do [**elemento DropDownColorPicker.**](windowsribbon-element-dropdowncolorpicker.md)<br/> É altamente recomendável que apenas um valor **de cor de** texto inicial seja definido pelo aplicativo. O último valor selecionado deve ser preservado e não definido quando o cursor é reposicionado dentro de um documento. Isso permite acesso rápido à última seleção do usuário e o seletor de cores não precisa ser reaberto.<br/> As travas de cores não podem ser personalizadas.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Definir um manipulador de comandos FontControl

Esta seção descreve as etapas necessárias para vincular um Controle de Fonte a um manipulador de comandos.

> [!WARNING]
> Qualquer tentativa de selecionar um swatch de cor do seletor de cores de um Controle de Fonte poderá resultar em uma violação de acesso se nenhum manipulador de comandos estiver associado ao controle.

 

O exemplo de código a seguir demonstra como vincular comandos declarados na marcação a um manipulador de comandos.


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



O exemplo de código a seguir ilustra como implementar o [**método IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para um Controle de Fonte.


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



O exemplo de código a seguir ilustra como implementar o [**método IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) para um controle de fonte.


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento FontControl**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Propriedades do controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Exemplo de FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

