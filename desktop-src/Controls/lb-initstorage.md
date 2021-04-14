---
title: Mensagem de LB_INITSTORAGE (WinUser. h)
description: Aloca memória para armazenar itens da caixa de listagem. Essa mensagem é usada antes que um aplicativo adicione um grande número de itens a uma caixa de listagem.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Controles de LB_INITSTORAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455179"
---
# <a name="lb_initstorage-message"></a><span data-ttu-id="5e01e-105">INITSTORAGE de mensagens de LB \_</span><span class="sxs-lookup"><span data-stu-id="5e01e-105">LB\_INITSTORAGE message</span></span>

<span data-ttu-id="5e01e-106">Aloca memória para armazenar itens da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="5e01e-106">Allocates memory for storing list box items.</span></span> <span data-ttu-id="5e01e-107">Essa mensagem é usada antes que um aplicativo adicione um grande número de itens a uma caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="5e01e-107">This message is used before an application adds a large number of items to a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e01e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e01e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e01e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e01e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e01e-110">O número de itens a serem adicionados.</span><span class="sxs-lookup"><span data-stu-id="5e01e-110">The number of items to add.</span></span>

<span data-ttu-id="5e01e-111">Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5e01e-111">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The *wParam* parameter is limited to 16-bit values.</span></span> <span data-ttu-id="5e01e-112">Isso significa que as caixas de listagem não podem conter mais de 32.767 itens.</span><span class="sxs-lookup"><span data-stu-id="5e01e-112">This means list boxes cannot contain more than 32,767 items.</span></span> <span data-ttu-id="5e01e-113">Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.</span><span class="sxs-lookup"><span data-stu-id="5e01e-113">Although the number of items is restricted, the total size in bytes of the items in a list box is limited only by available memory.</span></span>

</dd> <dt>

<span data-ttu-id="5e01e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e01e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e01e-115">A quantidade de memória, em bytes, a ser alocada para cadeias de caracteres de item.</span><span class="sxs-lookup"><span data-stu-id="5e01e-115">The amount of memory, in bytes, to allocate for item strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e01e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e01e-116">Return value</span></span>

<span data-ttu-id="5e01e-117">Se a mensagem for bem-sucedida, o valor de retorno será o número total de itens para os quais a memória foi alocada previamente, ou seja, o número total de itens adicionados por todas as mensagens **\_ INITSTORAGE de lb** bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="5e01e-117">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **LB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="5e01e-118">Se a mensagem falhar, o valor de retorno será LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="5e01e-118">If the message fails, the return value is LB\_ERRSPACE.</span></span>

<span data-ttu-id="5e01e-119">Microsoft Windows NT 4,0: esta mensagem não aloca a quantidade especificada de memória; no entanto, ele sempre retorna o valor especificado no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="5e01e-119">Microsoft Windows NT 4.0 : This message does not allocate the specified amount of memory; however, it always returns the value specified in the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e01e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e01e-120">Remarks</span></span>

<span data-ttu-id="5e01e-121">A **mensagem \_ INITSTORAGE de lb** ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100).</span><span class="sxs-lookup"><span data-stu-id="5e01e-121">The **LB\_INITSTORAGE** message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="5e01e-122">Ele reserva a quantidade especificada de memória para que as mensagens do [**lb \_ AddString**](lb-addstring.md), [**lb \_ InsertString**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)e [**lb \_ AddFile**](lb-addfile.md) tenham o menor tempo possível.</span><span class="sxs-lookup"><span data-stu-id="5e01e-122">It reserves the specified amount of memory so that subsequent [**LB\_ADDSTRING**](lb-addstring.md), [**LB\_INSERTSTRING**](lb-insertstring.md), [**LB\_DIR**](lb-dir.md), and [**LB\_ADDFILE**](lb-addfile.md) messages take the shortest possible time.</span></span> <span data-ttu-id="5e01e-123">Você pode usar estimativas para os parâmetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5e01e-123">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="5e01e-124">Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.</span><span class="sxs-lookup"><span data-stu-id="5e01e-124">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e01e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e01e-125">Requirements</span></span>



| <span data-ttu-id="5e01e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e01e-126">Requirement</span></span> | <span data-ttu-id="5e01e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="5e01e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e01e-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e01e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5e01e-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e01e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e01e-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e01e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5e01e-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e01e-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e01e-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e01e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e01e-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e01e-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e01e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e01e-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e01e-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="5e01e-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e01e-136">**o \_ ADDfile do lb**</span><span class="sxs-lookup"><span data-stu-id="5e01e-136">**LB\_ADDFILE**</span></span>](lb-addfile.md)
</dt> <dt>

[<span data-ttu-id="5e01e-137">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="5e01e-137">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="5e01e-138">**Dir. de LB \_**</span><span class="sxs-lookup"><span data-stu-id="5e01e-138">**LB\_DIR**</span></span>](lb-dir.md)
</dt> <dt>

[<span data-ttu-id="5e01e-139">**KG \_ InsertString**</span><span class="sxs-lookup"><span data-stu-id="5e01e-139">**LB\_INSERTSTRING**</span></span>](lb-insertstring.md)
</dt> </dl>

 

 





