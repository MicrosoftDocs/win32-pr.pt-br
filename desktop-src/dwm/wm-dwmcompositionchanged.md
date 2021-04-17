---
title: Mensagem de WM_DWMCOMPOSITIONCHANGED (WinUser. h)
description: Informa todas as janelas de nível superior que a composição de Gerenciador de Janelas da Área de Trabalho (DWM) foi habilitada ou desabilitada.
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowmessages\wm_dwmcompositionchanged.htm
keywords:
- Mensagem de WM_DWMCOMPOSITIONCHANGED Gerenciador de Janelas da Área de Trabalho
topic_type:
- apiref
api_name:
- WM_DWMCOMPOSITIONCHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec25f740e1a5d002edec2c1faeaaf068190583c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763160"
---
# <a name="wm_dwmcompositionchanged-message"></a><span data-ttu-id="d9456-104">Mensagem do WM \_ DWMCOMPOSITIONCHANGED</span><span class="sxs-lookup"><span data-stu-id="d9456-104">WM\_DWMCOMPOSITIONCHANGED message</span></span>

<span data-ttu-id="d9456-105">Informa todas as janelas de nível superior que a composição de Gerenciador de Janelas da Área de Trabalho (DWM) foi habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="d9456-105">Informs all top-level windows that Desktop Window Manager (DWM) composition has been enabled or disabled.</span></span>

> [!Note]  
> <span data-ttu-id="d9456-106">A partir do Windows 8, a composição do DWM é sempre habilitada, portanto, essa mensagem não é enviada independentemente das alterações no modo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d9456-106">As of Windows 8, DWM composition is always enabled, so this message is not sent regardless of video mode changes.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="d9456-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d9456-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9456-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9456-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9456-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d9456-109">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="d9456-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9456-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9456-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d9456-111">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9456-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d9456-112">Return value</span></span>

<span data-ttu-id="d9456-113">Se um aplicativo processar essa mensagem, ele deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="d9456-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9456-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9456-114">Remarks</span></span>

<span data-ttu-id="d9456-115">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d9456-115">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

<span data-ttu-id="d9456-116">A função [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) pode ser usada para determinar o estado de composição atual.</span><span class="sxs-lookup"><span data-stu-id="d9456-116">The [**DwmIsCompositionEnabled**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled) function can be used to determine the current composition state.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9456-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9456-117">Requirements</span></span>



| <span data-ttu-id="d9456-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9456-118">Requirement</span></span> | <span data-ttu-id="d9456-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d9456-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d9456-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9456-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d9456-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d9456-121">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d9456-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d9456-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d9456-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d9456-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d9456-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9456-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9456-125"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9456-125"><dt>Winuser.h</dt></span></span> </dl> |



 

