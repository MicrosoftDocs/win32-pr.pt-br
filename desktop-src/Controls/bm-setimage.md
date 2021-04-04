---
title: Mensagem de BM_SETIMAGE (WinUser. h)
description: Associa uma nova imagem (ícone ou bitmap) ao botão.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Controles de BM_SETIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085290"
---
# <a name="bm_setimage-message"></a><span data-ttu-id="12bb3-104">\_Mensagem BM SETimage</span><span class="sxs-lookup"><span data-stu-id="12bb3-104">BM\_SETIMAGE message</span></span>

<span data-ttu-id="12bb3-105">Associa uma nova imagem (ícone ou bitmap) ao botão.</span><span class="sxs-lookup"><span data-stu-id="12bb3-105">Associates a new image (icon or bitmap) with the button.</span></span>

## <a name="parameters"></a><span data-ttu-id="12bb3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12bb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12bb3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12bb3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12bb3-108">O tipo de imagem a ser associado ao botão.</span><span class="sxs-lookup"><span data-stu-id="12bb3-108">The type of image to associate with the button.</span></span> <span data-ttu-id="12bb3-109">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="12bb3-109">This parameter can be one of the following values:</span></span>

-   <span data-ttu-id="12bb3-110">BITMAP de imagem \_</span><span class="sxs-lookup"><span data-stu-id="12bb3-110">IMAGE\_BITMAP</span></span>
-   <span data-ttu-id="12bb3-111">ícone de imagem \_</span><span class="sxs-lookup"><span data-stu-id="12bb3-111">IMAGE\_ICON</span></span>

</dd> <dt>

<span data-ttu-id="12bb3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12bb3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12bb3-113">Um identificador (**HICON** ou **HBITMAP**) para a imagem a ser associada ao botão.</span><span class="sxs-lookup"><span data-stu-id="12bb3-113">A handle (**HICON** or **HBITMAP**) to the image to associate with the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12bb3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12bb3-114">Return value</span></span>

<span data-ttu-id="12bb3-115">O valor de retorno é um identificador para a imagem associada anteriormente ao botão, se houver; caso contrário, será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="12bb3-115">The return value is a handle to the image previously associated with the button, if any; otherwise, it is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="12bb3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="12bb3-116">Remarks</span></span>

<span data-ttu-id="12bb3-117">A aparência do texto, um ícone ou ambos em um controle de botão depende do [**\_ ícone de BS**](button-styles.md) e dos estilos de [**\_ bitmap BS**](button-styles.md) , e se a mensagem **\_ SetImage BM** é chamada.</span><span class="sxs-lookup"><span data-stu-id="12bb3-117">The appearance of text, an icon, or both on a button control depends on the [**BS\_ICON**](button-styles.md) and [**BS\_BITMAP**](button-styles.md) styles, and whether the **BM\_SETIMAGE** message is called.</span></span> <span data-ttu-id="12bb3-118">Os resultados possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="12bb3-118">The possible results are as follows:</span></span>



| <span data-ttu-id="12bb3-119">\_Ícone de BS ou \_ bitmap BS definido?</span><span class="sxs-lookup"><span data-stu-id="12bb3-119">BS\_ICON or BS\_BITMAP Set?</span></span> | <span data-ttu-id="12bb3-120">BM \_ SetImage chamada?</span><span class="sxs-lookup"><span data-stu-id="12bb3-120">BM\_SETIMAGE Called?</span></span> | <span data-ttu-id="12bb3-121">Resultado</span><span class="sxs-lookup"><span data-stu-id="12bb3-121">Result</span></span>              |
|-----------------------------|----------------------|---------------------|
| <span data-ttu-id="12bb3-122">Sim</span><span class="sxs-lookup"><span data-stu-id="12bb3-122">Yes</span></span>                         | <span data-ttu-id="12bb3-123">Sim</span><span class="sxs-lookup"><span data-stu-id="12bb3-123">Yes</span></span>                  | <span data-ttu-id="12bb3-124">Mostrar apenas o ícone.</span><span class="sxs-lookup"><span data-stu-id="12bb3-124">Show icon only.</span></span>     |
| <span data-ttu-id="12bb3-125">Não</span><span class="sxs-lookup"><span data-stu-id="12bb3-125">No</span></span>                          | <span data-ttu-id="12bb3-126">Sim</span><span class="sxs-lookup"><span data-stu-id="12bb3-126">Yes</span></span>                  | <span data-ttu-id="12bb3-127">Mostrar ícone e texto.</span><span class="sxs-lookup"><span data-stu-id="12bb3-127">Show icon and text.</span></span> |
| <span data-ttu-id="12bb3-128">Sim</span><span class="sxs-lookup"><span data-stu-id="12bb3-128">Yes</span></span>                         | <span data-ttu-id="12bb3-129">Não</span><span class="sxs-lookup"><span data-stu-id="12bb3-129">No</span></span>                   | <span data-ttu-id="12bb3-130">Mostrar somente texto.</span><span class="sxs-lookup"><span data-stu-id="12bb3-130">Show text only.</span></span>     |
| <span data-ttu-id="12bb3-131">Não</span><span class="sxs-lookup"><span data-stu-id="12bb3-131">No</span></span>                          | <span data-ttu-id="12bb3-132">Não</span><span class="sxs-lookup"><span data-stu-id="12bb3-132">No</span></span>                   | <span data-ttu-id="12bb3-133">Mostrar somente texto</span><span class="sxs-lookup"><span data-stu-id="12bb3-133">Show text only</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="12bb3-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12bb3-134">Requirements</span></span>



| <span data-ttu-id="12bb3-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bb3-135">Requirement</span></span> | <span data-ttu-id="12bb3-136">Valor</span><span class="sxs-lookup"><span data-stu-id="12bb3-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12bb3-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12bb3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="12bb3-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12bb3-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12bb3-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12bb3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="12bb3-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12bb3-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12bb3-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12bb3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="12bb3-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12bb3-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12bb3-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="12bb3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bb3-144">**BM \_ GETimage**</span><span class="sxs-lookup"><span data-stu-id="12bb3-144">**BM\_GETIMAGE**</span></span>](bm-getimage.md)
</dt> </dl>

 

 





