---
title: Mensagem de CB_FINDSTRINGEXACT (WinUser. h)
description: Localiza a primeira cadeia de caracteres da caixa de listagem em uma caixa de combinação que corresponde à cadeia de caracteres especificada no parâmetro lParam.
ms.assetid: 9065af9f-b18e-4fd5-a8cc-f780f8d0fb05
keywords:
- Controles de CB_FINDSTRINGEXACT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f99d85c7dddb95bdfb168443d6f977c22273a87
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327171"
---
# <a name="cb_findstringexact-message"></a><span data-ttu-id="44d32-104">\_Mensagem de FINDSTRINGEXACT CB</span><span class="sxs-lookup"><span data-stu-id="44d32-104">CB\_FINDSTRINGEXACT message</span></span>

<span data-ttu-id="44d32-105">Localiza a primeira cadeia de caracteres da caixa de listagem em uma caixa de combinação que corresponde à cadeia de caracteres especificada no parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="44d32-105">Finds the first list box string in a combo box that matches the string specified in the *lParam* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="44d32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44d32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44d32-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="44d32-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44d32-108">O índice de base zero do item que antecede o primeiro item a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="44d32-108">The zero-based index of the item preceding the first item to be searched.</span></span> <span data-ttu-id="44d32-109">Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará na parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="44d32-109">When the search reaches the bottom of the list box, it continues from the top of the list box back to the item specified by the *wParam* parameter.</span></span> <span data-ttu-id="44d32-110">Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.</span><span class="sxs-lookup"><span data-stu-id="44d32-110">If *wParam* is -1, the entire list box is searched from the beginning.</span></span>

</dd> <dt>

<span data-ttu-id="44d32-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44d32-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44d32-112">Um ponteiro para a cadeia de caracteres terminada em nulo para pesquisa.</span><span class="sxs-lookup"><span data-stu-id="44d32-112">A pointer to the null-terminated string for which to search.</span></span> <span data-ttu-id="44d32-113">A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="44d32-113">The search is not case sensitive, so this string can contain any combination of uppercase and lowercase letters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44d32-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44d32-114">Return value</span></span>

<span data-ttu-id="44d32-115">O valor de retorno é o índice de base zero do item correspondente.</span><span class="sxs-lookup"><span data-stu-id="44d32-115">The return value is the zero-based index of the matching item.</span></span> <span data-ttu-id="44d32-116">Se a pesquisa não for bem-sucedida, será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="44d32-116">If the search is unsuccessful, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="44d32-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="44d32-117">Remarks</span></span>

<span data-ttu-id="44d32-118">Essa função será bem-sucedida somente se a cadeia de caracteres especificada e um item de caixa de combinação tiverem o mesmo comprimento (exceto para o caractere nulo de terminação) e os mesmos caracteres.</span><span class="sxs-lookup"><span data-stu-id="44d32-118">This function is successful only if the specified string and a combo box item have the same length (except for the terminating null character) and the same characters.</span></span>

<span data-ttu-id="44d32-119">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , a funcionalidade da mensagem **CB \_ FINDSTRINGEXACT** dependerá se o aplicativo usa o estilo de [**\_ classificação CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="44d32-119">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the functionality of **CB\_FINDSTRINGEXACT** message depends on whether your application uses the [**CBS\_SORT**](combo-box-styles.md) style.</span></span> <span data-ttu-id="44d32-120">Se você usar o estilo de **\_ classificação CBS** , as mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) serão enviadas ao proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada.</span><span class="sxs-lookup"><span data-stu-id="44d32-120">If you use the **CBS\_SORT** style, [**WM\_COMPAREITEM**](wm-compareitem.md) messages are sent to the owner of the combo box to determine which item matches the specified string.</span></span> <span data-ttu-id="44d32-121">Se você não usar o estilo **de \_ classificação CBS** , a mensagem **CB \_ FINDSTRINGEXACT** procurará um item de lista que corresponda ao valor do parâmetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="44d32-121">If you do not use the **CBS\_SORT** style, the **CB\_FINDSTRINGEXACT** message searches for a list item that matches the value of the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="44d32-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44d32-122">Requirements</span></span>



| <span data-ttu-id="44d32-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="44d32-123">Requirement</span></span> | <span data-ttu-id="44d32-124">Valor</span><span class="sxs-lookup"><span data-stu-id="44d32-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44d32-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44d32-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44d32-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44d32-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="44d32-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44d32-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44d32-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44d32-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="44d32-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44d32-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="44d32-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44d32-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44d32-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="44d32-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="44d32-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="44d32-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="44d32-133">**localização da CB \_**</span><span class="sxs-lookup"><span data-stu-id="44d32-133">**CB\_FINDSTRING**</span></span>](cb-findstring.md)
</dt> <dt>

[<span data-ttu-id="44d32-134">**seleção do CB \_**</span><span class="sxs-lookup"><span data-stu-id="44d32-134">**CB\_SELECTSTRING**</span></span>](cb-selectstring.md)
</dt> <dt>

[<span data-ttu-id="44d32-135">**COMPAREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="44d32-135">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

 





