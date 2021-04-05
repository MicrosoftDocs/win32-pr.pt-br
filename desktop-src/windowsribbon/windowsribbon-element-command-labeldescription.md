---
title: Propriedade Command. LabelDescription
description: Representa uma descrição do rótulo.
ms.assetid: 6c683e9e-0742-466e-9fdd-3d29f8ccb9ff
keywords:
- Faixa de das propriedades do Windows de Propriedade Command. LabelDescription
topic_type:
- apiref
api_name:
- Command.LabelDescription
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f748425b4c8363feee737d18c750b3a1d91121b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918998"
---
# <a name="commandlabeldescription-property"></a><span data-ttu-id="ba8aa-104">Propriedade Command. LabelDescription</span><span class="sxs-lookup"><span data-stu-id="ba8aa-104">Command.LabelDescription property</span></span>

<span data-ttu-id="ba8aa-105">Representa uma descrição do rótulo.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-105">Represents a label description.</span></span>

## <a name="usage"></a><span data-ttu-id="ba8aa-106">Uso</span><span class="sxs-lookup"><span data-stu-id="ba8aa-106">Usage</span></span>

``` syntax
<Command.LabelDescription>
  child elements
</Command.LabelDescription>
```

## <a name="attributes"></a><span data-ttu-id="ba8aa-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="ba8aa-107">Attributes</span></span>

<span data-ttu-id="ba8aa-108">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ba8aa-109">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ba8aa-109">Child elements</span></span>



| <span data-ttu-id="ba8aa-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba8aa-110">Element</span></span>                                                   | <span data-ttu-id="ba8aa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba8aa-111">Description</span></span>                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="ba8aa-112">**Strings**</span><span class="sxs-lookup"><span data-stu-id="ba8aa-112">**String**</span></span>](windowsribbon-element-string.md)<br/> | <span data-ttu-id="ba8aa-113">Pode ocorrer no máximo uma vez</span><span class="sxs-lookup"><span data-stu-id="ba8aa-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ba8aa-114">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="ba8aa-114">Parent elements</span></span>



| <span data-ttu-id="ba8aa-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="ba8aa-115">Element</span></span>                                                     |
|-------------------------------------------------------------|
| [<span data-ttu-id="ba8aa-116">**Comando**</span><span class="sxs-lookup"><span data-stu-id="ba8aa-116">**Command**</span></span>](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ba8aa-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba8aa-117">Remarks</span></span>

<span data-ttu-id="ba8aa-118">Opcional.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-118">Optional.</span></span>

<span data-ttu-id="ba8aa-119">Pode ocorrer no máximo uma vez para cada [**comando**](windowsribbon-element-command.md).</span><span class="sxs-lookup"><span data-stu-id="ba8aa-119">May occur at most once for each [**Command**](windowsribbon-element-command.md).</span></span>

<span data-ttu-id="ba8aa-120">**Command. LabelDescription** pode conter um valor do *tipo xs: String* restrito a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-120">**Command.LabelDescription** can contain a value of *type xs:string* constrained to any sequence of characters, including white space and line-break characters.</span></span>

> [!Note]  
> <span data-ttu-id="ba8aa-121">Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-121">Use the Universal Character Set (UCS) XML character reference `&#xA;` to specify a line break.</span></span>

 

<span data-ttu-id="ba8aa-122">O comprimento máximo é não associado.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-122">The maximum length is unbounded.</span></span>

<span data-ttu-id="ba8aa-123">Se nenhum valor for fornecido para **Command. LabelDescription**, o elemento filho da [**cadeia de caracteres**](windowsribbon-element-string.md) será necessário.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-123">If no value is supplied for **Command.LabelDescription**, the [**String**](windowsribbon-element-string.md) child element is required.</span></span>

> [!Note]  
> <span data-ttu-id="ba8aa-124">Se **Command. LabelDescription** contiver um valor e um elemento filho de [**cadeia**](windowsribbon-element-string.md) de caracteres, a **cadeia de caracteres** terá precedência.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-124">If **Command.LabelDescription** contains both a value and a [**String**](windowsribbon-element-string.md) child element, **String** takes precedence.</span></span>

 

<span data-ttu-id="ba8aa-125">O **comando. LabelDescription** só dá suporte ao alinhamento à esquerda.</span><span class="sxs-lookup"><span data-stu-id="ba8aa-125">**Command.LabelDescription** only supports left alignment.</span></span>

## <a name="examples"></a><span data-ttu-id="ba8aa-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba8aa-126">Examples</span></span>

<span data-ttu-id="ba8aa-127">O exemplo a seguir mostra um manifesto dos comandos da área de transferência com várias declarações **Command. LabelDescription** .</span><span class="sxs-lookup"><span data-stu-id="ba8aa-127">The following example shows a manifest of clipboard Commands with various **Command.LabelDescription** declarations.</span></span>


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



## <a name="requirements"></a><span data-ttu-id="ba8aa-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8aa-128">Requirements</span></span>



| <span data-ttu-id="ba8aa-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba8aa-129">Requirement</span></span> | <span data-ttu-id="ba8aa-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ba8aa-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ba8aa-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba8aa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8aa-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ba8aa-132">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ba8aa-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba8aa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8aa-134">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="ba8aa-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba8aa-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba8aa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba8aa-136">\_LabelDescription PKEY \_ UI</span><span class="sxs-lookup"><span data-stu-id="ba8aa-136">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
</dt> </dl>

 

 





