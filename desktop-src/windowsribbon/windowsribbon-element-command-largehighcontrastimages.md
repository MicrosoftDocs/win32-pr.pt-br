---
title: Propriedade Command. LargeHighContrastImages
description: Representa um contêiner de imagens; Nesse caso, imagens grandes para uso com configurações do sistema de alto contraste.
ms.assetid: e25f207f-ac3f-4a5f-8104-c928b38a52a8
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. LargeHighContrastImages
topic_type:
- apiref
api_name:
- Command.LargeHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e94fc31e2113990a1862fab7288ffeefef787cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009663"
---
# <a name="commandlargehighcontrastimages-property"></a><span data-ttu-id="6814c-104">Propriedade Command. LargeHighContrastImages</span><span class="sxs-lookup"><span data-stu-id="6814c-104">Command.LargeHighContrastImages property</span></span>

<span data-ttu-id="6814c-105">Representa um contêiner de imagens; Nesse caso, imagens grandes para uso com configurações do sistema de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="6814c-105">Represents a container of images; in this case, large images for use with high-contrast system settings.</span></span>

## <a name="usage"></a><span data-ttu-id="6814c-106">Uso</span><span class="sxs-lookup"><span data-stu-id="6814c-106">Usage</span></span>

``` syntax
<Command.LargeHighContrastImages>
  child elements
</Command.LargeHighContrastImages>
```

## <a name="attributes"></a><span data-ttu-id="6814c-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="6814c-107">Attributes</span></span>

<span data-ttu-id="6814c-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="6814c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6814c-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6814c-109">Child elements</span></span>



| <span data-ttu-id="6814c-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="6814c-110">Element</span></span>                                                 | <span data-ttu-id="6814c-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6814c-111">Description</span></span>                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="6814c-112">**Imagem**</span><span class="sxs-lookup"><span data-stu-id="6814c-112">**Image**</span></span>](windowsribbon-element-image.md)<br/> | <span data-ttu-id="6814c-113">Pode ocorrer uma ou mais vezes</span><span class="sxs-lookup"><span data-stu-id="6814c-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6814c-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6814c-114">Parent elements</span></span>



| <span data-ttu-id="6814c-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="6814c-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="6814c-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="6814c-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6814c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6814c-117">Remarks</span></span>

<span data-ttu-id="6814c-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6814c-118">Optional.</span></span>

<span data-ttu-id="6814c-119">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="6814c-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="6814c-120">Os recursos de imagem devem estar em conformidade com o formato gráfico BMP (bitmap padrão) usado no Windows.</span><span class="sxs-lookup"><span data-stu-id="6814c-120">Image resources must conform to the standard bitmap (BMP) graphics format used in Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="6814c-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6814c-121">Examples</span></span>

<span data-ttu-id="6814c-122">O exemplo a seguir demonstra a marcação básica para o [**SplitButton**](windowsribbon-element-splitbutton.md) com um elemento de [**menu**](windowsribbon-element-menugroup.md) .</span><span class="sxs-lookup"><span data-stu-id="6814c-122">The following example demonstrates the basic markup for the [**SplitButton**](windowsribbon-element-splitbutton.md) with a [**MenuGroup**](windowsribbon-element-menugroup.md) element.</span></span>

<span data-ttu-id="6814c-123">Esta seção de código mostra as declarações de comando [**SplitButton**](windowsribbon-element-splitbutton.md) e de [**menu de menus**](windowsribbon-element-menugroup.md) com recursos de imagem de alto contraste grandes e pequenos.</span><span class="sxs-lookup"><span data-stu-id="6814c-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and [**MenuGroup**](windowsribbon-element-menugroup.md) Command declarations with large and small high contrast image resources.</span></span> <span data-ttu-id="6814c-124">Um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai do elemento **SplitButton** também é declarado.</span><span class="sxs-lookup"><span data-stu-id="6814c-124">An associated [**Group**](windowsribbon-element-group.md) that acts as the parent container for the **SplitButton** element is also declared.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6814c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6814c-125">Requirements</span></span>



| <span data-ttu-id="6814c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6814c-126">Requirement</span></span> | <span data-ttu-id="6814c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="6814c-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6814c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6814c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6814c-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6814c-129">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6814c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6814c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6814c-131">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="6814c-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6814c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6814c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6814c-133">Especificando recursos de imagem da faixa de uma</span><span class="sxs-lookup"><span data-stu-id="6814c-133">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> <dt>

[<span data-ttu-id="6814c-134">\_LargeHighContrastImage PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="6814c-134">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 





