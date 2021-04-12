---
title: Mensagem de CB_INSERTSTRING (WinUser. h)
description: Insere uma cadeia de caracteres ou dados de item na lista de uma caixa de combinação. Ao contrário da \_ mensagem de ADDSTRING CB, a mensagem de inserção de CB não faz com \_ que uma lista com o \_ estilo de classificação CBS seja classificada.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- Controles de CB_INSERTSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d050980137bc34652cb2fce39b9f188f4d5cd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455124"
---
# <a name="cb_insertstring-message"></a><span data-ttu-id="932e6-105">Mensagem de inserção de CB \_</span><span class="sxs-lookup"><span data-stu-id="932e6-105">CB\_INSERTSTRING message</span></span>

<span data-ttu-id="932e6-106">Insere uma cadeia de caracteres ou dados de item na lista de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="932e6-106">Inserts a string or item data into the list of a combo box.</span></span> <span data-ttu-id="932e6-107">Ao contrário da mensagem de [**\_ AddString CB**](cb-addstring.md) , a mensagem de **\_ inserção de CB** não faz com que uma lista com o estilo de [**\_ classificação CBS**](combo-box-styles.md) seja classificada.</span><span class="sxs-lookup"><span data-stu-id="932e6-107">Unlike the [**CB\_ADDSTRING**](cb-addstring.md) message, the **CB\_INSERTSTRING** message does not cause a list with the [**CBS\_SORT**](combo-box-styles.md) style to be sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="932e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="932e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="932e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="932e6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="932e6-110">O índice de base zero da posição na qual inserir a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="932e6-110">The zero-based index of the position at which to insert the string.</span></span> <span data-ttu-id="932e6-111">Se esse parâmetro for-1, a cadeia de caracteres será adicionada ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="932e6-111">If this parameter is -1, the string is added to the end of the list.</span></span>

</dd> <dt>

<span data-ttu-id="932e6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="932e6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="932e6-113">Um ponteiro para a cadeia de caracteres terminada em nulo a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="932e6-113">A pointer to the null-terminated string to be inserted.</span></span> <span data-ttu-id="932e6-114">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o valor do parâmetro *lParam* será armazenado em vez da cadeia de caracteres para a qual ele apontaria de outra forma.</span><span class="sxs-lookup"><span data-stu-id="932e6-114">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored rather than the string to which it would otherwise point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="932e6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="932e6-115">Return value</span></span>

<span data-ttu-id="932e6-116">O valor de retorno é o índice da posição na qual a cadeia de caracteres foi inserida.</span><span class="sxs-lookup"><span data-stu-id="932e6-116">The return value is the index of the position at which the string was inserted.</span></span> <span data-ttu-id="932e6-117">Se ocorrer um erro, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="932e6-117">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="932e6-118">Se não houver espaço suficiente disponível para armazenar a nova cadeia de caracteres, ela será CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="932e6-118">If there is insufficient space available to store the new string, it is CB\_ERRSPACE.</span></span>

<span data-ttu-id="932e6-119">Se a caixa de combinação tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você inserir uma cadeia de caracteres maior que a caixa de combinação, deverá enviar uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.</span><span class="sxs-lookup"><span data-stu-id="932e6-119">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you insert a string wider than the combo box, you should send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

## <a name="requirements"></a><span data-ttu-id="932e6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="932e6-120">Requirements</span></span>



| <span data-ttu-id="932e6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="932e6-121">Requirement</span></span> | <span data-ttu-id="932e6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="932e6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="932e6-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="932e6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="932e6-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="932e6-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="932e6-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="932e6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="932e6-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="932e6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="932e6-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="932e6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="932e6-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="932e6-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="932e6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="932e6-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="932e6-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="932e6-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="932e6-131">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="932e6-131">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="932e6-132">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="932e6-132">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="932e6-133">**\_pasta CB**</span><span class="sxs-lookup"><span data-stu-id="932e6-133">**CB\_DIR**</span></span>](cb-dir.md)
</dt> </dl>

 

