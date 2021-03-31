---
title: Mensagem de EM_CANREDO (RichEdit. h)
description: Determina se há alguma ação na fila de restauração do controle.
ms.assetid: 4a76adc8-f815-4cf7-8742-b7695e5a0f64
keywords:
- Controles de EM_CANREDO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CANREDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfb12f8e72bdf5321151cd3a70b74f322a46591
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824570"
---
# <a name="em_canredo-message"></a><span data-ttu-id="05a35-104">\_Mensagem em refazer</span><span class="sxs-lookup"><span data-stu-id="05a35-104">EM\_CANREDO message</span></span>

<span data-ttu-id="05a35-105">Determina se há alguma ação na fila de restauração do controle.</span><span class="sxs-lookup"><span data-stu-id="05a35-105">Determines whether there are any actions in the control redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="05a35-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05a35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a35-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="05a35-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05a35-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="05a35-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="05a35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="05a35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="05a35-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="05a35-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a35-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="05a35-111">Return value</span></span>

<span data-ttu-id="05a35-112">Se houver ações na fila de restauração do controle, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="05a35-112">If there are actions in the control redo queue, the return value is a nonzero value.</span></span>

<span data-ttu-id="05a35-113">Se a fila de restauração estiver vazia, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="05a35-113">If the redo queue is empty, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="05a35-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="05a35-114">Remarks</span></span>

<span data-ttu-id="05a35-115">Para refazer a operação de desfazer mais recente, envie a mensagem em [**\_ refazer**](em-redo.md) .</span><span class="sxs-lookup"><span data-stu-id="05a35-115">To redo the most recent undo operation, send the [**EM\_REDO**](em-redo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a35-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05a35-116">Requirements</span></span>



| <span data-ttu-id="05a35-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05a35-117">Requirement</span></span> | <span data-ttu-id="05a35-118">Valor</span><span class="sxs-lookup"><span data-stu-id="05a35-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05a35-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05a35-119">Minimum supported client</span></span><br/> | <span data-ttu-id="05a35-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05a35-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05a35-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05a35-121">Minimum supported server</span></span><br/> | <span data-ttu-id="05a35-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="05a35-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="05a35-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05a35-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a35-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a35-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05a35-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05a35-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="05a35-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="05a35-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="05a35-127">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="05a35-127">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="05a35-128">**em \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="05a35-128">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="05a35-129">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="05a35-129">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="05a35-130">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="05a35-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





