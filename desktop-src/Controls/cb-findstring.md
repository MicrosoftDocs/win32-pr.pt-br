---
title: Mensagem de CB_FINDSTRING (WinUser. h)
description: Pesquisa na caixa de listagem de uma caixa de combinação um item que começa com os caracteres em uma cadeia de caracteres especificada.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- Controles de CB_FINDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 295300790a27a956bce953e4e293c07c22ec0d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085539"
---
# <a name="cb_findstring-message"></a><span data-ttu-id="f19bc-104">Mensagem de localização do CB \_</span><span class="sxs-lookup"><span data-stu-id="f19bc-104">CB\_FINDSTRING message</span></span>

<span data-ttu-id="f19bc-105">Pesquisa na caixa de listagem de uma caixa de combinação um item que começa com os caracteres em uma cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="f19bc-105">Searches the list box of a combo box for an item beginning with the characters in a specified string.</span></span>

## <a name="parameters"></a><span data-ttu-id="f19bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f19bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19bc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f19bc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f19bc-108">O índice de base zero do item que antecede o primeiro item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="f19bc-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="f19bc-109">Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará na parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f19bc-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="f19bc-110">Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.</span><span class="sxs-lookup"><span data-stu-id="f19bc-110">If *wParam* is  -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="f19bc-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f19bc-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f19bc-112">Um ponteiro para a cadeia de caracteres terminada em nulo que contém os caracteres para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="f19bc-112">A pointer to the null-terminated string that contains the characters for which to search.</span></span> <span data-ttu-id="f19bc-113">A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f19bc-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19bc-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f19bc-114">Return value</span></span>

<span data-ttu-id="f19bc-115">O valor de retorno é o índice de base zero do item correspondente.</span><span class="sxs-lookup"><span data-stu-id="f19bc-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="f19bc-116">Se a pesquisa não for bem-sucedida, será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f19bc-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f19bc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f19bc-117">Remarks</span></span>

<span data-ttu-id="f19bc-118">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o que a mensagem de **\_ FindString do CB** dependerá se seu aplicativo usar o estilo de [**\_ classificação CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f19bc-118">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, what the **CB\_FINDSTRING** message does depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="f19bc-119">Se você usar o estilo de **\_ classificação CBS** , as mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) serão enviadas ao proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="f19bc-119">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="f19bc-120">Se você não usar o estilo **de \_ classificação CBS** , a mensagem de **\_ FindString CB** procurará um item de lista que corresponda ao valor do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f19bc-120">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRING** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f19bc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f19bc-121">Requirements</span></span>



| <span data-ttu-id="f19bc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f19bc-122">Requirement</span></span> | <span data-ttu-id="f19bc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f19bc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f19bc-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f19bc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f19bc-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f19bc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f19bc-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f19bc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f19bc-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f19bc-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f19bc-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f19bc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f19bc-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f19bc-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f19bc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="f19bc-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="f19bc-131">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f19bc-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f19bc-132">**\_FINDSTRINGEXACT CB**</span><span class="sxs-lookup"><span data-stu-id="f19bc-132">**CB\_FINDSTRINGEXACT**</span></span>](cb-findstringexact.md)
</dt> <dt>

[<span data-ttu-id="f19bc-133">**seleção do CB \_**</span><span class="sxs-lookup"><span data-stu-id="f19bc-133">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="f19bc-134">**CB \_ SETcurseal**</span><span class="sxs-lookup"><span data-stu-id="f19bc-134">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="f19bc-135">**COMPAREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f19bc-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





