---
title: Mensagem de TB_HIDEBUTTON (commctrl. h)
description: Oculta ou mostra o botão especificado em uma barra de ferramentas.
ms.assetid: 57941a40-279a-426e-baf9-115429c62839
keywords:
- Controles de TB_HIDEBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_HIDEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198a48ae65f13be699b76a20c9f423cdb0da197
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918269"
---
# <a name="tb_hidebutton-message"></a><span data-ttu-id="3fdaa-104">TB de \_ mensagem HIDEBUTTON</span><span class="sxs-lookup"><span data-stu-id="3fdaa-104">TB\_HIDEBUTTON message</span></span>

<span data-ttu-id="3fdaa-105">Oculta ou mostra o botão especificado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-105">Hides or shows the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3fdaa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fdaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fdaa-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fdaa-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fdaa-108">Identificador de comando do botão a ser ocultado ou mostrado.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-108">Command identifier of the button to hide or show.</span></span>

</dd> <dt>

<span data-ttu-id="3fdaa-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fdaa-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fdaa-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se é para ocultar ou mostrar o botão especificado.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to hide or show the specified button.</span></span> <span data-ttu-id="3fdaa-111">Se for **true**, o botão ficará oculto.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-111">If **TRUE**, the button is hidden.</span></span> <span data-ttu-id="3fdaa-112">Se for **false**, o botão será mostrado.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-112">If **FALSE**, the button is shown.</span></span>

<span data-ttu-id="3fdaa-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fdaa-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3fdaa-114">Return value</span></span>

<span data-ttu-id="3fdaa-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3fdaa-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fdaa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fdaa-116">Requirements</span></span>



| <span data-ttu-id="3fdaa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fdaa-117">Requirement</span></span> | <span data-ttu-id="3fdaa-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3fdaa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdaa-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fdaa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3fdaa-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fdaa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fdaa-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fdaa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3fdaa-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fdaa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fdaa-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fdaa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fdaa-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fdaa-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

