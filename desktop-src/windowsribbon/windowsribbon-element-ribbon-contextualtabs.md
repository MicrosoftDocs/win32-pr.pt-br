---
title: Propriedade Ribbon. ContextualTabs
description: Representa um contêiner para guias contextuais.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Faixa de ContextualTabs da propriedade Windows da faixa de propriedades
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644408"
---
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="8a712-104">Propriedade Ribbon. ContextualTabs</span><span class="sxs-lookup"><span data-stu-id="8a712-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="8a712-105">Representa um contêiner para guias contextuais.</span><span class="sxs-lookup"><span data-stu-id="8a712-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="8a712-106">Uso</span><span class="sxs-lookup"><span data-stu-id="8a712-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="8a712-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="8a712-107">Attributes</span></span>

<span data-ttu-id="8a712-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="8a712-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8a712-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8a712-109">Child elements</span></span>



| <span data-ttu-id="8a712-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a712-110">Element</span></span>                                                       | <span data-ttu-id="8a712-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a712-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="8a712-112">**TabGroup**</span><span class="sxs-lookup"><span data-stu-id="8a712-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="8a712-113">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="8a712-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="8a712-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="8a712-114">Parent elements</span></span>



| <span data-ttu-id="8a712-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="8a712-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="8a712-116">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="8a712-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="8a712-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a712-117">Remarks</span></span>

<span data-ttu-id="8a712-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8a712-118">Optional.</span></span>

<span data-ttu-id="8a712-119">Pode ocorrer no máximo uma vez para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="8a712-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="8a712-120">As guias contextuais são úteis para exibir a funcionalidade que é relevante apenas para um contexto de aplicativo específico, como uma guia de formatação de imagem em um editor de texto que é exibido somente quando uma imagem é realçada.</span><span class="sxs-lookup"><span data-stu-id="8a712-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="8a712-121">Normalmente, as guias contextuais não são visíveis até que um contexto de aplicativo específico ocorra e o aplicativo notifique a estrutura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="8a712-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="8a712-122">Quando exibidas, as guias contextuais são codificadas por cores para diferenciá-las das guias regulares.</span><span class="sxs-lookup"><span data-stu-id="8a712-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="8a712-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a712-123">Examples</span></span>

<span data-ttu-id="8a712-124">O exemplo a seguir demonstra a marcação básica para o elemento **Ribbon. ContextualTabs** .</span><span class="sxs-lookup"><span data-stu-id="8a712-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="8a712-125">Esta seção de código mostra uma declaração de comando [**TabGroup**](windowsribbon-element-tabgroup.md) e duas declarações de comando de [**guia**](windowsribbon-element-tab.md) contextual.</span><span class="sxs-lookup"><span data-stu-id="8a712-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="8a712-126">Esta seção de código mostra a declaração de controle **Ribbon. ContextualTabs** com um [**TabGroup**](windowsribbon-element-tabgroup.md) e dois controles de [**guia**](windowsribbon-element-tab.md) contextuais.</span><span class="sxs-lookup"><span data-stu-id="8a712-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8a712-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a712-127">Requirements</span></span>



| <span data-ttu-id="8a712-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a712-128">Requirement</span></span> | <span data-ttu-id="8a712-129">Valor</span><span class="sxs-lookup"><span data-stu-id="8a712-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="8a712-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a712-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8a712-131">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8a712-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="8a712-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a712-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8a712-133">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8a712-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a712-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8a712-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a712-135">**Faixa de guia. guias**</span><span class="sxs-lookup"><span data-stu-id="8a712-135">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





