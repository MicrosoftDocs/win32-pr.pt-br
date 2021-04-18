---
title: Mensagem de WM_PAINTCLIPBOARD (WinUser. h)
description: Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no \_ formato OWNERDISPLAY do
ms.assetid: 85aeefa5-e3d9-4689-a068-47b59ec7b571
keywords:
- Troca de dados de mensagem WM_PAINTCLIPBOARD
topic_type:
- apiref
api_name:
- WM_PAINTCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8148af6b513fd1fa956d48f22dc86e618544b073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757452"
---
# <a name="wm_paintclipboard-message"></a><span data-ttu-id="24392-104">Mensagem do WM \_ PAINTCLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="24392-104">WM\_PAINTCLIPBOARD message</span></span>

<span data-ttu-id="24392-105">Enviado para o proprietário da área de transferência por uma janela do Visualizador da área de transferência quando a área de transferência contém dados no formato [**\_ OWNERDISPLAY**](standard-clipboard-formats.md) do</span><span class="sxs-lookup"><span data-stu-id="24392-105">Sent to the clipboard owner by a clipboard viewer window when the clipboard contains data in the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format and the clipboard viewer's client area needs repainting.</span></span>


```C++
#define WM_PAINTCLIPBOARD               0x0309
```



## <a name="parameters"></a><span data-ttu-id="24392-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24392-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24392-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24392-108">Um identificador para a janela do Visualizador da área de transferência.</span><span class="sxs-lookup"><span data-stu-id="24392-108">A handle to the clipboard viewer window.</span></span>

</dd> <dt>

<span data-ttu-id="24392-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24392-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24392-110">Um identificador para um objeto de memória global que contém uma estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="24392-110">A handle to a global memory object that contains a [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="24392-111">A estrutura define a parte da área do cliente a ser pintada.</span><span class="sxs-lookup"><span data-stu-id="24392-111">The structure defines the part of the client area to paint.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24392-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24392-112">Return value</span></span>

<span data-ttu-id="24392-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="24392-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="24392-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="24392-114">Remarks</span></span>

<span data-ttu-id="24392-115">Para determinar se toda a área do cliente ou apenas uma parte dela precisa ser redesenhada, o proprietário da área de transferência deve comparar as dimensões das áreas de desenho fornecidas no membro **rcPaint** de [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) para as dimensões fornecidas na mensagem mais recente do [**WM \_ SIZECLIPBOARD**](wm-sizeclipboard.md) .</span><span class="sxs-lookup"><span data-stu-id="24392-115">To determine whether the entire client area or just a portion of it needs repainting, the clipboard owner must compare the dimensions of the drawing area given in the **rcPaint** member of [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) to the dimensions given in the most recent [**WM\_SIZECLIPBOARD**](wm-sizeclipboard.md) message.</span></span>

<span data-ttu-id="24392-116">O proprietário da área de transferência deve usar a função [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) para bloquear a memória que contém a estrutura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) .</span><span class="sxs-lookup"><span data-stu-id="24392-116">The clipboard owner must use the [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock) function to lock the memory that contains the [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) structure.</span></span> <span data-ttu-id="24392-117">Antes de retornar, o proprietário da área de transferência deve desbloquear essa memória usando a função [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) .</span><span class="sxs-lookup"><span data-stu-id="24392-117">Before returning, the clipboard owner must unlock that memory by using the [**GlobalUnlock**](/windows/desktop/api/winbase/nf-winbase-globalunlock) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="24392-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24392-118">Requirements</span></span>



| <span data-ttu-id="24392-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="24392-119">Requirement</span></span> | <span data-ttu-id="24392-120">Valor</span><span class="sxs-lookup"><span data-stu-id="24392-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24392-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24392-121">Minimum supported client</span></span><br/> | <span data-ttu-id="24392-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24392-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="24392-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24392-123">Minimum supported server</span></span><br/> | <span data-ttu-id="24392-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="24392-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="24392-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="24392-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="24392-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24392-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24392-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="24392-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="24392-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="24392-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24392-129">**SIZECLIPBOARD do WM \_**</span><span class="sxs-lookup"><span data-stu-id="24392-129">**WM\_SIZECLIPBOARD**</span></span>](wm-sizeclipboard.md)
</dt> <dt>

<span data-ttu-id="24392-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="24392-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24392-131">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="24392-131">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

