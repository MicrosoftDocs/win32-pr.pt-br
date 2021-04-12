---
title: Mensagem de WM_DWMWINDOWMAXIMIZEDCHANGE (WinUser. h)
description: Enviado quando uma janela composta de Gerenciador de Janelas da Área de Trabalho (DWM) é maximizada.
ms.assetid: db8cd104-388e-4211-9e4e-f169aef9651c
keywords:
- Mensagem de WM_DWMWINDOWMAXIMIZEDCHANGE Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMWINDOWMAXIMIZEDCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc49af267ea826eb9e35a627e14f6fc8b381df0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369653"
---
# <a name="wm_dwmwindowmaximizedchange-message"></a><span data-ttu-id="898f6-104">Mensagem do WM \_ DWMWINDOWMAXIMIZEDCHANGE</span><span class="sxs-lookup"><span data-stu-id="898f6-104">WM\_DWMWINDOWMAXIMIZEDCHANGE message</span></span>

<span data-ttu-id="898f6-105">Enviado quando uma janela composta de Gerenciador de Janelas da Área de Trabalho (DWM) é maximizada.</span><span class="sxs-lookup"><span data-stu-id="898f6-105">Sent when a Desktop Window Manager (DWM) composed window is maximized.</span></span>

## <a name="parameters"></a><span data-ttu-id="898f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="898f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="898f6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="898f6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="898f6-108">Defina como true para especificar que a janela foi maximizada.</span><span class="sxs-lookup"><span data-stu-id="898f6-108">Set to true to specify that the window has been maximized.</span></span>

</dd> <dt>

<span data-ttu-id="898f6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="898f6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="898f6-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="898f6-110">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="898f6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="898f6-111">Return value</span></span>

<span data-ttu-id="898f6-112">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="898f6-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="898f6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="898f6-113">Remarks</span></span>

<span data-ttu-id="898f6-114">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="898f6-114">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="898f6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="898f6-115">Requirements</span></span>



| <span data-ttu-id="898f6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="898f6-116">Requirement</span></span> | <span data-ttu-id="898f6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="898f6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="898f6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="898f6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="898f6-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="898f6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="898f6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="898f6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="898f6-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="898f6-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="898f6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="898f6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="898f6-123"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="898f6-123"><dt>Winuser.h</dt></span></span> </dl> |



 

