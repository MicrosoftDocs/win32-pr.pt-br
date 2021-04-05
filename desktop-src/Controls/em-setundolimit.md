---
title: Mensagem de EM_SETUNDOLIMIT (RichEdit. h)
description: Define o número máximo de ações que podem ser armazenadas na fila de desfazer de um controle de edição rico.
ms.assetid: 485dbcda-89f4-40de-ad55-cd524958e910
keywords:
- Controles de EM_SETUNDOLIMIT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETUNDOLIMIT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5b668d047f1de6d8720f09af5baf23e7cfc9cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918613"
---
# <a name="em_setundolimit-message"></a><span data-ttu-id="bcdb0-104">\_Mensagem em SETUNDOLIMIT</span><span class="sxs-lookup"><span data-stu-id="bcdb0-104">EM\_SETUNDOLIMIT message</span></span>

<span data-ttu-id="bcdb0-105">Define o número máximo de ações que podem ser armazenadas na fila de desfazer de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-105">Sets the maximum number of actions that can stored in the undo queue of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcdb0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcdb0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcdb0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcdb0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdb0-108">Especifica o número máximo de ações que podem ser armazenadas na fila de desfazer.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-108">Specifies the maximum number of actions that can be stored in the undo queue.</span></span>

</dd> <dt>

<span data-ttu-id="bcdb0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcdb0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcdb0-110">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-110">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcdb0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcdb0-111">Return value</span></span>

<span data-ttu-id="bcdb0-112">O valor de retorno é o novo número máximo de ações de desfazer para o controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-112">The return value is the new maximum number of undo actions for the rich edit control.</span></span> <span data-ttu-id="bcdb0-113">Esse valor pode ser menor que *wParam* se a memória for limitada.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-113">This value may be less than *wParam* if memory is limited.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcdb0-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcdb0-114">Remarks</span></span>

<span data-ttu-id="bcdb0-115">Por padrão, o número máximo de ações na fila de desfazer é de 100.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-115">By default, the maximum number of actions in the undo queue is 100.</span></span> <span data-ttu-id="bcdb0-116">Se você aumentar esse número, deverá haver memória suficiente disponível para acomodar o novo número.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-116">If you increase this number, there must be enough available memory to accommodate the new number.</span></span> <span data-ttu-id="bcdb0-117">Para obter um melhor desempenho, defina o limite para o menor valor possível.</span><span class="sxs-lookup"><span data-stu-id="bcdb0-117">For better performance, set the limit to the smallest possible value.</span></span>

<span data-ttu-id="bcdb0-118">Definir o limite como zero desabilita o recurso de **desfazer** .</span><span class="sxs-lookup"><span data-stu-id="bcdb0-118">Setting the limit to zero disables the **Undo** feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcdb0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcdb0-119">Requirements</span></span>



| <span data-ttu-id="bcdb0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcdb0-120">Requirement</span></span> | <span data-ttu-id="bcdb0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bcdb0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcdb0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcdb0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bcdb0-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcdb0-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcdb0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcdb0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bcdb0-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bcdb0-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcdb0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcdb0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcdb0-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcdb0-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcdb0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcdb0-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="bcdb0-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bcdb0-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bcdb0-130">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="bcdb0-130">**EM\_CANREDO**</span></span>](em-canredo.md)
</dt> <dt>

[<span data-ttu-id="bcdb0-131">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="bcdb0-131">**EM\_GETREDONAME**</span></span>](em-getredoname.md)
</dt> <dt>

[<span data-ttu-id="bcdb0-132">**em \_ GETundoname**</span><span class="sxs-lookup"><span data-stu-id="bcdb0-132">**EM\_GETUNDONAME**</span></span>](em-getundoname.md)
</dt> <dt>

[<span data-ttu-id="bcdb0-133">**em \_ refazer**</span><span class="sxs-lookup"><span data-stu-id="bcdb0-133">**EM\_REDO**</span></span>](em-redo.md)
</dt> <dt>

[<span data-ttu-id="bcdb0-134">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="bcdb0-134">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





