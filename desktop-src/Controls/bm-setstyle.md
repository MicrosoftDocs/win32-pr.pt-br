---
title: Mensagem de BM_SETSTYLE (WinUser. h)
description: Define o estilo de um botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetStyle do botão.
ms.assetid: 6439e68f-87fc-4a4a-8025-facc3c0e03e2
keywords:
- Controles de BM_SETSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETSTYLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c080e1098d70b17e1e68bbbcd2d5598db79ef8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918172"
---
# <a name="bm_setstyle-message"></a><span data-ttu-id="65201-105">BM \_ mensagem SETstyle</span><span class="sxs-lookup"><span data-stu-id="65201-105">BM\_SETSTYLE message</span></span>

<span data-ttu-id="65201-106">Define o estilo de um botão.</span><span class="sxs-lookup"><span data-stu-id="65201-106">Sets the style of a button.</span></span> <span data-ttu-id="65201-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetStyle do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .</span><span class="sxs-lookup"><span data-stu-id="65201-107">You can send this message explicitly or use the [**Button\_SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="65201-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65201-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65201-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65201-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65201-110">O estilo do botão.</span><span class="sxs-lookup"><span data-stu-id="65201-110">The button style.</span></span> <span data-ttu-id="65201-111">Esse parâmetro pode ser uma combinação de estilos de botão.</span><span class="sxs-lookup"><span data-stu-id="65201-111">This parameter can be a combination of button styles.</span></span> <span data-ttu-id="65201-112">Para obter uma tabela de estilos de botão, consulte [estilos de botão](button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="65201-112">For a table of button styles, see [Button Styles](button-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="65201-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65201-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65201-114">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) de *lParam* é um **bool** que especifica se o botão deve ser redesenhado.</span><span class="sxs-lookup"><span data-stu-id="65201-114">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of *lParam* is a **BOOL** that specifies whether the button is to be redrawn.</span></span> <span data-ttu-id="65201-115">Um valor de **true** redesenha o botão; um valor **false** não redesenha o botão.</span><span class="sxs-lookup"><span data-stu-id="65201-115">A value of **TRUE** redraws the button; a value of **FALSE** does not redraw the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65201-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65201-116">Return value</span></span>

<span data-ttu-id="65201-117">Essa mensagem sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="65201-117">This message always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="65201-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65201-118">Requirements</span></span>



| <span data-ttu-id="65201-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="65201-119">Requirement</span></span> | <span data-ttu-id="65201-120">Valor</span><span class="sxs-lookup"><span data-stu-id="65201-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65201-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65201-121">Minimum supported client</span></span><br/> | <span data-ttu-id="65201-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="65201-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="65201-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="65201-123">Minimum supported server</span></span><br/> | <span data-ttu-id="65201-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="65201-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="65201-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65201-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="65201-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65201-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

