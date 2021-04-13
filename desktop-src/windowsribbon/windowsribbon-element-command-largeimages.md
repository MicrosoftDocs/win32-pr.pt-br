---
title: Propriedade Command. LargeImages
description: Representa um contêiner de imagens; Nesse caso, imagens grandes.
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. LargeImages
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf71557506d4b9cced21069473d1a6db9b208b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455784"
---
# <a name="commandlargeimages-property"></a><span data-ttu-id="bc724-104">Propriedade Command. LargeImages</span><span class="sxs-lookup"><span data-stu-id="bc724-104">Command.LargeImages property</span></span>

<span data-ttu-id="bc724-105">Representa um contêiner de imagens; Nesse caso, imagens grandes.</span><span class="sxs-lookup"><span data-stu-id="bc724-105">Represents a container of images; in this case, large images.</span></span>

## <a name="usage"></a><span data-ttu-id="bc724-106">Uso</span><span class="sxs-lookup"><span data-stu-id="bc724-106">Usage</span></span>

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a><span data-ttu-id="bc724-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="bc724-107">Attributes</span></span>

<span data-ttu-id="bc724-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="bc724-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bc724-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="bc724-109">Child elements</span></span>



| <span data-ttu-id="bc724-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc724-110">Element</span></span>                                                 | <span data-ttu-id="bc724-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="bc724-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="bc724-112">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="bc724-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="bc724-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="bc724-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bc724-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="bc724-114">Parent elements</span></span>



| <span data-ttu-id="bc724-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="bc724-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="bc724-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="bc724-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bc724-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc724-117">Remarks</span></span>

<span data-ttu-id="bc724-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc724-118">Optional.</span></span>

<span data-ttu-id="bc724-119">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="bc724-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="bc724-120">Os recursos de imagem devem estar em conformidade com o formato gráfico BMP (bitmap padrão) usado no Windows.</span><span class="sxs-lookup"><span data-stu-id="bc724-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="bc724-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bc724-121">Examples</span></span>

<span data-ttu-id="bc724-122">O exemplo a seguir demonstra a marcação básica para o [**SplitButton**](windowsribbon-element-splitbutton.md) com um elemento de [**menu**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="bc724-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="bc724-123">Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e de [**menu de menus**](windowsribbon-element-menugroup.md) com um recurso de imagem grande e um pequeno.</span><span class="sxs-lookup"><span data-stu-id="bc724-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with a large and a small image resource.</span></span> <span data-ttu-id="bc724-124">Um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai do elemento **SplitButton** também é declarado.</span><span class="sxs-lookup"><span data-stu-id="bc724-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a><span data-ttu-id="bc724-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc724-125">Requirements</span></span>



| <span data-ttu-id="bc724-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc724-126">Requirement</span></span> | <span data-ttu-id="bc724-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bc724-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bc724-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc724-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc724-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bc724-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bc724-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bc724-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc724-131">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bc724-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc724-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc724-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc724-133">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="bc724-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="bc724-134">\_LargeImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="bc724-134">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 





