---
title: Mensagem de TCM_HITTEST (commctrl. h)
description: Determina qual guia, se houver, está em uma posição de tela especificada. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ HitTest.
ms.assetid: 0334f616-8d39-4460-a7f8-692a9ffab012
keywords:
- Controles de TCM_HITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04787662e417513d8c9c93e45cecd0d8bddc6cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754372"
---
# <a name="tcm_hittest-message"></a><span data-ttu-id="b8e3c-105">\_Mensagem de HITTEST TCM</span><span class="sxs-lookup"><span data-stu-id="b8e3c-105">TCM\_HITTEST message</span></span>

<span data-ttu-id="b8e3c-106">Determina qual guia, se houver, está em uma posição de tela especificada.</span><span class="sxs-lookup"><span data-stu-id="b8e3c-106">Determines which tab, if any, is at a specified screen position.</span></span> <span data-ttu-id="b8e3c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) .</span><span class="sxs-lookup"><span data-stu-id="b8e3c-107">You can send this message explicitly or by using the [**TabCtrl\_HitTest**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_hittest) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8e3c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8e3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e3c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8e3c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b8e3c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b8e3c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b8e3c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8e3c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8e3c-112">Ponteiro para uma estrutura [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) que especifica a posição da tela a ser testada.</span><span class="sxs-lookup"><span data-stu-id="b8e3c-112">Pointer to a [**TCHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tchittestinfo) structure that specifies the screen position to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e3c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8e3c-113">Return value</span></span>

<span data-ttu-id="b8e3c-114">Retorna o índice da guia ou-1 se nenhuma guia estiver na posição especificada.</span><span class="sxs-lookup"><span data-stu-id="b8e3c-114">Returns the index of the tab, or -1 if no tab is at the specified position.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e3c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8e3c-115">Requirements</span></span>



| <span data-ttu-id="b8e3c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8e3c-116">Requirement</span></span> | <span data-ttu-id="b8e3c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b8e3c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e3c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8e3c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e3c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8e3c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8e3c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8e3c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e3c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8e3c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8e3c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8e3c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8e3c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8e3c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





