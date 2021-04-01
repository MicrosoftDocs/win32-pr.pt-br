---
title: Mensagem de CB_GETITEMDATA (WinUser. h)
description: Um aplicativo envia uma \_ mensagem GETITEMDATA CB para uma caixa de combinação para recuperar o valor fornecido pelo aplicativo associado ao item especificado na caixa de combinação.
ms.assetid: 433b7f75-2831-4919-b931-c17ba651d145
keywords:
- Controles de CB_GETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643954cf266c52ccbeae082ffacf317c91bc7b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644638"
---
# <a name="cb_getitemdata-message"></a><span data-ttu-id="99a8d-104">\_Mensagem de GETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="99a8d-104">CB\_GETITEMDATA message</span></span>

<span data-ttu-id="99a8d-105">Um aplicativo envia uma **mensagem \_ GETITEMDATA CB** para uma caixa de combinação para recuperar o valor fornecido pelo aplicativo associado ao item especificado na caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="99a8d-105">An application sends a **CB\_GETITEMDATA** message to a combo box to retrieve the application-supplied value associated with the specified item in the combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="99a8d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99a8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99a8d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="99a8d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99a8d-108">O índice de base zero do item.</span><span class="sxs-lookup"><span data-stu-id="99a8d-108">The zero-based index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="99a8d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="99a8d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="99a8d-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="99a8d-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99a8d-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99a8d-111">Return value</span></span>

<span data-ttu-id="99a8d-112">O valor de retorno é o valor associado ao item.</span><span class="sxs-lookup"><span data-stu-id="99a8d-112">The return value is the value associated with the item.</span></span> <span data-ttu-id="99a8d-113">Se ocorrer um erro, será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="99a8d-113">If an error occurs, it is CB\_ERR.</span></span>

<span data-ttu-id="99a8d-114">Se o item estiver em uma caixa de combinação desenhada pelo proprietário criada sem o estilo [**\_ HASSTRINGS do CBS**](combo-box-styles.md) , o valor de retorno será o valor contido no parâmetro *lParam* da mensagem [**CB \_ AddString**](cb-addstring.md) ou [**CB \_ InsertString**](cb-insertstring.md) , que adicionou o item à caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="99a8d-114">If the item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the return value is the value contained in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message, that added the item to the combo box.</span></span> <span data-ttu-id="99a8d-115">Se o estilo **CBS \_ HASSTRINGS** não for usado, o valor de retorno será o parâmetro *lParam* contido em uma mensagem [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="99a8d-115">If the **CBS\_HASSTRINGS** style was not used, the return value is the *lParam* parameter contained in a [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a8d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99a8d-116">Requirements</span></span>



| <span data-ttu-id="99a8d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="99a8d-117">Requirement</span></span> | <span data-ttu-id="99a8d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="99a8d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99a8d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99a8d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="99a8d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="99a8d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="99a8d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99a8d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="99a8d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="99a8d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99a8d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99a8d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="99a8d-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99a8d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99a8d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="99a8d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="99a8d-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="99a8d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99a8d-127">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="99a8d-127">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="99a8d-128">**inserção de CB \_**</span><span class="sxs-lookup"><span data-stu-id="99a8d-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="99a8d-129">**\_SETITEMDATA CB**</span><span class="sxs-lookup"><span data-stu-id="99a8d-129">**CB\_SETITEMDATA**</span></span>](cb-setitemdata.md)
</dt> </dl>

 

 





