---
title: Exibir. tamanho
description: O método de tamanho redimensiona a exibição em uma borda especificada.
ms.assetid: c15a33b2-3618-41a7-bff1-9d48a566ed4f
keywords:
- Exibir. dimensionar o Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.size
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: def9b416dfe5eda052ef430b587fa1c6017b4e5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813732"
---
# <a name="viewsize"></a><span data-ttu-id="e114b-104">Exibir. tamanho</span><span class="sxs-lookup"><span data-stu-id="e114b-104">VIEW.size</span></span>

<span data-ttu-id="e114b-105">O método de **tamanho** redimensiona a **exibição** em uma borda especificada.</span><span class="sxs-lookup"><span data-stu-id="e114b-105">The **size** method resizes the **VIEW** on a specified edge.</span></span>

``` syntax
        elementID.size(handle)
```

## <a name="parameters"></a><span data-ttu-id="e114b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e114b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e114b-107"><span id="handle"></span><span id="HANDLE"></span>*processamento*</span><span class="sxs-lookup"><span data-stu-id="e114b-107"><span id="handle"></span><span id="HANDLE"></span>*handle*</span></span>
</dt> <dd>

<span data-ttu-id="e114b-108">Cadeia de caracteres que especifica a borda ou o canto a ser movido ao Dimensionar.</span><span class="sxs-lookup"><span data-stu-id="e114b-108">String specifying the edge or corner to move when sizing.</span></span> <span data-ttu-id="e114b-109">Essa cadeia de caracteres deve ter um dos oito valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e114b-109">This string must have one of the following eight values.</span></span>



| <span data-ttu-id="e114b-110">Edge</span><span class="sxs-lookup"><span data-stu-id="e114b-110">Edge</span></span>   | <span data-ttu-id="e114b-111">Canto</span><span class="sxs-lookup"><span data-stu-id="e114b-111">Corner</span></span>      |
|--------|-------------|
| <span data-ttu-id="e114b-112">top</span><span class="sxs-lookup"><span data-stu-id="e114b-112">top</span></span>    | <span data-ttu-id="e114b-113">canto superior</span><span class="sxs-lookup"><span data-stu-id="e114b-113">topright</span></span>    |
| <span data-ttu-id="e114b-114">direita</span><span class="sxs-lookup"><span data-stu-id="e114b-114">right</span></span>  | <span data-ttu-id="e114b-115">bottomright</span><span class="sxs-lookup"><span data-stu-id="e114b-115">bottomright</span></span> |
| <span data-ttu-id="e114b-116">parte inferior</span><span class="sxs-lookup"><span data-stu-id="e114b-116">bottom</span></span> | <span data-ttu-id="e114b-117">bottomleft</span><span class="sxs-lookup"><span data-stu-id="e114b-117">bottomleft</span></span>  |
| <span data-ttu-id="e114b-118">esquerda</span><span class="sxs-lookup"><span data-stu-id="e114b-118">left</span></span>   | <span data-ttu-id="e114b-119">topleft</span><span class="sxs-lookup"><span data-stu-id="e114b-119">topleft</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e114b-120">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e114b-120">Return Value</span></span>

<span data-ttu-id="e114b-121">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e114b-121">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e114b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="e114b-122">Remarks</span></span>

<span data-ttu-id="e114b-123">Esse método é normalmente chamado de dentro de um manipulador de **OnMouseDown** .</span><span class="sxs-lookup"><span data-stu-id="e114b-123">This method is typically called from within an **onmousedown** handler.</span></span> <span data-ttu-id="e114b-124">Ele cuida do redimensionamento enquanto o mouse é arrastado e para o redimensionamento quando o botão do mouse é liberado.</span><span class="sxs-lookup"><span data-stu-id="e114b-124">It takes care of resizing while the mouse is dragged and stops resizing when the mouse button is released.</span></span> <span data-ttu-id="e114b-125">Se o tamanho da **exibição** for restrito, você não poderá arrastar o mouse para redimensionar a **exibição** além dos limites restritos.</span><span class="sxs-lookup"><span data-stu-id="e114b-125">If the size of the **VIEW** is restricted, you cannot drag the mouse to resize the **View** beyond the restricted bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="e114b-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e114b-126">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="sizer" horizontalAlignment="right" 
        verticalAlignment="bottom" image="Open.png" 
        onmousedown="jscript:View1.size('bottomright')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="e114b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e114b-127">Requirements</span></span>



| <span data-ttu-id="e114b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e114b-128">Requirement</span></span> | <span data-ttu-id="e114b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="e114b-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e114b-130">Versão</span><span class="sxs-lookup"><span data-stu-id="e114b-130">Version</span></span><br/> | <span data-ttu-id="e114b-131">Windows Media Player versão 7,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="e114b-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e114b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e114b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e114b-133">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="e114b-133">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





