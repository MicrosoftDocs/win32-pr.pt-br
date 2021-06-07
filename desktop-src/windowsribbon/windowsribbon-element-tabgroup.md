---
title: Elemento TabGroup
description: Representa um conjunto contextual de controles Tab.
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- Faixa de Opções do Windows do elemento TabGroup
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4c18db72d6b0161842bfde9d5a836d14189c6a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444057"
---
# <a name="tabgroup-element"></a><span data-ttu-id="4555b-104">Elemento TabGroup</span><span class="sxs-lookup"><span data-stu-id="4555b-104">TabGroup element</span></span>

<span data-ttu-id="4555b-105">Representa um conjunto contextual de [controles Tab.](windowsribbon-controls-tabgroup.md)</span><span class="sxs-lookup"><span data-stu-id="4555b-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="4555b-106">Uso</span><span class="sxs-lookup"><span data-stu-id="4555b-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="4555b-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="4555b-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4555b-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="4555b-108">Attribute</span></span></th>
<th><span data-ttu-id="4555b-109">Type</span><span class="sxs-lookup"><span data-stu-id="4555b-109">Type</span></span></th>
<th><span data-ttu-id="4555b-110">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4555b-110">Required</span></span></th>
<th><span data-ttu-id="4555b-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4555b-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4555b-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="4555b-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="4555b-113">xs:positiveInteger ou xs:string</span><span class="sxs-lookup"><span data-stu-id="4555b-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="4555b-114">Não</span><span class="sxs-lookup"><span data-stu-id="4555b-114">No</span></span><br/></td>
<td><span data-ttu-id="4555b-115">Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4555b-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="4555b-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)</span><span class="sxs-lookup"><span data-stu-id="4555b-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="4555b-117">Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive.</span><span class="sxs-lookup"><span data-stu-id="4555b-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="4555b-118">O valor deve ser exclusivo dentro do documento XML da Faixa de Opções.</span><span class="sxs-lookup"><span data-stu-id="4555b-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="4555b-119">Comprimento máximo: 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4555b-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="4555b-120">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4555b-120">Child elements</span></span>



| <span data-ttu-id="4555b-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="4555b-121">Element</span></span>                                             | <span data-ttu-id="4555b-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="4555b-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="4555b-123">**Guia**</span><span class="sxs-lookup"><span data-stu-id="4555b-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="4555b-124">Deve ocorrer pelo menos uma vez</span><span class="sxs-lookup"><span data-stu-id="4555b-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="4555b-125">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="4555b-125">Parent elements</span></span>



| <span data-ttu-id="4555b-126">Elemento</span><span class="sxs-lookup"><span data-stu-id="4555b-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="4555b-127">**Ribbon.ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="4555b-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="4555b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4555b-128">Remarks</span></span>

<span data-ttu-id="4555b-129">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="4555b-129">Required.</span></span>

<span data-ttu-id="4555b-130">Deve ocorrer pelo menos uma vez para cada [**elemento Ribbon.ContextualTabs.**](windowsribbon-element-ribbon-contextualtabs.md)</span><span class="sxs-lookup"><span data-stu-id="4555b-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="4555b-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4555b-131">Examples</span></span>

<span data-ttu-id="4555b-132">O exemplo a seguir demonstra a marcação básica para o **elemento TabGroup.**</span><span class="sxs-lookup"><span data-stu-id="4555b-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="4555b-133">Esta seção de código mostra uma declaração **comando TabGroup** com duas guias contextuais.</span><span class="sxs-lookup"><span data-stu-id="4555b-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


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



<span data-ttu-id="4555b-134">Esta seção de código mostra as declarações **de controle TabGroup** correspondentes.</span><span class="sxs-lookup"><span data-stu-id="4555b-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="4555b-135">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="4555b-135">Element information</span></span>

- <span data-ttu-id="4555b-136">**Sistema mínimo com suporte:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="4555b-136">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="4555b-137">**Pode estar vazio:** Não</span><span class="sxs-lookup"><span data-stu-id="4555b-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="4555b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="4555b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4555b-139">Controle De grupo de guias</span><span class="sxs-lookup"><span data-stu-id="4555b-139">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="4555b-140">Controle guia</span><span class="sxs-lookup"><span data-stu-id="4555b-140">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





