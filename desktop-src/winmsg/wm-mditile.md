---
description: Um aplicativo envia a mensagem do WM \_ MDITILE para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas MDI em um formato de bloco.
ms.assetid: a480ba61-807e-4d0e-bda2-f1876e0bb13c
title: Mensagem de WM_MDITILE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf7ee38fbb3622e2d17bf4cea5a28b6b492a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164421"
---
# <a name="wm_mditile-message"></a><span data-ttu-id="a56ff-103">Mensagem do WM \_ MDITILE</span><span class="sxs-lookup"><span data-stu-id="a56ff-103">WM\_MDITILE message</span></span>

<span data-ttu-id="a56ff-104">Um aplicativo envia a mensagem do **WM \_ MDITILE** para uma janela de cliente MDI (interface de vários documentos) para organizar todas as janelas filhas MDI em um formato de bloco.</span><span class="sxs-lookup"><span data-stu-id="a56ff-104">An application sends the **WM\_MDITILE** message to a multiple-document interface (MDI) client window to arrange all of its MDI child windows in a tile format.</span></span>


```C++
#define WM_MDITILE                      0x0226
```



## <a name="parameters"></a><span data-ttu-id="a56ff-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a56ff-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56ff-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a56ff-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a56ff-107">A opção de divisão.</span><span class="sxs-lookup"><span data-stu-id="a56ff-107">The tiling option.</span></span> <span data-ttu-id="a56ff-108">Esse parâmetro pode ser um dos valores a seguir, opcionalmente combinado com **MDITILE \_ SKIPDISABLED** para impedir que janelas filho MDI desabilitadas sejam colocadas lado a lado.</span><span class="sxs-lookup"><span data-stu-id="a56ff-108">This parameter can be one of the following values, optionally combined with **MDITILE\_SKIPDISABLED** to prevent disabled MDI child windows from being tiled.</span></span>



| <span data-ttu-id="a56ff-109">Valor</span><span class="sxs-lookup"><span data-stu-id="a56ff-109">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="a56ff-110">Significado</span><span class="sxs-lookup"><span data-stu-id="a56ff-110">Meaning</span></span>                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MDITILE_HORIZONTAL"></span><span id="mditile_horizontal"></span><dl> <span data-ttu-id="a56ff-111"><dt>**MDITILE \_**</dt> <dt>0x0001</dt> horizontal</span><span class="sxs-lookup"><span data-stu-id="a56ff-111"><dt>**MDITILE\_HORIZONTAL**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="a56ff-112">Janelas de blocos horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="a56ff-112">Tiles windows horizontally.</span></span><br/> |
| <span id="MDITILE_VERTICAL"></span><span id="mditile_vertical"></span><dl> <span data-ttu-id="a56ff-113"><dt>**MDITILE \_**</dt> <dt>0x0000</dt> vertical</span><span class="sxs-lookup"><span data-stu-id="a56ff-113"><dt>**MDITILE\_VERTICAL**</dt> <dt>0x0000</dt></span></span> </dl>       | <span data-ttu-id="a56ff-114">Janelas de blocos verticalmente.</span><span class="sxs-lookup"><span data-stu-id="a56ff-114">Tiles windows vertically.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a56ff-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a56ff-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a56ff-116">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a56ff-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56ff-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a56ff-117">Return value</span></span>

<span data-ttu-id="a56ff-118">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="a56ff-118">Type: **BOOL**</span></span>

<span data-ttu-id="a56ff-119">Se a mensagem tiver sucesso, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="a56ff-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="a56ff-120">Se a mensagem falhar, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="a56ff-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56ff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a56ff-121">Requirements</span></span>



| <span data-ttu-id="a56ff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56ff-122">Requirement</span></span> | <span data-ttu-id="a56ff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a56ff-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56ff-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a56ff-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a56ff-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a56ff-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a56ff-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a56ff-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a56ff-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a56ff-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a56ff-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a56ff-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a56ff-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a56ff-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a56ff-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a56ff-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a56ff-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a56ff-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a56ff-132">**MDICASCADE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a56ff-132">**WM\_MDICASCADE**</span></span>](wm-mdicascade.md)
</dt> <dt>

[<span data-ttu-id="a56ff-133">**MDIICONARRANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a56ff-133">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

<span data-ttu-id="a56ff-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a56ff-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a56ff-135">Interface de vários documentos</span><span class="sxs-lookup"><span data-stu-id="a56ff-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




