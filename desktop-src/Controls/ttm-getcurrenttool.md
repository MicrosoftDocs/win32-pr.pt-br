---
title: Mensagem de TTM_GETCURRENTTOOL (commctrl. h)
description: Recupera as informações da ferramenta atual em um controle ToolTip.
ms.assetid: acb254cf-064c-4ed8-b488-a3138b648405
keywords:
- Controles de TTM_GETCURRENTTOOL de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETCURRENTTOOL
- TTM_GETCURRENTTOOLA
- TTM_GETCURRENTTOOLW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa6218bcb4ad9aa43c7ffba0d332786956d9a62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918471"
---
# <a name="ttm_getcurrenttool-message"></a><span data-ttu-id="23e8f-104">\_Mensagem TTM GETCURRENTTOOL</span><span class="sxs-lookup"><span data-stu-id="23e8f-104">TTM\_GETCURRENTTOOL message</span></span>

<span data-ttu-id="23e8f-105">Recupera as informações da ferramenta atual em um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="23e8f-105">Retrieves the information for the current tool in a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="23e8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23e8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23e8f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23e8f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="23e8f-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="23e8f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="23e8f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23e8f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23e8f-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recebe informações sobre a ferramenta atual.</span><span class="sxs-lookup"><span data-stu-id="23e8f-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the current tool.</span></span> <span data-ttu-id="23e8f-111">Se esse valor for **nulo**, o valor de retorno indicará a existência da ferramenta atual sem realmente recuperar as informações da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="23e8f-111">If this value is **NULL**, the return value indicates the existence of the current tool without actually retrieving the tool information.</span></span> <span data-ttu-id="23e8f-112">Se esse valor não for **nulo**, o membro **CbSize** da estrutura **TOOLINFO** deverá ser preenchido antes de enviar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="23e8f-112">If this value is not **NULL**, the **cbSize** member of the **TOOLINFO** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23e8f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23e8f-113">Return value</span></span>

<span data-ttu-id="23e8f-114">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="23e8f-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="23e8f-115">Se *lParam* for **nulo**, retornará um valor diferente de zero se existir uma ferramenta atual ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="23e8f-115">If *lParam* is **NULL**, returns nonzero if a current tool exists, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="23e8f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23e8f-116">Requirements</span></span>



| <span data-ttu-id="23e8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="23e8f-117">Requirement</span></span> | <span data-ttu-id="23e8f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="23e8f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23e8f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23e8f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="23e8f-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23e8f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23e8f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23e8f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="23e8f-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23e8f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23e8f-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23e8f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="23e8f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23e8f-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="23e8f-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="23e8f-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="23e8f-126">**TTM \_ GETCURRENTTOOLW** (Unicode) e **TTM \_ GETCURRENTTOOLA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="23e8f-126">**TTM\_GETCURRENTTOOLW** (Unicode) and **TTM\_GETCURRENTTOOLA** (ANSI)</span></span><br/>     |



 

 





