---
title: Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento
description: os controles hospedados na barra de comandos da faixa de opções estão sujeitos a regras de layout que são impostas pelo Windows estrutura da faixa de opções e com base em uma combinação de comportamentos padrão e modelos de layout (ambos definidos pelo framework e personalizados), conforme declarado na marcação da faixa de opções. Essas regras definem os comportamentos de layout adaptável da estrutura da faixa de opção que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opção em tempo de execução.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows Faixa de faixas, personalizando
- Faixa de faixas, personalizando
- Windows Faixa de SizeDefinition, modelos de modelo
- Faixa de SizeDefinition, modelos de modelo
- Windows Faixa de, modelos personalizados
- Faixa de, modelos personalizados
- personalizando a faixa de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eff1a9d1b2582d5386ce6ea0e02e20cfb5a806e1aaa4a98529474a756b5a8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933488"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Personalizando uma faixa de guia por meio de definições de tamanho e políticas de dimensionamento

os controles hospedados na barra de comandos da faixa de opções estão sujeitos a regras de layout que são impostas pelo Windows estrutura da faixa de opções e com base em uma combinação de comportamentos padrão e modelos de layout (ambos definidos pelo framework e personalizados), conforme declarado na marcação da faixa de opções. Essas regras definem os comportamentos de layout adaptável da estrutura da faixa de opção que influenciam como os controles na barra de comandos se adaptam a vários tamanhos de faixa de opção em tempo de execução.

-   [Introdução](#introduction)
    -   [Modelos de faixa de SizeDefinition](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Modelos personalizados](#custom-templates)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O layout adaptável, conforme definido pela estrutura da faixa de opção, é a capacidade de todos os controles dentro da interface do usuário da faixa de opção ajustarem dinamicamente sua organização, tamanho, formato e escala relativa com base nas alterações no tamanho da faixa de opção em tempo de execução.

A estrutura expõe a funcionalidade de layout adaptável por meio de um conjunto de elementos de marcação dedicados à especificação e à personalização de vários comportamentos de layout. Uma coleção de modelos, chamada [**SizeDefinitions**](windowsribbon-element-sizedefinition.md), é definida pela estrutura, cada um com suporte para vários cenários de controle e layout. No entanto, a estrutura também dá suporte a modelos personalizados caso os modelos predefinidos não forneçam a experiência de interface do usuário ou os layouts exigidos por um aplicativo.

Para exibir controles em um layout preferencial em um tamanho de faixa de opções específico, os modelos predefinidos e os modelos personalizados funcionam em conjunto com o elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) . Esse elemento contém um manifesto de preferências de tamanho que a estrutura usa como um guia ao renderizar a faixa de opções.

> [!Note]  
> A estrutura da faixa de opção fornece comportamentos de layout padrão com base em um conjunto de heurísticas internas para a organização e apresentação de controles em tempo de execução sem a necessidade de modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidos. No entanto, esse recurso destina-se apenas a fins de protótipo.

 

### <a name="ribbon-sizedefinition-templates"></a>Modelos de faixa de SizeDefinition

A estrutura da faixa de opção fornece um conjunto abrangente de modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) que especificam o comportamento de tamanho e layout para um [grupo](windowsribbon-controls-group.md) de controles de faixa de opção. Esses modelos abrangem os cenários mais comuns para organizar controles em um aplicativo da faixa de faixas.

Para impor uma experiência de usuário consistente em aplicativos de faixa de faixas, cada modelo de [**SizeDefinition**](windowsribbon-element-sizedefinition.md) impõe restrições aos controles ou à família de controles com suporte.

Por exemplo, a família de botões de controles inclui:

-   [Botão](windowsribbon-controls-button.md)
-   [Botão de alternância](windowsribbon-controls-togglebutton.md)
-   [Botão suspenso](windowsribbon-controls-dropdownbutton.md)
-   [Botão de divisão](windowsribbon-controls-splitbutton.md)
-   [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)
-   [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md)
-   [Seletor de cores suspensa](windowsribbon-controls-dropdowncolorpicker.md)

Embora a família de entrada de controles inclua:

-   [Caixa de combinação](windowsribbon-controls-combobox.md)
-   [Controle giratório](windowsribbon-controls-spinner.md)

A [caixa de seleção](windowsribbon-controls-checkbox.md) e a [Galeria de faixa de](windowsribbon-controls-inribbongallery.md) opções não pertencem à família de botões ou à família de entrada. Esses dois controles podem ser usados apenas onde indicado explicitamente em um modelo [**SizeDefinition**](windowsribbon-element-sizedefinition.md) .

A seguir está uma lista dos modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) com uma descrição do layout e dos controles permitidos por cada modelo.

> [!IMPORTANT]
> Se os controles declarados na marcação não forem mapeados exatamente para o tipo de controle, a ordem e a quantidade definidos no modelo associado, um [erro de validação](windowsribbon-compilationerrors.md) será registrado pelo [compilador de marcação](windowsribbon-intentcl.md) e a compilação será encerrada.

 



OneButton

Um controle de família de botões.<br/> Há suporte apenas para o tamanho do grupo grande.<br/>

![imagem do modelo oneButton sizedefinition.](images/overviews/sizedefinition-onebutton.png)

TwoButtons

Dois controles de família de botões.<br/> Há suporte apenas para tamanhos de grupo grande e médio.<br/>

![imagem do modelo twobuttons grande sizedefinition.](images/overviews/sizedefinition-twobuttons-large.png)

![Picture of twobuttons Medium sizedefinition template.](images/overviews/sizedefinition-twobuttons-medium.png)

ThreeButtons

Controles da família de três botões.<br/> Há suporte apenas para tamanhos de grupo grande e médio.<br/>

![imagem do modelo threebuttons grande sizedefinition.](images/overviews/sizedefinition-threebuttons-large.png)

![Picture of threebuttons Medium sizedefinition template.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Controles da família de três botões.<br/> O primeiro botão é apresentado em destaque em todos os três tamanhos.<br/>

![imagem do modelo threebuttons-onebigandtwosmall grande sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Picture of threebuttons-onebigandtwosmall Medium sizedefinition template.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![imagem do modelo threebuttons-onebigandtwosmall Small sizedefinition.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

ThreeButtonsAndOneCheckBox

Controles de família de botões acompanhados por um único controle de caixa de seleção.<br/> Há suporte apenas para tamanhos de grupo grande e médio.<br/>

![imagem do modelo threebuttonsandonecheckbox grande sizedefinition.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Picture of threebuttonsandonecheckbox Medium sizedefinition template.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

FourButtons

Controles de família de botões.<br/>

![imagem do modelo fourbuttons grande sizedefinition.](images/overviews/sizedefinition-fourbuttons-large.png)

![Picture of fourbuttons Medium sizedefinition template.](images/overviews/sizedefinition-fourbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do fourbuttons.](images/overviews/sizedefinition-fourbuttons-small.png)

FiveButtons

Controles da família de cinco botões.<br/>

![imagem do modelo fivebuttons grande sizedefinition.](images/overviews/sizedefinition-fivebuttons-large.png)

![Picture of fivebuttons Medium sizedefinition template.](images/overviews/sizedefinition-fivebuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do fivebuttons.](images/overviews/sizedefinition-fivebuttons-small.png)

FiveOrSixButtons

Os cinco controles da família de botões e um sexto botão opcional.<br/>

![imagem do modelo fiveorsixbuttons grande sizedefinition.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Picture of fiveorsixbuttons Medium sizedefinition template.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do fiveorsixbuttons.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

SixButtons

Seis controles da família de botões.<br/>

![imagem do modelo sixbuttons grande sizedefinition.](images/overviews/sizedefinition-sixbuttons-large.png)

![Picture of sixbuttons Medium sizedefinition template.](images/overviews/sizedefinition-sixbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do sixbuttons.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Seis botões – controles da família (apresentação alternativa).<br/>

![imagem do modelo sixbuttons-twocolumns grande sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![sixbuttons-twocolumns Medium sizedefinition template.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![imagem do modelo sixbuttons-twocolumns Small sizedefinition.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

SevenButtons

Sete controles de família de botões.<br/>

![imagem do modelo sevenbuttons grande sizedefinition.](images/overviews/sizedefinition-sevenbuttons-large.png)

![imagem do modelo sevenbuttons mediumsizedefinition.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do sevenbuttons.](images/overviews/sizedefinition-sevenbuttons-small.png)

EightButtons

Os oito controles da família de botões.<br/>

![imagem do modelo eightbuttons-lastthreesmall grande sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Picture of eightbuttons-lastthreesmall Medium sizedefinition template.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![imagem do modelo eightbuttons-lastthreesmall Small sizedefinition.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Oito botões – controles da família (apresentação alternativa).<br/>

> [!Note]  
> Todos os elementos de controle declarados com este modelo devem estar contidos em dois elementos de [**Control**](windowsribbon-element-controlgroup.md) : um para os cinco primeiros elementos e um para os últimos três elementos.

<br/> O exemplo a seguir demonstra a marcação necessária para este modelo.<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![imagem do modelo eightbuttons grande sizedefinition.](images/overviews/sizedefinition-eightbuttons-large.png)

![Picture of eightbuttons Medium sizedefinition template.](images/overviews/sizedefinition-eightbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do eightbuttons.](images/overviews/sizedefinition-eightbuttons-small.png)

NineButtons

Nove controles de família de botões.

![imagem do modelo ninebuttons grande sizedefinition.](images/overviews/sizedefinition-ninebuttons-large.png)

![Picture of ninebuttons Medium sizedefinition template.](images/overviews/sizedefinition-ninebuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do ninebuttons.](images/overviews/sizedefinition-ninebuttons-small.png)

TenButtons

Dez controles de família de botões.

![imagem do modelo tenbuttons grande sizedefinition.](images/overviews/sizedefinition-tenbuttons-large.png)

![Picture of tenbuttons Medium sizedefinition template.](images/overviews/sizedefinition-tenbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do tenbuttons.](images/overviews/sizedefinition-tenbuttons-small.png)

ElevenButtons

11 botões-controles da família.

![imagem do modelo elevenbuttons grande sizedefinition.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Picture of elevenbuttons Medium sizedefinition template.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![imagem do modelo de sizedefinition pequeno do elevenbuttons.](images/overviews/sizedefinition-elevenbuttons-small.png)

OneFontControl

Um [**FontControl**](windowsribbon-element-fontcontrol.md).

Há suporte apenas para tamanhos de grupo grande e médio.

> [!IMPORTANT]
> A estrutura não oferece suporte à inclusão de um [**FontControl**](windowsribbon-element-fontcontrol.md) em uma definição de modelo personalizado.

 

![imagem do modelo onefontcontrol grande sizedefinition.](images/overviews/sizedefinition-onefontcontrol-large.png)

![Picture of onefontcontrol Medium sizedefinition template.](images/overviews/sizedefinition-onefontcontrol-medium.png)

OneInRibbonGallery

Um controle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .

Há suporte apenas para tamanhos de grupos grandes e pequenos.

![imagem do modelo oneinribbongallery grande sizedefinition.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![imagem do modelo de sizedefinition pequeno do oneinribbongallery.](images/overviews/sizedefinition-oneinribbongallery-small.png)

InRibbonGalleryAndBigButton

Um controle [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) e um controle de família de botões.

Há suporte apenas para tamanhos de grupos grandes e pequenos.

![imagem do modelo inribbongalleryandbigbutton grande sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![imagem do modelo de sizedefinition pequeno do inribbongalleryandbigbutton.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Um controle [de galeria na faixa de faixas](windowsribbon-controls-inribbongallery.md) e dois ou três controles de família de botões.

A Galeria recolhe a representação pop-up em tamanhos de grupo médio e pequeno.

![imagem do modelo inribbongalleryandbuttons-galleryscalesfirst grande sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Picture of inribbongalleryandbuttons-galleryscalesfirst Medium sizedefinition template.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![imagem do modelo inribbongalleryandbuttons-galleryscalesfirst Small sizedefinition.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

ButtonGroups

Uma organização complexa de controles de família de botão 32 (a maioria deles é opcional).

> [!Note]  
> Além do botão de tamanho normal opcional do modelo de ButtonGroups grande, todos os elementos de controle declarados com esse modelo devem estar contidos nos elementos do [**controlador de controle**](windowsribbon-element-controlgroup.md) .

 

O exemplo a seguir demonstra a marcação necessária para exibir todos os elementos de controle de 32 (obrigatórios e opcionais) com este modelo.


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![imagem do modelo ButtonGroups grande sizedefinition.](images/overviews/sizedefinition-buttongroups-large.png)

![Picture of ButtonGroups Medium sizedefinition template.](images/overviews/sizedefinition-buttongroups-medium.png)

![imagem do modelo de sizedefinition pequeno do ButtonGroups.](images/overviews/sizedefinition-buttongroups-small.png)

ButtonGroupsAndInputs

Dois controles de família de entrada (o segundo é opcional) seguido por uma disposição complexa de 29 botões de família de botão (a maioria deles é opcional).

Há suporte apenas para tamanhos de grupo grande e médio.

> [!Note]  
> Todos os elementos de controle declarados com esse modelo devem estar contidos em elementos de [**Control**](windowsribbon-element-controlgroup.md) .

 

O exemplo a seguir demonstra a marcação necessária para exibir todos os elementos de controle (obrigatórios e opcionais) com este modelo.


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![imagem do modelo buttongroupsandinputs grande sizedefinition.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Picture of buttongroupsandinputs Medium sizedefinition template.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

BigButtonsAndSmallButtonsOrInputs

Dois controles de família de botões (ambos opcionais) seguidos por dois ou três controles de botão ou de família de entrada.

Há suporte apenas para tamanhos de grupo grande e médio.

![imagem do modelo bigbuttonsandsmallbuttonsorinputs grande sizedefinition.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Picture of bigbuttonsandsmallbuttonsorinputs Medium sizedefinition template.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Exemplo de SizeDefinition básico

O exemplo de código a seguir fornece uma demonstração básica de como declarar um modelo [**SizeDefinition**](windowsribbon-element-sizedefinition.md) na marcação da faixa de opções.

O *OneInRibbonGallery* [**SizeDefinition**](windowsribbon-element-sizedefinition.md) é usado para esse exemplo específico, mas todos os modelos de estrutura são especificados de maneira semelhante.


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Exemplo de SizeDefinition complexo com políticas de dimensionamento

O comportamento de recolhimento dos modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) pode ser controlado por meio do uso de políticas de dimensionamento na marcação da faixa de faixas.

O elemento [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) contém um manifesto de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) e declarações de [**escala**](windowsribbon-element-scale.md) que especificam preferências de layout adaptável para um ou mais elementos de [**grupo**](windowsribbon-element-group.md) quando a faixa de opções é redimensionada.

> [!Note]  
> É altamente recomendável que os detalhes da política de dimensionamento adequados sejam especificados de forma que a maioria, se não todos, os elementos do [**grupo**](windowsribbon-element-group.md) sejam associados a um elemento [**Scale**](windowsribbon-element-scale.md) , no qual o atributo *size* é igual a `Popup` . Isso permite que a estrutura processe a faixa de opções com o menor tamanho possível e ofereça suporte à maior variedade de dispositivos de vídeo, antes de introduzir automaticamente um mecanismo de rolagem.

 

O exemplo de código a seguir demonstra um manifesto [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) que especifica uma preferência de [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) [**SizeDefinition**](windowsribbon-element-sizedefinition.md) para cada um dos quatro grupos de controles em uma guia **página inicial** . Além disso, os elementos [**Scale**](windowsribbon-element-scale.md) são especificados para influenciar o comportamento de recolhimento, em ordem de tamanho decrescente, de cada grupo.


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>Modelos personalizados

Se os comportamentos de layout padrão e os modelos [**SizeDefinition**](windowsribbon-element-sizedefinition.md) predefinidos não oferecerem a flexibilidade ou o suporte para um cenário de layout específico, os modelos personalizados serão suportados pela estrutura da faixa de opções por meio do elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) .

Os modelos personalizados podem ser declarados de duas maneiras: um método autônomo usando o elemento [**Ribbon. SizeDefinitions**](windowsribbon-element-ribbon-sizedefinitions.md) para declarar modelos reutilizáveis, nomeados ou um método embutido específico do [**grupo**](windowsribbon-element-group.md).

### <a name="standalone-template"></a>Modelo autônomo

O exemplo de código a seguir ilustra um modelo personalizado básico e reutilizável.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>Modelo embutido

Os exemplos de código a seguir ilustram um modelo personalizado embutido básico para um grupo de quatro botões.

Esta seção de código mostra as declarações de comando para um grupo de botões. Recursos de imagem grandes e pequenos também são especificados aqui.


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



Esta seção de código demonstra como definir modelos de [**GroupSizeDefinition**](windowsribbon-element-groupsizedefinition.md) grandes, médios e pequenos para exibir os quatro botões em vários tamanhos e layouts. A Declaração [**ScalingPolicy**](windowsribbon-element-scalingpolicy.md) para a guia define qual modelo é usado para um grupo de controles com base no tamanho da faixa de medida e no espaço exigido pela guia ativa.


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



As imagens a seguir mostram como os modelos do exemplo anterior são aplicados à interface do usuário da faixa de opções para acomodar uma diminuição no tamanho da faixa de opções.



|  Tipo  |      Imagem                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| Grande  | ![imagem de um modelo personalizado grande embutido.](images/overviews/sizedefinition-custom-large.png)   |
| Médio | ![imagem de um modelo personalizado médio embutido.](images/overviews/sizedefinition-custom-medium.png) |
| Small  | ![imagem de um modelo personalizado pequeno embutido.](images/overviews/sizedefinition-custom-small.png)   |
| Pop-up  | ![imagem de um modelo personalizado pop-up embutido.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**SizeDefinition**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Escala**](windowsribbon-element-scale.md)
</dt> <dt>

[**Grupo**](windowsribbon-element-group.md)
</dt> </dl>

 

 





