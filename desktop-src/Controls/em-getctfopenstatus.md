---
title: Mensagem de EM_GETCTFOPENSTATUS (RichEdit. h)
description: Determina se o teclado da estrutura de serviços de texto (TSF) está aberto ou fechado.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- Controles de EM_GETCTFOPENSTATUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918562"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="067ae-104">\_Mensagem em GETCTFOPENSTATUS</span><span class="sxs-lookup"><span data-stu-id="067ae-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="067ae-105">Determina se o teclado da estrutura de serviços de texto (TSF) está aberto ou fechado.</span><span class="sxs-lookup"><span data-stu-id="067ae-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="067ae-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="067ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="067ae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="067ae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="067ae-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="067ae-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="067ae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="067ae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="067ae-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="067ae-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="067ae-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="067ae-111">Return value</span></span>

<span data-ttu-id="067ae-112">Se o teclado TSF estiver aberto, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="067ae-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="067ae-113">Caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="067ae-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="067ae-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="067ae-114">Requirements</span></span>



| <span data-ttu-id="067ae-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="067ae-115">Requirement</span></span> | <span data-ttu-id="067ae-116">Valor</span><span class="sxs-lookup"><span data-stu-id="067ae-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="067ae-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="067ae-117">Minimum supported client</span></span><br/> | <span data-ttu-id="067ae-118">\[Somente aplicativos da área de trabalho do Windows XP com SP1\]</span><span class="sxs-lookup"><span data-stu-id="067ae-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="067ae-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="067ae-119">Minimum supported server</span></span><br/> | <span data-ttu-id="067ae-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="067ae-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="067ae-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="067ae-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="067ae-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="067ae-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="067ae-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="067ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067ae-124">**em \_ SETCTFOPENSTATUS**</span><span class="sxs-lookup"><span data-stu-id="067ae-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





