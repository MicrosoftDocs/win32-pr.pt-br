---
title: Mensagem de TB_ENABLEBUTTON (commctrl. h)
description: Habilita ou desabilita o botão especificado em uma barra de ferramentas.
ms.assetid: d73851ee-f909-4b70-9514-c45cd3a7e999
keywords:
- Controles de TB_ENABLEBUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_ENABLEBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caf2fe865d49f9c89e31b1701abfcbf7991ae72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749306"
---
# <a name="tb_enablebutton-message"></a><span data-ttu-id="97ca4-104">TB de \_ mensagem ENABLEBUTTON</span><span class="sxs-lookup"><span data-stu-id="97ca4-104">TB\_ENABLEBUTTON message</span></span>

<span data-ttu-id="97ca4-105">Habilita ou desabilita o botão especificado em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="97ca4-105">Enables or disables the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="97ca4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97ca4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ca4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97ca4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97ca4-108">Identificador de comando do botão a ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="97ca4-108">Command identifier of the button to enable or disable.</span></span>

</dd> <dt>

<span data-ttu-id="97ca4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97ca4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97ca4-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é um **bool** que indica se o botão especificado deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="97ca4-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is a **BOOL** that indicates whether to enable or disable the specified button.</span></span> <span data-ttu-id="97ca4-111">Se for **true**, o botão será habilitado.</span><span class="sxs-lookup"><span data-stu-id="97ca4-111">If **TRUE**, the button is enabled.</span></span> <span data-ttu-id="97ca4-112">Se for **false**, o botão será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="97ca4-112">If **FALSE**, the button is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ca4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97ca4-113">Return value</span></span>

<span data-ttu-id="97ca4-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="97ca4-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="97ca4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="97ca4-115">Remarks</span></span>

<span data-ttu-id="97ca4-116">Quando um botão é habilitado, ele pode ser pressionado e verificado.</span><span class="sxs-lookup"><span data-stu-id="97ca4-116">When a button has been enabled, it can be pressed and checked.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ca4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97ca4-117">Requirements</span></span>



| <span data-ttu-id="97ca4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97ca4-118">Requirement</span></span> | <span data-ttu-id="97ca4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="97ca4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97ca4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97ca4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97ca4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97ca4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97ca4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97ca4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97ca4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97ca4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97ca4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97ca4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ca4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="97ca4-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

