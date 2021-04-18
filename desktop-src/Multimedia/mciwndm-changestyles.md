---
title: Mensagem de MCIWNDM_CHANGESTYLES (VFW. h)
description: A \_ mensagem MCIWNDM CHANGESTYLES altera os estilos usados pela janela MCIWnd. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndChangeStyles.
ms.assetid: 9074c21a-e49f-4089-a6d2-af8d513cb632
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CHANGESTYLES
topic_type:
- apiref
api_name:
- MCIWNDM_CHANGESTYLES
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2cea636c3c879da642da753c4fd084b06c4334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749975"
---
# <a name="mciwndm_changestyles-message"></a><span data-ttu-id="d890c-105">\_Mensagem MCIWNDM CHANGESTYLES</span><span class="sxs-lookup"><span data-stu-id="d890c-105">MCIWNDM\_CHANGESTYLES message</span></span>

<span data-ttu-id="d890c-106">A mensagem **MCIWNDM \_ CHANGESTYLES** altera os estilos usados pela janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="d890c-106">The **MCIWNDM\_CHANGESTYLES** message changes the styles used by the MCIWnd window.</span></span> <span data-ttu-id="d890c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) .</span><span class="sxs-lookup"><span data-stu-id="d890c-107">You can send this message explicitly or by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro.</span></span>


```C++
MCIWNDM_CHANGESTYLES 
wParam = (WPARAM) (UINT) mask; 
lParam = (LPARAM) (LONG) value; 
```



## <a name="parameters"></a><span data-ttu-id="d890c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d890c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d890c-109"><span id="mask"></span><span id="MASK"></span>*mascara*</span><span class="sxs-lookup"><span data-stu-id="d890c-109"><span id="mask"></span><span id="MASK"></span>*mask*</span></span>
</dt> <dd>

<span data-ttu-id="d890c-110">Máscara que identifica os estilos que podem ser alterados.</span><span class="sxs-lookup"><span data-stu-id="d890c-110">Mask that identifies the styles that can change.</span></span> <span data-ttu-id="d890c-111">Essa máscara é o operador OR de todos os estilos que terão permissão para alterar.</span><span class="sxs-lookup"><span data-stu-id="d890c-111">This mask is the bitwise OR operator of all styles that will be permitted to change.</span></span>

</dd> <dt>

<span data-ttu-id="d890c-112"><span id="value"></span><span id="VALUE"></span>*valor*</span><span class="sxs-lookup"><span data-stu-id="d890c-112"><span id="value"></span><span id="VALUE"></span>*value*</span></span>
</dt> <dd>

<span data-ttu-id="d890c-113">Novas configurações de estilo para a janela.</span><span class="sxs-lookup"><span data-stu-id="d890c-113">New style settings for the window.</span></span> <span data-ttu-id="d890c-114">Especifique zero para esse parâmetro para desativar todos os estilos identificados na máscara.</span><span class="sxs-lookup"><span data-stu-id="d890c-114">Specify zero for this parameter to turn off all styles identified in the mask.</span></span> <span data-ttu-id="d890c-115">Para obter uma lista dos estilos disponíveis, consulte a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="d890c-115">For a list of the available styles, see the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d890c-116">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d890c-116">Return Value</span></span>

<span data-ttu-id="d890c-117">Retorna zero.</span><span class="sxs-lookup"><span data-stu-id="d890c-117">Returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="d890c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d890c-118">Requirements</span></span>



| <span data-ttu-id="d890c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d890c-119">Requirement</span></span> | <span data-ttu-id="d890c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d890c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d890c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d890c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d890c-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d890c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d890c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d890c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d890c-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d890c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d890c-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d890c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d890c-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d890c-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d890c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d890c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d890c-128">**MCIWndCreate**</span><span class="sxs-lookup"><span data-stu-id="d890c-128">**MCIWndCreate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)
</dt> <dt>

[<span data-ttu-id="d890c-129">**MCIWndChangeStyles**</span><span class="sxs-lookup"><span data-stu-id="d890c-129">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> </dl>

 

 





