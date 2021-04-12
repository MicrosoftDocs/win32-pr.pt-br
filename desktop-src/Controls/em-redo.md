---
title: Mensagem de EM_REDO (RichEdit. h)
description: Envia uma \_ mensagem em em um controle de edição rico para refazer a próxima ação na fila de restauração do controle.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Controles de EM_REDO de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455441"
---
# <a name="em_redo-message"></a><span data-ttu-id="39e6b-104">\_Mensagem em restauração</span><span class="sxs-lookup"><span data-stu-id="39e6b-104">EM\_REDO message</span></span>

<span data-ttu-id="39e6b-105">Envia uma **mensagem \_ em em um controle** de edição rico para refazer a próxima ação na fila de restauração do controle.</span><span class="sxs-lookup"><span data-stu-id="39e6b-105">Sends an **EM\_REDO** message to a rich edit control to redo the next action in the control's redo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="39e6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39e6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39e6b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39e6b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39e6b-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="39e6b-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="39e6b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39e6b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39e6b-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="39e6b-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39e6b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="39e6b-111">Return value</span></span>

<span data-ttu-id="39e6b-112">Se a operação de **refazer** for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="39e6b-112">If the **Redo** operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="39e6b-113">Se a operação de **refazer** falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="39e6b-113">If the **Redo** operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="39e6b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="39e6b-114">Remarks</span></span>

<span data-ttu-id="39e6b-115">Para determinar se há alguma ação na fila de restauração do controle, envie a mensagem [**em \_ refazer**](em-canredo.md) .</span><span class="sxs-lookup"><span data-stu-id="39e6b-115">To determine whether there are any actions in the control's redo queue, send the [**EM\_CANREDO**](em-canredo.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="39e6b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39e6b-116">Requirements</span></span>



| <span data-ttu-id="39e6b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="39e6b-117">Requirement</span></span> | <span data-ttu-id="39e6b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="39e6b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39e6b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39e6b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="39e6b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39e6b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39e6b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39e6b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="39e6b-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39e6b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39e6b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39e6b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="39e6b-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="39e6b-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39e6b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="39e6b-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="39e6b-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="39e6b-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39e6b-127">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="39e6b-127">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="39e6b-128">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="39e6b-128">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="39e6b-129">**em \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="39e6b-129">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="39e6b-130">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="39e6b-130">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





