---
title: Mensagem de CB_SETTOPINDEX (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETTOPINDEX para garantir que um item específico esteja visível na caixa de listagem de uma caixa de combinação.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_settopindex.htm
keywords:
- Controles de CB_SETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f402cbd16cd61a829a2221600bd3c548829f348
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644304"
---
# <a name="cb_settopindex-message"></a><span data-ttu-id="ae912-104">\_Mensagem de SETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="ae912-104">CB\_SETTOPINDEX message</span></span>

<span data-ttu-id="ae912-105">Um aplicativo envia a mensagem **CB \_ SETTOPINDEX** para garantir que um item específico esteja visível na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="ae912-105">An application sends the **CB\_SETTOPINDEX** message to ensure that a particular item is visible in the list box of a combo box.</span></span> <span data-ttu-id="ae912-106">O sistema rola o conteúdo da caixa de listagem para que o item especificado seja exibido na parte superior da caixa de listagem ou o intervalo máximo de rolagem tenha sido atingido.</span><span class="sxs-lookup"><span data-stu-id="ae912-106">The system scrolls the list box contents so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae912-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae912-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae912-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae912-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae912-109">Especifica o índice de base zero do item de lista.</span><span class="sxs-lookup"><span data-stu-id="ae912-109">Specifies the zero-based index of the list item.</span></span>

</dd> <dt>

<span data-ttu-id="ae912-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae912-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae912-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ae912-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae912-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae912-112">Return value</span></span>

<span data-ttu-id="ae912-113">Se a mensagem for bem-sucedida, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="ae912-113">If the message is successful, the return value is zero.</span></span>

<span data-ttu-id="ae912-114">Se a mensagem falhar, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="ae912-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae912-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae912-115">Requirements</span></span>



| <span data-ttu-id="ae912-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae912-116">Requirement</span></span> | <span data-ttu-id="ae912-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ae912-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae912-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae912-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae912-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae912-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae912-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae912-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae912-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae912-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae912-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae912-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae912-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae912-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae912-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae912-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae912-125">**\_GETTOPINDEX CB**</span><span class="sxs-lookup"><span data-stu-id="ae912-125">**CB\_GETTOPINDEX**</span></span>](cb-gettopindex.md)
</dt> </dl>

 

 





