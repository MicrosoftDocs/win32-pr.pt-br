---
description: Enviado para uma janela que o usuário está redimensionando. Ao processar essa mensagem, um aplicativo pode monitorar o tamanho e a posição do retângulo de arrastar e, se necessário, alterar seu tamanho ou posição.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Mensagem de WM_SIZING (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662199"
---
# <a name="wm_sizing-message"></a><span data-ttu-id="c597e-104">\_Mensagem de dimensionamento do WM</span><span class="sxs-lookup"><span data-stu-id="c597e-104">WM\_SIZING message</span></span>

<span data-ttu-id="c597e-105">Enviado para uma janela que o usuário está redimensionando.</span><span class="sxs-lookup"><span data-stu-id="c597e-105">Sent to a window that the user is resizing.</span></span> <span data-ttu-id="c597e-106">Ao processar essa mensagem, um aplicativo pode monitorar o tamanho e a posição do retângulo de arrastar e, se necessário, alterar seu tamanho ou posição.</span><span class="sxs-lookup"><span data-stu-id="c597e-106">By processing this message, an application can monitor the size and position of the drag rectangle and, if needed, change its size or position.</span></span>

<span data-ttu-id="c597e-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="c597e-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a><span data-ttu-id="c597e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c597e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c597e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c597e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c597e-110">A borda da janela que está sendo dimensionada.</span><span class="sxs-lookup"><span data-stu-id="c597e-110">The edge of the window that is being sized.</span></span> <span data-ttu-id="c597e-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c597e-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="c597e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c597e-112">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="c597e-113">Significado</span><span class="sxs-lookup"><span data-stu-id="c597e-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <span data-ttu-id="c597e-114"><dt>**WMSZ \_**</dt> <dt>6</dt> últimos</span><span class="sxs-lookup"><span data-stu-id="c597e-114"><dt>**WMSZ\_BOTTOM**</dt> <dt>6</dt></span></span> </dl>                | <span data-ttu-id="c597e-115">Borda inferior</span><span class="sxs-lookup"><span data-stu-id="c597e-115">Bottom edge</span></span><br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <span data-ttu-id="c597e-116"><dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-116"><dt>**WMSZ\_BOTTOMLEFT**</dt> <dt>7</dt></span></span> </dl>    | <span data-ttu-id="c597e-117">Canto inferior esquerdo</span><span class="sxs-lookup"><span data-stu-id="c597e-117">Bottom-left corner</span></span><br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <span data-ttu-id="c597e-118"><dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-118"><dt>**WMSZ\_BOTTOMRIGHT**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="c597e-119">Canto inferior direito</span><span class="sxs-lookup"><span data-stu-id="c597e-119">Bottom-right corner</span></span><br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <span data-ttu-id="c597e-120"><dt>**WMSZ \_ ESQUERDA**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-120"><dt>**WMSZ\_LEFT**</dt> <dt>1</dt></span></span> </dl>                      | <span data-ttu-id="c597e-121">Borda esquerda</span><span class="sxs-lookup"><span data-stu-id="c597e-121">Left edge</span></span><br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <span data-ttu-id="c597e-122"><dt>**WMSZ \_ DIREITA**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-122"><dt>**WMSZ\_RIGHT**</dt> <dt>2</dt></span></span> </dl>                   | <span data-ttu-id="c597e-123">Borda direita</span><span class="sxs-lookup"><span data-stu-id="c597e-123">Right edge</span></span><br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <span data-ttu-id="c597e-124"><dt>**WMSZ \_**</dt> <dt>3</dt> principais</span><span class="sxs-lookup"><span data-stu-id="c597e-124"><dt>**WMSZ\_TOP**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="c597e-125">Borda superior</span><span class="sxs-lookup"><span data-stu-id="c597e-125">Top edge</span></span><br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <span data-ttu-id="c597e-126"><dt>**WMSZ \_ TOPLEFT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-126"><dt>**WMSZ\_TOPLEFT**</dt> <dt>4</dt></span></span> </dl>             | <span data-ttu-id="c597e-127">Canto superior esquerdo</span><span class="sxs-lookup"><span data-stu-id="c597e-127">Top-left corner</span></span><br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <span data-ttu-id="c597e-128"><dt>**WMSZ \_ CANTO superior**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-128"><dt>**WMSZ\_TOPRIGHT**</dt> <dt>5</dt></span></span> </dl>          | <span data-ttu-id="c597e-129">Canto superior direito</span><span class="sxs-lookup"><span data-stu-id="c597e-129">Top-right corner</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="c597e-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c597e-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c597e-131">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com as coordenadas de tela do retângulo de arrastar.</span><span class="sxs-lookup"><span data-stu-id="c597e-131">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure with the screen coordinates of the drag rectangle.</span></span> <span data-ttu-id="c597e-132">Para alterar o tamanho ou a posição do retângulo de arrastar, um aplicativo deve alterar os membros dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="c597e-132">To change the size or position of the drag rectangle, an application must change the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c597e-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c597e-133">Return value</span></span>

<span data-ttu-id="c597e-134">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="c597e-134">Type: **LRESULT**</span></span>

<span data-ttu-id="c597e-135">Um aplicativo deve retornar **true** se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c597e-135">An application should return **TRUE** if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c597e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c597e-136">Requirements</span></span>



| <span data-ttu-id="c597e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c597e-137">Requirement</span></span> | <span data-ttu-id="c597e-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c597e-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c597e-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c597e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c597e-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c597e-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c597e-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c597e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c597e-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c597e-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c597e-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c597e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c597e-144"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c597e-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c597e-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="c597e-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="c597e-146">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c597e-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c597e-147">**movimentação do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c597e-147">**WM\_MOVING**</span></span>](wm-moving.md)
</dt> <dt>

[<span data-ttu-id="c597e-148">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c597e-148">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

<span data-ttu-id="c597e-149">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c597e-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c597e-150">Windows</span><span class="sxs-lookup"><span data-stu-id="c597e-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="c597e-151">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="c597e-151">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c597e-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c597e-152">[**RECT**](/previous-versions//dd162897(v=vs.85))</span></span>
</dt> </dl>

 

 
