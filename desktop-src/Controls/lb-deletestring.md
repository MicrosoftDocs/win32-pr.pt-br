---
title: Mensagem de LB_DELETESTRING (WinUser. h)
description: Exclui uma cadeia de caracteres em uma caixa de listagem.
ms.assetid: 3f360e07-b70d-4bfc-89d4-18d3b18b0fcf
keywords:
- Controles de LB_DELETESTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 557256484ad5c5fa698d787144a37ff619b02ef2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824640"
---
# <a name="lb_deletestring-message"></a><span data-ttu-id="89983-104">LB \_ mensagem de exclusão</span><span class="sxs-lookup"><span data-stu-id="89983-104">LB\_DELETESTRING message</span></span>

<span data-ttu-id="89983-105">Exclui uma cadeia de caracteres em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="89983-105">Deletes a string in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="89983-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89983-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89983-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89983-108">O índice de base zero da cadeia de caracteres a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="89983-108">The zero-based index of the string to be deleted.</span></span>

<span data-ttu-id="89983-109">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="89983-109">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="89983-110">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="89983-110">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="89983-111">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="89983-111">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="89983-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89983-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="89983-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="89983-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89983-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89983-114">Return value</span></span>

<span data-ttu-id="89983-115">O valor de retorno é uma contagem das cadeias de caracteres restantes na lista.</span><span class="sxs-lookup"><span data-stu-id="89983-115">The return value is a count of the strings remaining in the list.</span></span> <span data-ttu-id="89983-116">O valor de retorno será LB \_ Err se o parâmetro *wParam* especificar um índice maior que o número de itens na lista.</span><span class="sxs-lookup"><span data-stu-id="89983-116">The return value is LB\_ERR if the *wParam* parameter specifies an index greater than the number of items in the list.</span></span>

## <a name="remarks"></a><span data-ttu-id="89983-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="89983-117">Remarks</span></span>

<span data-ttu-id="89983-118">Se um aplicativo criar a caixa de listagem com um estilo desenhado pelo proprietário, mas sem o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o sistema enviará uma mensagem do [**WM \_ DELETEITEM**](wm-deleteitem.md) para o proprietário da caixa de listagem para que o aplicativo possa liberar quaisquer dados adicionais associados ao item.</span><span class="sxs-lookup"><span data-stu-id="89983-118">If an application creates the list box with an owner-drawn style but without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, the system sends a [**WM\_DELETEITEM**](wm-deleteitem.md) message to the owner of the list box so the application can free any additional data associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="89983-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89983-119">Requirements</span></span>



| <span data-ttu-id="89983-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89983-120">Requirement</span></span> | <span data-ttu-id="89983-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89983-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89983-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89983-122">Minimum supported client</span></span><br/> | <span data-ttu-id="89983-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89983-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="89983-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89983-124">Minimum supported server</span></span><br/> | <span data-ttu-id="89983-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89983-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="89983-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89983-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="89983-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89983-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89983-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="89983-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="89983-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="89983-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="89983-130">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="89983-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="89983-131">**KG \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="89983-131">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="89983-132">**DELETEITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="89983-132">**WM\_DELETEITEM**</span></span>](wm-deleteitem.md)
</dt> </dl>

 

 





