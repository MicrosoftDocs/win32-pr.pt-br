---
title: Mensagem de CB_GETTOPINDEX (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB GETTOPINDEX para recuperar o índice de base zero do primeiro item visível na parte da caixa de listagem de uma caixa de combinação.
ms.assetid: vs|controls|~\controls\comboboxes\comboboxreference\comboboxmessages\cb_gettopindex.htm
keywords:
- Controles de CB_GETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59d5d6834dd954261822c8b1cb1a449d16398284
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918433"
---
# <a name="cb_gettopindex-message"></a><span data-ttu-id="6fcdc-104">\_Mensagem de GETTOPINDEX CB</span><span class="sxs-lookup"><span data-stu-id="6fcdc-104">CB\_GETTOPINDEX message</span></span>

<span data-ttu-id="6fcdc-105">Um aplicativo envia a mensagem **CB \_ GETTOPINDEX** para recuperar o índice de base zero do primeiro item visível na parte da caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="6fcdc-105">An application sends the **CB\_GETTOPINDEX** message to retrieve the zero-based index of the first visible item in the list box portion of a combo box.</span></span> <span data-ttu-id="6fcdc-106">Inicialmente, o item com o índice 0 está na parte superior da caixa de listagem, mas se o conteúdo da caixa de listagem tiver sido rolado, outro item poderá estar na parte superior.</span><span class="sxs-lookup"><span data-stu-id="6fcdc-106">Initially, the item with index 0 is at the top of the list box, but if the list box contents have been scrolled, another item may be at the top.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fcdc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fcdc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fcdc-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fcdc-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fcdc-109">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6fcdc-109">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6fcdc-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fcdc-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fcdc-111">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6fcdc-111">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fcdc-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fcdc-112">Return value</span></span>

<span data-ttu-id="6fcdc-113">Se a mensagem for bem-sucedida, o valor de retorno será o índice do primeiro item visível na caixa de listagem da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="6fcdc-113">If the message is successful, the return value is the index of the first visible item in the list box of the combo box.</span></span>

<span data-ttu-id="6fcdc-114">Se a mensagem falhar, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="6fcdc-114">If the message fails, the return value is CB\_ERR.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcdc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fcdc-115">Requirements</span></span>



| <span data-ttu-id="6fcdc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcdc-116">Requirement</span></span> | <span data-ttu-id="6fcdc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6fcdc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcdc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fcdc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcdc-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fcdc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6fcdc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fcdc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcdc-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fcdc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fcdc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fcdc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fcdc-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fcdc-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fcdc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fcdc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fcdc-125">**\_SETTOPINDEX CB**</span><span class="sxs-lookup"><span data-stu-id="6fcdc-125">**CB\_SETTOPINDEX**</span></span>](cb-settopindex.md)
</dt> </dl>

 

 





