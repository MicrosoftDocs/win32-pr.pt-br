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
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="65a92-106">Exibindo guias contextuais</span><span class="sxs-lookup"><span data-stu-id="65a92-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="65a92-107">Em um aplicativo do Windows Ribbon Framework, uma guia contextual é um controle de [guia](windowsribbon-controls-tab.md) oculto que é exibido na linha da guia quando um objeto no espaço de trabalho do aplicativo, como uma imagem, é selecionado ou realçado.</span><span class="sxs-lookup"><span data-stu-id="65a92-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="65a92-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="65a92-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="65a92-109">Implementando guias contextuais</span><span class="sxs-lookup"><span data-stu-id="65a92-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="65a92-110">Marcação</span><span class="sxs-lookup"><span data-stu-id="65a92-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="65a92-111">Código</span><span class="sxs-lookup"><span data-stu-id="65a92-111">Code</span></span>](#code)
-   [<span data-ttu-id="65a92-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65a92-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="65a92-113">Introdução</span><span class="sxs-lookup"><span data-stu-id="65a92-113">Introduction</span></span>

<span data-ttu-id="65a92-114">Em contraste com as guias principais, que contêm vários comandos comuns que são relevantes independentemente do contexto do espaço de trabalho, as guias contextuais normalmente contêm um ou mais comandos que se aplicam apenas a um objeto selecionado ou realçado.</span><span class="sxs-lookup"><span data-stu-id="65a92-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="65a92-115">Quando um objeto é selecionado ou realçado no espaço de trabalho do aplicativo, o tipo e o contexto do objeto podem exigir comandos diferentes que não fazem sentido organizacional ou funcional em uma guia contextual. Nesses casos, várias guias contextuais, que estão contidas em um [grupo de guias](windowsribbon-controls-tabgroup.md), podem ser necessárias.</span><span class="sxs-lookup"><span data-stu-id="65a92-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="65a92-116">Por exemplo, selecionar uma imagem contida em uma célula de tabela pode exigir duas guias contextuais que expõem a funcionalidade de tabela e imagem.</span><span class="sxs-lookup"><span data-stu-id="65a92-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="65a92-117">Além de várias guias contextuais, a estrutura da faixa de faixas também dá suporte a vários controles de [grupo de guias](windowsribbon-controls-tabgroup.md) em uma faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="65a92-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="65a92-118">Ao exibir guias contextuais, a estrutura da faixa de faixas impõe um conjunto básico de comportamentos que incluem:</span><span class="sxs-lookup"><span data-stu-id="65a92-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="65a92-119">As guias contextuais são posicionadas na ordem em que são declaradas e à direita das guias de núcleo na linha da guia da faixa de lista.</span><span class="sxs-lookup"><span data-stu-id="65a92-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="65a92-120">Quando a faixa de faixas é redimensionada, as guias são dimensionadas e os rótulos da guia são truncados conforme o espaço é necessário.</span><span class="sxs-lookup"><span data-stu-id="65a92-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="65a92-121">No entanto, as guias contextuais visíveis recebem uma prioridade de exibição mais alta na qual elas são dimensionadas e truncadas por último.</span><span class="sxs-lookup"><span data-stu-id="65a92-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="65a92-122">O rótulo de um [grupo de guias](windowsribbon-controls-tabgroup.md) é exibido na barra de título do aplicativo e abrange todas as guias contextuais associadas.</span><span class="sxs-lookup"><span data-stu-id="65a92-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="65a92-123">Quando vários controles de [grupo de guias](windowsribbon-controls-tabgroup.md) são exibidos ao mesmo tempo, uma das cinco cores exclusivas é atribuída ao plano de fundo de cada grupo de guias na barra de título do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65a92-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="65a92-124">Essa cor também é usada como uma cor de realce para as guias contextuais no grupo de guias.</span><span class="sxs-lookup"><span data-stu-id="65a92-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="65a92-125">A atribuição de cor do [grupo de guias](windowsribbon-controls-tabgroup.md) baseia-se na ordem em que os elementos do grupo de guias são declarados na marcação.</span><span class="sxs-lookup"><span data-stu-id="65a92-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="65a92-126">As cores são definidas pela estrutura e não podem ser especificadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65a92-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="65a92-127">As cores do [grupo de guias](windowsribbon-controls-tabgroup.md) definidas pela estrutura podem ser modificadas indiretamente por meio das chaves de propriedade de [Propriedades da estrutura](windowsribbon-reference-properties-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="65a92-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="65a92-128">Para obter mais informações, consulte [Personalizando as cores da faixa](ribbon-color.md)de forma.</span><span class="sxs-lookup"><span data-stu-id="65a92-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="65a92-129">Quando mais de cinco controles de [grupo de guias](windowsribbon-controls-tabgroup.md) são exibidos a qualquer momento, a estrutura circula as cores associadas.</span><span class="sxs-lookup"><span data-stu-id="65a92-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="65a92-130">O número máximo de controles de [guia](windowsribbon-controls-tab.md) em uma faixa de faixas é limitado a 100.</span><span class="sxs-lookup"><span data-stu-id="65a92-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="65a92-131">Isso inclui guias contextuais, visíveis ou não.</span><span class="sxs-lookup"><span data-stu-id="65a92-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="65a92-132">A captura de tela a seguir mostra uma guia contextual do Paint do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65a92-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![captura de tela que mostra um controle de guia contextual.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="65a92-134">Implementando guias contextuais</span><span class="sxs-lookup"><span data-stu-id="65a92-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="65a92-135">Esta seção aborda os detalhes de implementação das guias contextuais da faixa de medida e explica como incorporá-las em um aplicativo da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="65a92-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="65a92-136">Marcação</span><span class="sxs-lookup"><span data-stu-id="65a92-136">Markup</span></span>

<span data-ttu-id="65a92-137">Os exemplos a seguir demonstram a marcação básica para um elemento [**TabGroup**](windowsribbon-element-tabgroup.md) que contém duas guias contextuais.</span><span class="sxs-lookup"><span data-stu-id="65a92-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="65a92-138">Esta seção de código mostra as declarações de comando [**TabGroup**](windowsribbon-element-tabgroup.md) e [Tab](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="65a92-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="65a92-139">Esta seção de código mostra as declarações de controle necessárias para exibir duas guias contextuais em um [**TabGroup**](windowsribbon-element-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="65a92-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


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



### <a name="code"></a><span data-ttu-id="65a92-140">Código</span><span class="sxs-lookup"><span data-stu-id="65a92-140">Code</span></span>

<span data-ttu-id="65a92-141">[Interface do usuário \_ PKEY \_ ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) é a única chave de propriedade definida pela estrutura para especificar a visibilidade e o estado de guias contextuais.</span><span class="sxs-lookup"><span data-stu-id="65a92-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="65a92-142">Quando um objeto é selecionado no espaço de trabalho do aplicativo, essa propriedade pode ser atribuída a um dos três valores da enumeração [**\_ CONTEXTAVAILABILITY da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) que definem se uma guia contextual existe e, se for, se ela é mostrada como a guia ativa.</span><span class="sxs-lookup"><span data-stu-id="65a92-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="65a92-143">Um aplicativo solicita uma atualização de [grupo de guias](windowsribbon-controls-tabgroup.md) invalidando e atualizando a propriedade [ \_ PKEY \_ ContextAvailable da interface do usuário](windowsribbon-reference-properties-uipkey-contextavailable.md) quando o contexto do espaço de trabalho é alterado.</span><span class="sxs-lookup"><span data-stu-id="65a92-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="65a92-144">As seções a seguir do código demonstram como exibir uma guia contextual quando uma imagem é selecionada em um espaço de trabalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="65a92-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="65a92-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65a92-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65a92-146">Diretrizes de experiência do usuário da faixa de das</span><span class="sxs-lookup"><span data-stu-id="65a92-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="65a92-147">Processo de design da faixa de das</span><span class="sxs-lookup"><span data-stu-id="65a92-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 