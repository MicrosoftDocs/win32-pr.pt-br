---
title: Mensagem de PGM_GETBUTTONSIZE (commctrl. h)
description: Recupera o tamanho do botão atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro getbuttons do pager.
ms.assetid: fa8b4814-4587-4149-83a7-84faad2a4641
keywords:
- Controles de PGM_GETBUTTONSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae5cb36d203aaeae748db9adb1b13cacf2e40f5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009557"
---
# <a name="pgm_getbuttonsize-message"></a><span data-ttu-id="4b8c6-105">\_Mensagem de GETbuttons do PGM</span><span class="sxs-lookup"><span data-stu-id="4b8c6-105">PGM\_GETBUTTONSIZE message</span></span>

<span data-ttu-id="4b8c6-106">Recupera o tamanho do botão atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="4b8c6-106">Retrieves the current button size for the pager control.</span></span> <span data-ttu-id="4b8c6-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getbuttons do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) .</span><span class="sxs-lookup"><span data-stu-id="4b8c6-107">You can send this message explicitly or use the [**Pager\_GetButtonSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4b8c6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b8c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b8c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4b8c6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4b8c6-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4b8c6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4b8c6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4b8c6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4b8c6-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4b8c6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b8c6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b8c6-113">Return value</span></span>

<span data-ttu-id="4b8c6-114">Retorna um valor INT que contém o tamanho do botão atual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="4b8c6-114">Returns an INT value that contains the current button size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8c6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b8c6-115">Requirements</span></span>



| <span data-ttu-id="4b8c6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8c6-116">Requirement</span></span> | <span data-ttu-id="4b8c6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4b8c6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8c6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b8c6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8c6-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b8c6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4b8c6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b8c6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8c6-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b8c6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b8c6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b8c6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b8c6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b8c6-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b8c6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b8c6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8c6-125">**SetButtons do PGM \_**</span><span class="sxs-lookup"><span data-stu-id="4b8c6-125">**PGM\_SETBUTTONSIZE**</span></span>](pgm-setbuttonsize.md)
</dt> </dl>

 

 





