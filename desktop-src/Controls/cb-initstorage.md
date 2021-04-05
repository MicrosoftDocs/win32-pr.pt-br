---
title: Mensagem de CB_INITSTORAGE (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB INITSTORAGE antes de adicionar um grande número de itens à parte da caixa de listagem de uma caixa de combinação. Essa mensagem aloca memória para armazenar itens da caixa de listagem.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- Controles de CB_INITSTORAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085537"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="30a42-105">\_Mensagem de INITSTORAGE CB</span><span class="sxs-lookup"><span data-stu-id="30a42-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="30a42-106">Um aplicativo envia a mensagem **CB \_ INITSTORAGE** antes de adicionar um grande número de itens à parte da caixa de listagem de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="30a42-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="30a42-107">Essa mensagem aloca memória para armazenar itens da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="30a42-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="30a42-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30a42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a42-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30a42-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30a42-110">O número de itens a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="30a42-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="30a42-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30a42-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="30a42-112">A quantidade de memória a ser alocada para cadeias de caracteres de item, em bytes.</span><span class="sxs-lookup"><span data-stu-id="30a42-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a42-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30a42-113">Return value</span></span>

<span data-ttu-id="30a42-114">Se a mensagem for bem-sucedida, o valor de retorno será o número total de itens para os quais a memória foi alocada previamente, ou seja, o número total de itens adicionados por todas as mensagens do **CB \_ INITSTORAGE** bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="30a42-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="30a42-115">Se a mensagem falhar, o valor de retorno será CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="30a42-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="30a42-116">A mensagem aloca memória e retorna os valores de êxito e erro descritos acima.</span><span class="sxs-lookup"><span data-stu-id="30a42-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a42-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="30a42-117">Remarks</span></span>

<span data-ttu-id="30a42-118">A mensagem **CB \_ INITSTORAGE** ajuda a acelerar a inicialização de caixas de combinação que têm um grande número de itens (mais de 100).</span><span class="sxs-lookup"><span data-stu-id="30a42-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="30a42-119">Ele reserva a quantidade especificada de memória para que as mensagens de [**\_ dir**](cb-dir.md) subsequentes [**CB \_**](cb-addstring.md), [**CB \_ InsertString**](cb-insertstring.md)e CB tenham o menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="30a42-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="30a42-120">Você pode usar estimativas para os parâmetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="30a42-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="30a42-121">Se você superestimar, a memória extra é alocada, se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="30a42-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a42-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30a42-122">Requirements</span></span>



| <span data-ttu-id="30a42-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="30a42-123">Requirement</span></span> | <span data-ttu-id="30a42-124">Valor</span><span class="sxs-lookup"><span data-stu-id="30a42-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a42-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30a42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="30a42-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="30a42-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="30a42-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30a42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="30a42-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="30a42-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="30a42-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30a42-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="30a42-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30a42-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a42-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="30a42-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="30a42-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="30a42-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="30a42-133">**AddString CB \_**</span><span class="sxs-lookup"><span data-stu-id="30a42-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="30a42-134">**\_pasta CB**</span><span class="sxs-lookup"><span data-stu-id="30a42-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="30a42-135">**inserção de CB \_**</span><span class="sxs-lookup"><span data-stu-id="30a42-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





