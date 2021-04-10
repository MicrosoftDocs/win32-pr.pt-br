---
title: Mensagem de BCM_SETSHIELD (commctrl. h)
description: Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados. Envie essa mensagem explicitamente ou usando o botão \_ SetElevationRequiredState macro.
ms.assetid: 2ce2a006-7136-415b-824b-46b282b100f4
keywords:
- Controles de BCM_SETSHIELD de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETSHIELD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2149e2945f2876309459c287961b7b0a4a1f9acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085468"
---
# <a name="bcm_setshield-message"></a><span data-ttu-id="2f4c1-105">\_Mensagem de SETshield do BCM</span><span class="sxs-lookup"><span data-stu-id="2f4c1-105">BCM\_SETSHIELD message</span></span>

<span data-ttu-id="2f4c1-106">Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="2f4c1-106">Sets the elevation required state for a specified button or command link to display an elevated icon.</span></span> <span data-ttu-id="2f4c1-107">Envie essa mensagem explicitamente ou usando o [**botão \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span><span class="sxs-lookup"><span data-stu-id="2f4c1-107">Send this message explicitly or by using the [**Button\_SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f4c1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f4c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f4c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f4c1-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2f4c1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2f4c1-111">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f4c1-111">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4c1-112">Um **bool** que é **verdadeiro** para desenhar um ícone com privilégios elevados ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="2f4c1-112">A **BOOL** that is **TRUE** to draw an elevated icon, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4c1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f4c1-113">Return value</span></span>

<span data-ttu-id="2f4c1-114">Retornará 1 se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="2f4c1-114">Returns 1 if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f4c1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f4c1-115">Remarks</span></span>

<span data-ttu-id="2f4c1-116">Um aplicativo deve ser manifestado para usar comctl32.dll versão 6 para obter essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="2f4c1-116">An application must be manifested to use comctl32.dll version 6 to gain this functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f4c1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f4c1-117">Requirements</span></span>



| <span data-ttu-id="2f4c1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f4c1-118">Requirement</span></span> | <span data-ttu-id="2f4c1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2f4c1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4c1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f4c1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f4c1-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f4c1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f4c1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f4c1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f4c1-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2f4c1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f4c1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f4c1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f4c1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f4c1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





