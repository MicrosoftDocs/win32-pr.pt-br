---
title: Mensagem de TB_GETINSERTMARK (commctrl. h)
description: Recupera a marca de inserção atual para a barra de ferramentas.
ms.assetid: b22770a4-e859-451d-a726-279bbc49b984
keywords:
- Controles de TB_GETINSERTMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b45a4cafbd49c709e9ca5b8e9afeda51323de491
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008992"
---
# <a name="tb_getinsertmark-message"></a><span data-ttu-id="f5ce2-104">TB de \_ mensagem GETINSERTMARK</span><span class="sxs-lookup"><span data-stu-id="f5ce2-104">TB\_GETINSERTMARK message</span></span>

<span data-ttu-id="f5ce2-105">Recupera a marca de inserção atual para a barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-105">Retrieves the current insertion mark for the toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5ce2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5ce2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ce2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5ce2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f5ce2-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f5ce2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5ce2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ce2-110">Ponteiro para uma estrutura [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) que recebe a marca de inserção.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-110">Pointer to a [**TBINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-tbinsertmark) structure that receives the insertion mark.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ce2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5ce2-111">Return value</span></span>

<span data-ttu-id="f5ce2-112">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="f5ce2-112">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ce2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5ce2-113">Requirements</span></span>



| <span data-ttu-id="f5ce2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ce2-114">Requirement</span></span> | <span data-ttu-id="f5ce2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f5ce2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ce2-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ce2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ce2-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5ce2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5ce2-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5ce2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ce2-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f5ce2-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5ce2-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5ce2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ce2-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ce2-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ce2-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5ce2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ce2-123">**TB de \_ SETINSERTMARK**</span><span class="sxs-lookup"><span data-stu-id="f5ce2-123">**TB\_SETINSERTMARK**</span></span>](tb-setinsertmark.md)
</dt> </dl>

 

 





