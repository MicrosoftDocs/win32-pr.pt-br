---
title: Propriedade Ribbon. HelpButton
description: Representa um contêiner para o botão de ajuda.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Faixa de HelpButton da propriedade Windows da faixa de propriedades
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644848"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="ebdb4-104">Propriedade Ribbon. HelpButton</span><span class="sxs-lookup"><span data-stu-id="ebdb4-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="ebdb4-105">Representa um contêiner para o [botão de ajuda](windowsribbon-controls-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="ebdb4-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="ebdb4-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ebdb4-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="ebdb4-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ebdb4-107">Attributes</span></span>

<span data-ttu-id="ebdb4-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ebdb4-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ebdb4-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ebdb4-109">Child elements</span></span>



| <span data-ttu-id="ebdb4-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebdb4-110">Element</span></span>                                                           | <span data-ttu-id="ebdb4-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ebdb4-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ebdb4-112">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="ebdb4-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="ebdb4-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="ebdb4-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ebdb4-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ebdb4-114">Parent elements</span></span>



| <span data-ttu-id="ebdb4-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ebdb4-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="ebdb4-116">**Faixa de opções**</span><span class="sxs-lookup"><span data-stu-id="ebdb4-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ebdb4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ebdb4-117">Remarks</span></span>

<span data-ttu-id="ebdb4-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ebdb4-118">Optional.</span></span>

<span data-ttu-id="ebdb4-119">Pode ocorrer no máximo uma vez para cada [**faixa de faixas**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="ebdb4-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ebdb4-120">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ebdb4-120">Examples</span></span>

<span data-ttu-id="ebdb4-121">O exemplo a seguir demonstra a marcação básica necessária para implementar um botão de ajuda da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="ebdb4-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="ebdb4-122">Esta seção de código mostra a declaração de comando **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="ebdb4-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="ebdb4-123">Esta seção de código mostra a declaração de controle **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="ebdb4-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="ebdb4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebdb4-124">Requirements</span></span>



| <span data-ttu-id="ebdb4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebdb4-125">Requirement</span></span> | <span data-ttu-id="ebdb4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ebdb4-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ebdb4-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebdb4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ebdb4-128">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ebdb4-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ebdb4-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ebdb4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ebdb4-130">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ebdb4-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





