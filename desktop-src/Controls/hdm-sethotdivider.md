---
title: Mensagem de HDM_SETHOTDIVIDER (commctrl. h)
description: Altera a cor de um divisor entre itens de cabeçalho para indicar o destino de uma operação de arrastar e soltar externa. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetHotDivider do cabeçalho.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- Controles de HDM_SETHOTDIVIDER de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085499"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="c0b63-105">\_Mensagem HDM SETHOTDIVIDER</span><span class="sxs-lookup"><span data-stu-id="c0b63-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="c0b63-106">Altera a cor de um divisor entre itens de cabeçalho para indicar o destino de uma operação de arrastar e soltar externa.</span><span class="sxs-lookup"><span data-stu-id="c0b63-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="c0b63-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetHotDivider do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) .</span><span class="sxs-lookup"><span data-stu-id="c0b63-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0b63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0b63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b63-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0b63-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b63-110">O tipo de valor representado por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c0b63-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="c0b63-111">Este valor pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="c0b63-111">This value can be one of the following:</span></span>



| <span data-ttu-id="c0b63-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c0b63-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="c0b63-113">Significado</span><span class="sxs-lookup"><span data-stu-id="c0b63-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="c0b63-114"><dt>VERDADEIRO \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c0b63-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="c0b63-115">Indica que *lParam* mantém as coordenadas do cliente do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="c0b63-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="c0b63-116"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c0b63-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="c0b63-117">Indica que *lParam* contém um valor de índice divisória.</span><span class="sxs-lookup"><span data-stu-id="c0b63-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="c0b63-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0b63-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c0b63-119">Um valor mantido em *lParam* é interpretado dependendo do valor de *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c0b63-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="c0b63-120">Se *wParam* for **true**, *lParam* representará as coordenadas x e y do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="c0b63-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="c0b63-121">A coordenada x está na palavra inferior e a coordenada y está na palavra alta.</span><span class="sxs-lookup"><span data-stu-id="c0b63-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="c0b63-122">Quando o controle de cabeçalho recebe a mensagem, ele realça o divisor apropriado com base nas coordenadas *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c0b63-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="c0b63-123">Se *wParam* for **false**, *lParam* representará o índice de inteiro do divisor a ser realçado.</span><span class="sxs-lookup"><span data-stu-id="c0b63-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b63-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0b63-124">Return value</span></span>

<span data-ttu-id="c0b63-125">Retorna um valor igual ao índice do divisor que o controle realçou.</span><span class="sxs-lookup"><span data-stu-id="c0b63-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0b63-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0b63-126">Remarks</span></span>

<span data-ttu-id="c0b63-127">Essa mensagem cria um efeito que um controle de cabeçalho produz automaticamente quando tem o estilo de [**\_ DRAGDROP da HDS**](header-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b63-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="c0b63-128">A mensagem **HDM \_ SETHOTDIVIDER** é destinada a ser usada quando o proprietário do controle manipula as operações de arrastar e soltar manualmente.</span><span class="sxs-lookup"><span data-stu-id="c0b63-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b63-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0b63-129">Requirements</span></span>



| <span data-ttu-id="c0b63-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0b63-130">Requirement</span></span> | <span data-ttu-id="c0b63-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c0b63-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b63-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0b63-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b63-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0b63-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0b63-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0b63-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b63-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0b63-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0b63-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0b63-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0b63-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0b63-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





