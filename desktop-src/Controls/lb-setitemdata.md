---
title: Mensagem de LB_SETITEMDATA (WinUser. h)
description: Define um valor associado ao item especificado em uma caixa de listagem.
ms.assetid: df974fa2-114a-43ef-b0ac-0451c31d95cd
keywords:
- Controles de LB_SETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d9f9cc952ea3bf2d83358ce3b15ce6c3a2546b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086173"
---
# <a name="lb_setitemdata-message"></a><span data-ttu-id="b99b4-104">SETITEMDATA de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="b99b4-104">LB\_SETITEMDATA message</span></span>

<span data-ttu-id="b99b4-105">Define um valor associado ao item especificado em uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="b99b4-105">Sets a value associated with the specified item in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b99b4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b99b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b99b4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b99b4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b99b4-108">Especifica o índice de base zero do item.</span><span class="sxs-lookup"><span data-stu-id="b99b4-108">Specifies the zero-based index of the item.</span></span> <span data-ttu-id="b99b4-109">Se esse valor for-1, o valor de *lParam* se aplicará a todos os itens na caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="b99b4-109">If this value is -1, the *lParam* value applies to all items in the list box.</span></span>

<span data-ttu-id="b99b4-110">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="b99b4-110">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="b99b4-111">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="b99b4-111">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="b99b4-112">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="b99b4-112">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="b99b4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b99b4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b99b4-114">Especifica o valor a ser associado ao item.</span><span class="sxs-lookup"><span data-stu-id="b99b4-114">Specifies the value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b99b4-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b99b4-115">Return value</span></span>

<span data-ttu-id="b99b4-116">Se ocorrer um erro, o valor de retorno será um erro de LB \_ .</span><span class="sxs-lookup"><span data-stu-id="b99b4-116">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b99b4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b99b4-117">Remarks</span></span>

<span data-ttu-id="b99b4-118">Se o item estiver em uma caixa de listagem desenhada pelo proprietário criada sem o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , essa mensagem substituirá o valor contido no parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lb \_ InsertString**](lb-insertstring.md) que adicionou o item à caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="b99b4-118">If the item is in an owner-drawn list box created without the [**LBS\_HASSTRINGS**](list-box-styles.md) style, this message replaces the value contained in the *lParam* parameter of the [**LB\_ADDSTRING**](lb-addstring.md) or [**LB\_INSERTSTRING**](lb-insertstring.md) message that added the item to the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="b99b4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b99b4-119">Requirements</span></span>



| <span data-ttu-id="b99b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b99b4-120">Requirement</span></span> | <span data-ttu-id="b99b4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b99b4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b99b4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b99b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b99b4-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b99b4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b99b4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b99b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b99b4-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b99b4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b99b4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b99b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b99b4-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b99b4-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b99b4-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b99b4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b99b4-129">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b99b4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b99b4-130">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="b99b4-130">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="b99b4-131">**\_GETITEMDATA lb**</span><span class="sxs-lookup"><span data-stu-id="b99b4-131">**LB\_GETITEMDATA**</span></span>](lb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="b99b4-132">**KG \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="b99b4-132">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





