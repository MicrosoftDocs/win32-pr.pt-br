---
title: Mensagem de WM_DESTROYCLIPBOARD (WinUser. h)
description: Enviado ao proprietário da área de transferência quando uma chamada para a função EmptyClipboard esvazia a área de transferência. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 9f75b7fb-e9ae-4876-ba99-7db931b9c2ff
keywords:
- Troca de dados de mensagem WM_DESTROYCLIPBOARD
topic_type:
- apiref
api_name:
- WM_DESTROYCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3e4b6c2e2d378d0f78cee1824b1e4ce17a433a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919178"
---
# <a name="wm_destroyclipboard-message"></a><span data-ttu-id="dae4d-105">Mensagem do WM \_ DESTROYCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="dae4d-105">WM\_DESTROYCLIPBOARD message</span></span>

<span data-ttu-id="dae4d-106">Enviado ao proprietário da área de transferência quando uma chamada para a função [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) esvazia a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="dae4d-106">Sent to the clipboard owner when a call to the [**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard) function empties the clipboard.</span></span>

<span data-ttu-id="dae4d-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="dae4d-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_DESTROYCLIPBOARD             0x0307
```



## <a name="parameters"></a><span data-ttu-id="dae4d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dae4d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae4d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dae4d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dae4d-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dae4d-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dae4d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dae4d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dae4d-112">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dae4d-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dae4d-113">Return value</span></span>

<span data-ttu-id="dae4d-114">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="dae4d-114">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="dae4d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dae4d-115">Requirements</span></span>



| <span data-ttu-id="dae4d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dae4d-116">Requirement</span></span> | <span data-ttu-id="dae4d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dae4d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae4d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dae4d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dae4d-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dae4d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dae4d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dae4d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dae4d-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dae4d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dae4d-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dae4d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dae4d-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dae4d-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dae4d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dae4d-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="dae4d-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="dae4d-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dae4d-126">**EmptyClipboard**</span><span class="sxs-lookup"><span data-stu-id="dae4d-126">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

<span data-ttu-id="dae4d-127">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="dae4d-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dae4d-128">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="dae4d-128">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

