---
title: Mensagem de TB_PRESSBUTTON (commctrl. h)
description: Pressiona ou libera o botão especificado em uma barra de ferramentas.
ms.assetid: 03f6c3c2-d679-4e3a-a07b-c7e46c97972a
keywords:
- Controles de TB_PRESSBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_PRESSBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b0e86092951b242cee7388fc0d5d1bbdbca835e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086010"
---
# <a name="tb_pressbutton-message"></a><span data-ttu-id="0174a-104">TB de \_ mensagem PRESSBUTTON</span><span class="sxs-lookup"><span data-stu-id="0174a-104">TB\_PRESSBUTTON message</span></span>

<span data-ttu-id="0174a-105">Pressiona ou libera o botão especificado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="0174a-105">Presses or releases the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0174a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0174a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0174a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0174a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0174a-108">Identificador de comando do botão a ser pressionado ou liberado.</span><span class="sxs-lookup"><span data-stu-id="0174a-108">Command identifier of the button to press or release.</span></span>

</dd> <dt>

<span data-ttu-id="0174a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0174a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0174a-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se o botão especificado deve ser pressionado ou liberado.</span><span class="sxs-lookup"><span data-stu-id="0174a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to press or release the specified button.</span></span> <span data-ttu-id="0174a-111">Se **for true**, o botão será pressionado.</span><span class="sxs-lookup"><span data-stu-id="0174a-111">If **TRUE**, the button is pressed.</span></span> <span data-ttu-id="0174a-112">Se for **false**, o botão será liberado.</span><span class="sxs-lookup"><span data-stu-id="0174a-112">If **FALSE**, the button is released.</span></span>

<span data-ttu-id="0174a-113">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0174a-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0174a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0174a-114">Return value</span></span>

<span data-ttu-id="0174a-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0174a-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0174a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0174a-116">Requirements</span></span>



| <span data-ttu-id="0174a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0174a-117">Requirement</span></span> | <span data-ttu-id="0174a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0174a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0174a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0174a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0174a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0174a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0174a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0174a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0174a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0174a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0174a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0174a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0174a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0174a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

