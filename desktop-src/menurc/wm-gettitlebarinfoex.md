---
title: Mensagem de WM_GETTITLEBARINFOEX (WinUser. h)
description: Enviado para solicitar informações da barra de título estendida. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369356"
---
# <a name="wm_gettitlebarinfoex-message"></a><span data-ttu-id="55641-105">Mensagem do WM \_ GETTITLEBARINFOEX</span><span class="sxs-lookup"><span data-stu-id="55641-105">WM\_GETTITLEBARINFOEX message</span></span>

<span data-ttu-id="55641-106">Enviado para solicitar informações da barra de título estendida.</span><span class="sxs-lookup"><span data-stu-id="55641-106">Sent to request extended title bar information.</span></span> <span data-ttu-id="55641-107">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="55641-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a><span data-ttu-id="55641-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55641-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55641-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="55641-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55641-110">Esse parâmetro não é usado e deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="55641-110">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="55641-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="55641-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="55641-112">Um ponteiro para uma estrutura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="55641-112">A pointer to a [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span> <span data-ttu-id="55641-113">O remetente da mensagem é responsável por alocar memória para esta estrutura.</span><span class="sxs-lookup"><span data-stu-id="55641-113">The message sender is responsible for allocating memory for this structure.</span></span> <span data-ttu-id="55641-114">Defina o membro **cbSize** dessa estrutura como `sizeof(TITLEBARINFOEX)` antes de passar essa estrutura com a mensagem.</span><span class="sxs-lookup"><span data-stu-id="55641-114">Set the **cbSize** member of this structure to `sizeof(TITLEBARINFOEX)` before passing this structure with the message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55641-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="55641-115">Remarks</span></span>

<span data-ttu-id="55641-116">O exemplo a seguir mostra como o receptor de mensagem converte um valor de **lParam** para recuperar a estrutura [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="55641-116">The following example shows how the message receiver casts an **LPARAM** value to retrieve the [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span>

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a><span data-ttu-id="55641-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55641-117">Requirements</span></span>



| <span data-ttu-id="55641-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="55641-118">Requirement</span></span> | <span data-ttu-id="55641-119">Valor</span><span class="sxs-lookup"><span data-stu-id="55641-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55641-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55641-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55641-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55641-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55641-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55641-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55641-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55641-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="55641-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55641-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55641-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55641-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55641-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="55641-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55641-127">Visão geral dos menus</span><span class="sxs-lookup"><span data-stu-id="55641-127">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

