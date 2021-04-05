---
title: Mensagem de CB_ADDSTRING (WinUser. h)
description: Adiciona uma cadeia de caracteres à caixa de listagem de uma caixa de combinação. Se a caixa de combinação não tiver o \_ estilo de classificação CBS, a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Controles de CB_ADDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918990"
---
# <a name="cb_addstring-message"></a><span data-ttu-id="d3b0c-106">\_Mensagem ADDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="d3b0c-106">CB\_ADDSTRING message</span></span>

<span data-ttu-id="d3b0c-107">Adiciona uma cadeia de caracteres à caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-107">Adds a string to the list box of a combo box.</span></span> <span data-ttu-id="d3b0c-108">Se a caixa de combinação não tiver o estilo de [**\_ classificação CBS**](combo-box-styles.md) , a cadeia de caracteres será adicionada ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-108">If the combo box does not have the [**CBS\_SORT**](combo-box-styles.md) style, the string is added to the end of the list.</span></span> <span data-ttu-id="d3b0c-109">Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-109">Otherwise, the string is inserted into the list, and the list is sorted.</span></span>

## <a name="parameters"></a><span data-ttu-id="d3b0c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3b0c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3b0c-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3b0c-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b0c-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="d3b0c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3b0c-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3b0c-114">Um ponteiro **LPCTSTR** para a cadeia de caracteres terminada em nulo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-114">An **LPCTSTR** pointer to the null-terminated string to be added.</span></span> <span data-ttu-id="d3b0c-115">Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o valor do parâmetro *lParam* será armazenado como dados de item, e não a cadeia de caracteres que, de outra forma, apontaria para.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-115">If you create the combo box with an owner-drawn style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the value of the *lParam* parameter is stored as item data rather than the string it would otherwise point to.</span></span> <span data-ttu-id="d3b0c-116">Os dados do item podem ser recuperados ou modificados enviando a mensagem [**CB \_ GETITEMDATA**](cb-getitemdata.md) ou [**CB \_ SETITEMDATA**](cb-setitemdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d3b0c-116">The item data can be retrieved or modified by sending the [**CB\_GETITEMDATA**](cb-getitemdata.md) or [**CB\_SETITEMDATA**](cb-setitemdata.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3b0c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d3b0c-117">Return value</span></span>

<span data-ttu-id="d3b0c-118">O valor de retorno é o índice de base zero para a cadeia de caracteres na caixa de listagem da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-118">The return value is the zero-based index to the string in the list box of the combo box.</span></span> <span data-ttu-id="d3b0c-119">Se ocorrer um erro, o valor de retorno será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-119">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="d3b0c-120">Se o espaço insuficiente estiver disponível para armazenar a nova cadeia de caracteres, ele será CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-120">If insufficient space is available to store the new string, it is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b0c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3b0c-121">Remarks</span></span>

<span data-ttu-id="d3b0c-122">Se você criar uma caixa de combinação desenhada pelo proprietário com o estilo de [**\_ classificação CBS**](combo-box-styles.md) , mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , a mensagem do [**WM \_ COMPAREITEM**](wm-compareitem.md) será enviada uma ou mais vezes ao proprietário da caixa de combinação para que o novo item possa ser colocado corretamente na lista.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-122">If you create an owner-drawn combo box with the [**CBS\_SORT**](combo-box-styles.md) style but without the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the [**WM\_COMPAREITEM**](wm-compareitem.md) message is sent one or more times to the owner of the combo box so the new item can be properly placed in the list.</span></span>

<span data-ttu-id="d3b0c-123">Para inserir uma cadeia de caracteres em um local específico dentro da lista, use a mensagem de [**\_ inserção de CB**](cb-insertstring.md) .</span><span class="sxs-lookup"><span data-stu-id="d3b0c-123">To insert a string at a specific location within the list, use the [**CB\_INSERTSTRING**](cb-insertstring.md) message.</span></span>

<span data-ttu-id="d3b0c-124">Se a caixa de combinação tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você adicionar uma cadeia de caracteres mais larga do que a caixa de combinação, envie uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-124">If the combo box has [**WS\_HSCROLL**](/windows/desktop/winmsg/window-styles) style and you add a string wider than the combo box, send a [**LB\_SETHORIZONTALEXTENT**](lb-sethorizontalextent.md) message to ensure the horizontal scroll bar appears.</span></span>

<span data-ttu-id="d3b0c-125">**Comclt32.dll versão 5,0 ou posterior:** Se a configuração de [**\_ maiúsculas**](combo-box-styles.md) e [**\_ minúsculas**](combo-box-styles.md) do CBS for definida, a versão Unicode do **CB \_ AddString** alterará a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-125">**Comclt32.dll version 5.0 or later:** If [**CBS\_LOWERCASE**](combo-box-styles.md) or [**CBS\_UPPERCASE**](combo-box-styles.md) is set, the Unicode version of **CB\_ADDSTRING** alters the string.</span></span> <span data-ttu-id="d3b0c-126">Se estiver usando memória global somente leitura, isso fará com que o aplicativo falhe.</span><span class="sxs-lookup"><span data-stu-id="d3b0c-126">If using read-only global memory, this causes the application to fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b0c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3b0c-127">Requirements</span></span>



| <span data-ttu-id="d3b0c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3b0c-128">Requirement</span></span> | <span data-ttu-id="d3b0c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d3b0c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b0c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3b0c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b0c-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3b0c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3b0c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d3b0c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b0c-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3b0c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3b0c-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3b0c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3b0c-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b0c-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b0c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d3b0c-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3b0c-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="d3b0c-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3b0c-138">**\_pasta CB**</span><span class="sxs-lookup"><span data-stu-id="d3b0c-138">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="d3b0c-139">**inserção de CB \_**</span><span class="sxs-lookup"><span data-stu-id="d3b0c-139">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="d3b0c-140">**\_SETHORIZONTALEXTENT lb**</span><span class="sxs-lookup"><span data-stu-id="d3b0c-140">**LB\_SETHORIZONTALEXTENT**</span></span>](lb-sethorizontalextent.md)
</dt> <dt>

[<span data-ttu-id="d3b0c-141">**COMPAREITEM do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d3b0c-141">**WM\_COMPAREITEM**</span></span>](wm-compareitem.md)
</dt> </dl>

 

