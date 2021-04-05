---
title: Mensagem de WM_DWMNCRENDERINGCHANGED (WinUser. h)
description: Enviado quando a política de renderização de área não cliente é alterada.
ms.assetid: 31beb127-ebec-49a8-8b65-de00941cbd67
keywords:
- Mensagem de WM_DWMNCRENDERINGCHANGED Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMNCRENDERINGCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac32704ea240ccfc4d4de913b940e098ff8f4de4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918531"
---
# <a name="wm_dwmncrenderingchanged-message"></a><span data-ttu-id="8a6ee-104">Mensagem do WM \_ DWMNCRENDERINGCHANGED</span><span class="sxs-lookup"><span data-stu-id="8a6ee-104">WM\_DWMNCRENDERINGCHANGED message</span></span>

<span data-ttu-id="8a6ee-105">Enviado quando a política de renderização de área não cliente é alterada.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-105">Sent when the non-client area rendering policy has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="8a6ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a6ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6ee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8a6ee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a6ee-108">Especifica se a renderização DWM está habilitada para a área não cliente da janela.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-108">Specifies whether DWM rendering is enabled for the non-client area of the window.</span></span> <span data-ttu-id="8a6ee-109">**Verdadeiro** se habilitado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-109">**TRUE** if enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8a6ee-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8a6ee-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8a6ee-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a6ee-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a6ee-112">Return value</span></span>

<span data-ttu-id="8a6ee-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6ee-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a6ee-114">Remarks</span></span>

<span data-ttu-id="8a6ee-115">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8a6ee-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="8a6ee-116">As funções [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) são usadas para obter ou definir a política de renderização que não é de cliente.</span><span class="sxs-lookup"><span data-stu-id="8a6ee-116">The [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions are used to get or set the non-client rendering policy.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6ee-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a6ee-117">Requirements</span></span>



| <span data-ttu-id="8a6ee-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a6ee-118">Requirement</span></span> | <span data-ttu-id="8a6ee-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8a6ee-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6ee-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a6ee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6ee-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a6ee-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8a6ee-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a6ee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6ee-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a6ee-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8a6ee-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a6ee-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a6ee-125"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a6ee-125"><dt>Winuser.h</dt></span></span> </dl> |



 

