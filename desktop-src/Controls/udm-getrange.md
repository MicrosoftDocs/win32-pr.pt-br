---
title: Mensagem de UDM_GETRANGE (commctrl. h)
description: Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.
ms.assetid: fd42538a-8d96-4a9c-a1db-07c3e9afef84
keywords:
- Controles de UDM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6fd8467ad4494bea92a4c1f9a68d675ef1471f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163627"
---
# <a name="udm_getrange-message"></a><span data-ttu-id="b528f-104">Mensagem do UDM \_ GETrange</span><span class="sxs-lookup"><span data-stu-id="b528f-104">UDM\_GETRANGE message</span></span>

<span data-ttu-id="b528f-105">Recupera as posições mínima e máxima (intervalo) para um controle acima-abaixo.</span><span class="sxs-lookup"><span data-stu-id="b528f-105">Retrieves the minimum and maximum positions (range) for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b528f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b528f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b528f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b528f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b528f-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b528f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b528f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b528f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b528f-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b528f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b528f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b528f-111">Return value</span></span>

<span data-ttu-id="b528f-112">O valor de retorno é um valor de 32 bits que contém as posições mínima e máxima.</span><span class="sxs-lookup"><span data-stu-id="b528f-112">The return value is a 32-bit value that contains the minimum and maximum positions.</span></span> <span data-ttu-id="b528f-113">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é a posição máxima do controle e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é a posição mínima.</span><span class="sxs-lookup"><span data-stu-id="b528f-113">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum position for the control, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is the minimum position.</span></span>

## <a name="requirements"></a><span data-ttu-id="b528f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b528f-114">Requirements</span></span>



| <span data-ttu-id="b528f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b528f-115">Requirement</span></span> | <span data-ttu-id="b528f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b528f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b528f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b528f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b528f-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b528f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b528f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b528f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b528f-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b528f-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b528f-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b528f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b528f-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b528f-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

