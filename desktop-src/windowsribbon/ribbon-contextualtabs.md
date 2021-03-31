---
title: Exibindo guias contextuais
description: Em um aplicativo do Windows Ribbon Framework, uma guia contextual é um controle de guia oculto que é exibido na linha da guia quando um objeto no espaço de trabalho do aplicativo, como uma imagem, é selecionado ou realçado.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Faixa de medida do Windows, guias contextuais
- Faixa de guia, guias contextuais
- exibindo guias contextuais da faixa de das do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641116"
---
# <a name="displaying-contextual-tabs"></a>Exibindo guias contextuais

Em um aplicativo do Windows Ribbon Framework, uma guia contextual é um controle de [guia](windowsribbon-controls-tab.md) oculto que é exibido na linha da guia quando um objeto no espaço de trabalho do aplicativo, como uma imagem, é selecionado ou realçado.

-   [Introdução](#introduction)
-   [Implementando guias contextuais](#implementing-contextual-tabs)
    -   [Marcação](#markup)
    -   [Código](#code)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Em contraste com as guias principais, que contêm vários comandos comuns que são relevantes independentemente do contexto do espaço de trabalho, as guias contextuais normalmente contêm um ou mais comandos que se aplicam apenas a um objeto selecionado ou realçado.

Quando um objeto é selecionado ou realçado no espaço de trabalho do aplicativo, o tipo e o contexto do objeto podem exigir comandos diferentes que não fazem sentido organizacional ou funcional em uma guia contextual. Nesses casos, várias guias contextuais, que estão contidas em um [grupo de guias](windowsribbon-controls-tabgroup.md), podem ser necessárias. Por exemplo, selecionar uma imagem contida em uma célula de tabela pode exigir duas guias contextuais que expõem a funcionalidade de tabela e imagem.

> [!Note]  
> Além de várias guias contextuais, a estrutura da faixa de faixas também dá suporte a vários controles de [grupo de guias](windowsribbon-controls-tabgroup.md) em uma faixa de faixas.

 

Ao exibir guias contextuais, a estrutura da faixa de faixas impõe um conjunto básico de comportamentos que incluem:

-   As guias contextuais são posicionadas na ordem em que são declaradas e à direita das guias de núcleo na linha da guia da faixa de lista.
-   Quando a faixa de faixas é redimensionada, as guias são dimensionadas e os rótulos da guia são truncados conforme o espaço é necessário. No entanto, as guias contextuais visíveis recebem uma prioridade de exibição mais alta na qual elas são dimensionadas e truncadas por último.
-   O rótulo de um [grupo de guias](windowsribbon-controls-tabgroup.md) é exibido na barra de título do aplicativo e abrange todas as guias contextuais associadas.
-   Quando vários controles de [grupo de guias](windowsribbon-controls-tabgroup.md) são exibidos ao mesmo tempo, uma das cinco cores exclusivas é atribuída ao plano de fundo de cada grupo de guias na barra de título do aplicativo. Essa cor também é usada como uma cor de realce para as guias contextuais no grupo de guias.
-   A atribuição de cor do [grupo de guias](windowsribbon-controls-tabgroup.md) baseia-se na ordem em que os elementos do grupo de guias são declarados na marcação. As cores são definidas pela estrutura e não podem ser especificadas pelo aplicativo.
-   As cores do [grupo de guias](windowsribbon-controls-tabgroup.md) definidas pela estrutura podem ser modificadas indiretamente por meio das chaves de propriedade de [Propriedades da estrutura](windowsribbon-reference-properties-framework.md) . Para obter mais informações, consulte [Personalizando as cores da faixa](ribbon-color.md)de forma.
-   Quando mais de cinco controles de [grupo de guias](windowsribbon-controls-tabgroup.md) são exibidos a qualquer momento, a estrutura circula as cores associadas.
-   O número máximo de controles de [guia](windowsribbon-controls-tab.md) em uma faixa de faixas é limitado a 100. Isso inclui guias contextuais, visíveis ou não.

A captura de tela a seguir mostra uma guia contextual do Paint do Windows 7.

![captura de tela que mostra um controle de guia contextual.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a>Implementando guias contextuais

Esta seção aborda os detalhes de implementação das guias contextuais da faixa de medida e explica como incorporá-las em um aplicativo da faixa de faixas.

### <a name="markup"></a>Marcação

Os exemplos a seguir demonstram a marcação básica para um elemento [**TabGroup**](windowsribbon-element-tabgroup.md) que contém duas guias contextuais.

Esta seção de código mostra as declarações de comando [**TabGroup**](windowsribbon-element-tabgroup.md) e [Tab](windowsribbon-controls-tab.md) .


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



Esta seção de código mostra as declarações de controle necessárias para exibir duas guias contextuais em um [**TabGroup**](windowsribbon-element-tabgroup.md).


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a>Código

[Interface do usuário \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) é a única chave de propriedade definida pela estrutura para especificar a visibilidade e o estado de guias contextuais. Quando um objeto é selecionado no espaço de trabalho do aplicativo, essa propriedade pode ser atribuída a um dos três valores da enumeração [**\_ CONTEXTAVAILABILITY da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) que definem se uma guia contextual existe e, se for, se ela é mostrada como a guia ativa.

Um aplicativo solicita uma atualização de [grupo de guias](windowsribbon-controls-tabgroup.md) invalidando e atualizando a propriedade [ \_ PKEY \_ ContextAvailable da interface do usuário](windowsribbon-reference-properties-uipkey-contextavailable.md) quando o contexto do espaço de trabalho é alterado.

As seções a seguir do código demonstram como exibir uma guia contextual quando uma imagem é selecionada em um espaço de trabalho do aplicativo.


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes de experiência do usuário da faixa de das](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de das](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 