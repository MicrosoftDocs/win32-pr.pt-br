---
title: Mensagem de WM_DELETEITEM (WinUser. h)
description: Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou a caixa de combinação é destruída ou quando os itens são removidos pela \_ mensagem lb DeleteString, lb \_ RESETCONTENT, CB \_ excluirstring ou CB \_ RESETCONTENT.
ms.assetid: c3adf8fb-45f2-44f1-8821-6ffa7d76dc78
keywords:
- Controles de WM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_DELETEITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf37f8a367d23353903bd3cda85b573f6884ff2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455065"
---
# <a name="wm_deleteitem-message"></a><span data-ttu-id="da1be-104">Mensagem do WM \_ DELETEITEM</span><span class="sxs-lookup"><span data-stu-id="da1be-104">WM\_DELETEITEM message</span></span>

<span data-ttu-id="da1be-105">Enviado ao proprietário de uma caixa de listagem ou caixa de combinação quando a caixa de listagem ou a caixa de combinação é destruída ou quando os itens são removidos pela mensagem [**lb \_ DeleteString**](lb-deletestring.md), [**lb \_ RESETCONTENT**](lb-resetcontent.md), [**CB \_ excluirstring**](cb-deletestring.md)ou [**CB \_ RESETCONTENT**](cb-resetcontent.md) .</span><span class="sxs-lookup"><span data-stu-id="da1be-105">Sent to the owner of a list box or combo box when the list box or combo box is destroyed or when items are removed by the [**LB\_DELETESTRING**](lb-deletestring.md), [**LB\_RESETCONTENT**](lb-resetcontent.md), [**CB\_DELETESTRING**](cb-deletestring.md), or [**CB\_RESETCONTENT**](cb-resetcontent.md) message.</span></span> <span data-ttu-id="da1be-106">O sistema envia uma mensagem do **WM \_ DELETEITEM** para cada item excluído.</span><span class="sxs-lookup"><span data-stu-id="da1be-106">The system sends a **WM\_DELETEITEM** message for each deleted item.</span></span> <span data-ttu-id="da1be-107">O sistema envia a mensagem do **WM \_ DELETEITEM** para qualquer caixa de listagem ou item de caixa de combinação excluído com dados de item diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="da1be-107">The system sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>


```C++
WM_DELETEITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="da1be-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da1be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1be-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da1be-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da1be-110">Especifica o identificador do controle que enviou a mensagem **de \_ DELETEITEM do WM** .</span><span class="sxs-lookup"><span data-stu-id="da1be-110">Specifies the identifier of the control that sent the **WM\_DELETEITEM** message.</span></span>

</dd> <dt>

<span data-ttu-id="da1be-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da1be-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da1be-112">Ponteiro para uma estrutura [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) que contém informações sobre o item excluído de uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="da1be-112">Pointer to a [**DELETEITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-deleteitemstruct) structure that contains information about the item deleted from a list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1be-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da1be-113">Return value</span></span>

<span data-ttu-id="da1be-114">Um aplicativo deve retornar **true** se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="da1be-114">An application should return **TRUE** if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1be-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="da1be-115">Remarks</span></span>

<span data-ttu-id="da1be-116">Microsoft Windows NT e posterior: o Windows envia uma mensagem do **WM \_ DELETEITEM** somente para itens excluídos de uma caixa de listagem desenhada pelo proprietário (com o estilo [**lbs \_ OwnerDrawFixed**](list-box-styles.md) ou [**lbs \_ OwnerDrawVariable**](list-box-styles.md) ) ou a caixa de combinação desenhada pelo proprietário (com o estilo [**CBS \_ OwnerDrawFixed**](combo-box-styles.md) ou [**CBS \_ OwnerDrawVariable**](combo-box-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="da1be-116">Microsoft Windows NT and later: Windows sends a **WM\_DELETEITEM** message only for items deleted from an owner-drawn list box (with the [**LBS\_OWNERDRAWFIXED**](list-box-styles.md) or [**LBS\_OWNERDRAWVARIABLE**](list-box-styles.md) style) or owner-drawn combo box (with the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) or [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style).</span></span>

<span data-ttu-id="da1be-117">Windows 95: o Windows envia a mensagem do **WM \_ DELETEITEM** para qualquer caixa de listagem ou item de caixa de combinação excluído com dados de item diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="da1be-117">Windows 95: Windows sends the **WM\_DELETEITEM** message for any deleted list box or combo box item with nonzero item data.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1be-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da1be-118">Requirements</span></span>



| <span data-ttu-id="da1be-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="da1be-119">Requirement</span></span> | <span data-ttu-id="da1be-120">Valor</span><span class="sxs-lookup"><span data-stu-id="da1be-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da1be-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da1be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da1be-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da1be-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="da1be-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="da1be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da1be-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="da1be-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da1be-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="da1be-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="da1be-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da1be-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da1be-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="da1be-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="da1be-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="da1be-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da1be-129">**excluído de CB \_**</span><span class="sxs-lookup"><span data-stu-id="da1be-129">**CB\_DELETESTRING**</span></span>](cb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="da1be-130">**\_RESETCONTENT CB**</span><span class="sxs-lookup"><span data-stu-id="da1be-130">**CB\_RESETCONTENT**</span></span>](cb-resetcontent.md)
</dt> <dt>

[<span data-ttu-id="da1be-131">**DELETEITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="da1be-131">**DELETEITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-deleteitemstruct)
</dt> <dt>

[<span data-ttu-id="da1be-132">**LB \_ DeleteString**</span><span class="sxs-lookup"><span data-stu-id="da1be-132">**LB\_DELETESTRING**</span></span>](lb-deletestring.md)
</dt> <dt>

[<span data-ttu-id="da1be-133">**\_RESETCONTENT lb**</span><span class="sxs-lookup"><span data-stu-id="da1be-133">**LB\_RESETCONTENT**</span></span>](lb-resetcontent.md)
</dt> </dl>

 

 





