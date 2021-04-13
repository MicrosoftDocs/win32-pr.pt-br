---
title: Propriedade Ribbon. QuickAccessToolbar
description: Representa um contêiner para a barra de ferramentas de acesso rápido (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Faixa de QuickAccessToolbar da propriedade Windows da faixa de propriedades
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369256"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="36061-104">Propriedade Ribbon. QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="36061-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="36061-105">Representa um contêiner para a barra de ferramentas de acesso rápido (QAT).</span><span class="sxs-lookup"><span data-stu-id="36061-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="36061-106">Uso</span><span class="sxs-lookup"><span data-stu-id="36061-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="36061-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="36061-107">Attributes</span></span>

<span data-ttu-id="36061-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="36061-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="36061-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="36061-109">Child elements</span></span>



| <span data-ttu-id="36061-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="36061-110">Element</span></span>                                                                           | <span data-ttu-id="36061-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="36061-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="36061-112">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="36061-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="36061-113">Deve ocorrer exatamente uma vez</span><span class="sxs-lookup"><span data-stu-id="36061-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="36061-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="36061-114">Parent elements</span></span>



| <span data-ttu-id="36061-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="36061-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="36061-116">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="36061-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="36061-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="36061-117">Remarks</span></span>

<span data-ttu-id="36061-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="36061-118">Required.</span></span>

<span data-ttu-id="36061-119">Pode ocorrer uma ou mais vezes para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="36061-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="36061-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36061-120">Examples</span></span>

<span data-ttu-id="36061-121">O exemplo a seguir demonstra a marcação básica para o elemento **Ribbon. QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="36061-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="36061-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36061-122">Requirements</span></span>



| <span data-ttu-id="36061-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="36061-123">Requirement</span></span> | <span data-ttu-id="36061-124">Valor</span><span class="sxs-lookup"><span data-stu-id="36061-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="36061-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36061-125">Minimum supported client</span></span><br/> | <span data-ttu-id="36061-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="36061-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="36061-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36061-127">Minimum supported server</span></span><br/> | <span data-ttu-id="36061-128">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="36061-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





