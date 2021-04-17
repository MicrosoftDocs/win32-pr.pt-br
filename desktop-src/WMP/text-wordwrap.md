---
title: TEXT. wordWrap
description: O atributo wordWrap especifica ou recupera um valor que indica se a quebra automática de texto está habilitada ou desabilitada.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- Windows Media Player de TEXT. wordWrap
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751573"
---
# <a name="textwordwrap"></a><span data-ttu-id="fbee4-104">TEXT. wordWrap</span><span class="sxs-lookup"><span data-stu-id="fbee4-104">TEXT.wordWrap</span></span>

<span data-ttu-id="fbee4-105">O atributo **WordWrap** especifica ou recupera um valor que indica se a quebra automática de texto está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="fbee4-105">The **wordWrap** attribute specifies or retrieves a value indicating whether word wrap is enabled or disabled.</span></span>

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a><span data-ttu-id="fbee4-106">Valores possíveis</span><span class="sxs-lookup"><span data-stu-id="fbee4-106">Possible Values</span></span>

<span data-ttu-id="fbee4-107">Esse atributo é um **booliano** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fbee4-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="fbee4-108">Valor</span><span class="sxs-lookup"><span data-stu-id="fbee4-108">Value</span></span> | <span data-ttu-id="fbee4-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fbee4-109">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbee4-110">true</span><span class="sxs-lookup"><span data-stu-id="fbee4-110">true</span></span>  | <span data-ttu-id="fbee4-111">A quebra automática de texto está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fbee4-111">Word wrap is enabled.</span></span>                                                                             |
| <span data-ttu-id="fbee4-112">false</span><span class="sxs-lookup"><span data-stu-id="fbee4-112">false</span></span> | <span data-ttu-id="fbee4-113">Padrão.</span><span class="sxs-lookup"><span data-stu-id="fbee4-113">Default.</span></span> <span data-ttu-id="fbee4-114">A quebra automática de texto está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="fbee4-114">Word wrap is disabled.</span></span> <span data-ttu-id="fbee4-115">Se o texto não couber no controle, o texto será cortado.</span><span class="sxs-lookup"><span data-stu-id="fbee4-115">If the text does not fit within the control, the text is cropped.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="fbee4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbee4-116">Remarks</span></span>

<span data-ttu-id="fbee4-117">O controle de texto não separa as palavras.</span><span class="sxs-lookup"><span data-stu-id="fbee4-117">The Text control does not split words apart.</span></span> <span data-ttu-id="fbee4-118">Se uma palavra ultrapassar a largura do controle, a quebra automática de linha será empregada para mover a palavra para a próxima.</span><span class="sxs-lookup"><span data-stu-id="fbee4-118">If a word extends beyond the width of the control, word wrap is employed to move the word to the next line.</span></span> <span data-ttu-id="fbee4-119">Se uma única palavra for maior do que a largura do controle, essa palavra será recortada e ocupará uma única linha.</span><span class="sxs-lookup"><span data-stu-id="fbee4-119">If a single word is longer than the control width, that word is clipped and occupies a single line.</span></span>

<span data-ttu-id="fbee4-120">Se o atributo **Width** não for especificado, **WordWrap** será ignorado e o controle Text será redimensionado em vez de encapsular o texto.</span><span class="sxs-lookup"><span data-stu-id="fbee4-120">If the **width** attribute is not specified, **wordWrap** is ignored and the Text control will resize rather than wrapping the text.</span></span>

<span data-ttu-id="fbee4-121">Se as quebras de linha forem desejadas em locais específicos, elas deverão ser especificadas explicitamente em **valor** usando "&\# 13;" ou " \\ r".</span><span class="sxs-lookup"><span data-stu-id="fbee4-121">If line breaks are desired in particular locations, they must be explicitly specified in **value** using "&\#13;" or "\\r".</span></span> <span data-ttu-id="fbee4-122">Se o último formulário for usado ao especificar o valor diretamente, a cadeia de caracteres deverá ser prefixada com "JScript:" e o valor real deverá estar entre aspas simples, como mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="fbee4-122">If the latter form is used when specifying the value directly, the string must be prefixed with "JScript:" and the actual value must be surrounded by single quotes, as shown below.</span></span> <span data-ttu-id="fbee4-123">Isso não será necessário se o valor for definido dinamicamente de dentro de um manipulador de eventos.</span><span class="sxs-lookup"><span data-stu-id="fbee4-123">This is not necessary if the value is set dynamically from within an event handler.</span></span>

<span data-ttu-id="fbee4-124">Se **WordWrap** for definido como true e **ToolTip** não for especificado, a dica de ferramenta exibirá o texto completo do atributo **Value** .</span><span class="sxs-lookup"><span data-stu-id="fbee4-124">If **wordWrap** is set to true and **toolTip** is not specified, the ToolTip will display the full text of the **value** attribute.</span></span> <span data-ttu-id="fbee4-125">Se nenhuma dica de ferramenta for desejada, defina **ToolTip** como "" (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="fbee4-125">If no ToolTip is desired, set **toolTip** to "" (empty string).</span></span>

## <a name="examples"></a><span data-ttu-id="fbee4-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fbee4-126">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="fbee4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbee4-127">Requirements</span></span>



| <span data-ttu-id="fbee4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbee4-128">Requirement</span></span> | <span data-ttu-id="fbee4-129">Valor</span><span class="sxs-lookup"><span data-stu-id="fbee4-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fbee4-130">Versão</span><span class="sxs-lookup"><span data-stu-id="fbee4-130">Version</span></span><br/> | <span data-ttu-id="fbee4-131">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fbee4-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbee4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbee4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbee4-133">**Ambiente. largura**</span><span class="sxs-lookup"><span data-stu-id="fbee4-133">**AmbientAttributes.width**</span></span>](ambientattributes-width.md)
</dt> <dt>

[<span data-ttu-id="fbee4-134">**Elemento de texto**</span><span class="sxs-lookup"><span data-stu-id="fbee4-134">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="fbee4-135">**TEXT. toolTip**</span><span class="sxs-lookup"><span data-stu-id="fbee4-135">**TEXT.toolTip**</span></span>](text-tooltip.md)
</dt> <dt>

[<span data-ttu-id="fbee4-136">**TEXT. Value**</span><span class="sxs-lookup"><span data-stu-id="fbee4-136">**TEXT.value**</span></span>](text-value.md)
</dt> </dl>

 

 





