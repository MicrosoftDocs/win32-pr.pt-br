---
title: Mensagem de CB_DELETESTRING (WinUser. h)
description: Exclui uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- Controles de CB_DELETESTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb0d3900c86874db1113c219fd9f7967c5f6bb6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086330"
---
# <a name="cb_deletestring-message"></a><span data-ttu-id="db9da-104">\_Mensagem excluída CB</span><span class="sxs-lookup"><span data-stu-id="db9da-104">CB\_DELETESTRING message</span></span>

<span data-ttu-id="db9da-105">Exclui uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="db9da-105">Deletes a string in the list box of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="db9da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db9da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="db9da-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db9da-108">O índice de base zero da cadeia de caracteres a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="db9da-108">The zero-based index of the string to delete.</span></span>

</dd> <dt>

<span data-ttu-id="db9da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db9da-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db9da-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="db9da-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9da-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="db9da-111">Return value</span></span>

<span data-ttu-id="db9da-112">O valor de retorno é uma contagem das cadeias de caracteres restantes na lista.</span><span class="sxs-lookup"><span data-stu-id="db9da-112">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="db9da-113">Se o parâmetro *wParam* especificar um índice maior que o número de itens na lista, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="db9da-113">If the *wParam* parameter specifies an index greater than the number of items in the list, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9da-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="db9da-114">Remarks</span></span>

<span data-ttu-id="db9da-115">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o sistema enviará uma mensagem do [**WM \_ DELETEITEM**](wm-deleteitem.md) para o proprietário da caixa de combinação para que o aplicativo possa liberar quaisquer dados adicionais associados ao item.</span><span class="sxs-lookup"><span data-stu-id="db9da-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the combo box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db9da-116">Requirements</span></span>



| <span data-ttu-id="db9da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="db9da-117">Requirement</span></span> | <span data-ttu-id="db9da-118">Valor</span><span class="sxs-lookup"><span data-stu-id="db9da-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9da-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db9da-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db9da-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db9da-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="db9da-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db9da-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db9da-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db9da-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="db9da-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db9da-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9da-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db9da-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db9da-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="db9da-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="db9da-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="db9da-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="db9da-127">**\_RESETCONTENT CB**</span><span class="sxs-lookup"><span data-stu-id="db9da-127">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="db9da-128">**DELETEITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="db9da-128">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





