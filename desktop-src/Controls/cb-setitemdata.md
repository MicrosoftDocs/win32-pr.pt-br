---
title: Mensagem de CB_SETITEMDATA (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETITEMDATA CB para definir o valor associado ao item especificado em uma caixa de combinação.
ms.assetid: 8be9eb57-a635-4c52-9838-556368813c74
keywords:
- Controles de CB_SETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbb1603f9906ebf30a391b57bd812dc2002136c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824572"
---
# <a name="cb_setitemdata-message"></a><span data-ttu-id="9bca9-104">\_Mensagem de SETITEMDATA CB</span><span class="sxs-lookup"><span data-stu-id="9bca9-104">CB\_SETITEMDATA message</span></span>

<span data-ttu-id="9bca9-105">Um aplicativo envia uma mensagem de **\_ SETITEMDATA CB** para definir o valor associado ao item especificado em uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="9bca9-105">An application sends a **CB\_SETITEMDATA** message to set the value associated with the specified item in a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="9bca9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bca9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bca9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bca9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bca9-108">Especifica o índice de base zero do item.</span><span class="sxs-lookup"><span data-stu-id="9bca9-108">Specifies the item's zero-based index.</span></span>

</dd> <dt>

<span data-ttu-id="9bca9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bca9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bca9-110">Especifica o novo valor a ser associado ao item.</span><span class="sxs-lookup"><span data-stu-id="9bca9-110">Specifies the new value to be associated with the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bca9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bca9-111">Return value</span></span>

<span data-ttu-id="9bca9-112">Se ocorrer um erro, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="9bca9-112">If an error occurs, the return value is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bca9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bca9-113">Remarks</span></span>

<span data-ttu-id="9bca9-114">Se o item especificado estiver em uma caixa de combinação desenhada pelo proprietário criada sem o estilo [**\_ HASSTRINGS do CBS**](combo-box-styles.md) , essa mensagem substituirá o valor no parâmetro *lParam* da mensagem [**CB \_ AddString**](cb-addstring.md) ou [**CB \_ InsertString**](cb-insertstring.md) que adicionou o item à caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="9bca9-114">If the specified item is in an owner-drawn combo box created without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, this message replaces the value in the *lParam* parameter of the [**CB\_ADDSTRING**](cb-addstring.md) or [**CB\_INSERTSTRING**](cb-insertstring.md) message that added the item to the combo box.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bca9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bca9-115">Requirements</span></span>



| <span data-ttu-id="9bca9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bca9-116">Requirement</span></span> | <span data-ttu-id="9bca9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9bca9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bca9-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bca9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9bca9-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9bca9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9bca9-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bca9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9bca9-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9bca9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9bca9-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bca9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bca9-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bca9-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bca9-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bca9-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="9bca9-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="9bca9-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9bca9-126">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="9bca9-126">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="9bca9-127">**\_GETITEMDATA CB**</span><span class="sxs-lookup"><span data-stu-id="9bca9-127">**CB\_GETITEMDATA**</span></span>](cb-getitemdata.md)
</dt> <dt>

[<span data-ttu-id="9bca9-128">**inserção de CB \_**</span><span class="sxs-lookup"><span data-stu-id="9bca9-128">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





