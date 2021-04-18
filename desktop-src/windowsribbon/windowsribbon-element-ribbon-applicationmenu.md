---
title: Propriedade Ribbon. ApplicationMenu
description: Representa o menu do aplicativo. | Propriedade Ribbon. ApplicationMenu
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Faixa de ApplicationMenu da propriedade Windows da faixa de propriedades
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105780384"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="ea4ce-105">Propriedade Ribbon. ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="ea4ce-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="ea4ce-106">Representa o menu do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea4ce-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="ea4ce-107">Uso</span><span class="sxs-lookup"><span data-stu-id="ea4ce-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="ea4ce-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ea4ce-108">Attributes</span></span>

<span data-ttu-id="ea4ce-109">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ea4ce-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ea4ce-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ea4ce-110">Child elements</span></span>



| <span data-ttu-id="ea4ce-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea4ce-111">Element</span></span>                                                                     | <span data-ttu-id="ea4ce-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ea4ce-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ea4ce-113">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="ea4ce-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="ea4ce-114">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="ea4ce-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ea4ce-115">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ea4ce-115">Parent elements</span></span>



| <span data-ttu-id="ea4ce-116">Elemento</span><span class="sxs-lookup"><span data-stu-id="ea4ce-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="ea4ce-117">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="ea4ce-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ea4ce-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea4ce-118">Remarks</span></span>

<span data-ttu-id="ea4ce-119">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="ea4ce-119">Required.</span></span>

<span data-ttu-id="ea4ce-120">Pode ocorrer no máximo uma vez para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="ea4ce-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ea4ce-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ea4ce-121">Examples</span></span>

<span data-ttu-id="ea4ce-122">O exemplo a seguir demonstra a marcação básica para o elemento **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="ea4ce-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="ea4ce-123">Esta seção de código mostra a declaração de controle **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="ea4ce-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="ea4ce-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea4ce-124">Requirements</span></span>



| <span data-ttu-id="ea4ce-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea4ce-125">Requirement</span></span> | <span data-ttu-id="ea4ce-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ea4ce-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ea4ce-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea4ce-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ea4ce-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ea4ce-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ea4ce-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea4ce-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ea4ce-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ea4ce-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





