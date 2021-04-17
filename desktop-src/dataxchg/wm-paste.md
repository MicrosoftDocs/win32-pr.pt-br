---
title: Mensagem de WM_PASTE (WinUser. h)
description: Um aplicativo envia uma mensagem de colagem do WM \_ para um controle de edição ou caixa de combinação para copiar o conteúdo atual da área de transferência para o controle de edição na posição atual do cursor. Os dados só serão inseridos se a área de transferência contiver dados no formato de texto do CF \_ .
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Troca de dados de mensagem WM_PASTE
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369834"
---
# <a name="wm_paste-message"></a><span data-ttu-id="3a44f-105">Mensagem de colagem do WM \_</span><span class="sxs-lookup"><span data-stu-id="3a44f-105">WM\_PASTE message</span></span>

<span data-ttu-id="3a44f-106">Um aplicativo envia uma mensagem de **\_ colagem do WM** para um controle de edição ou caixa de combinação para copiar o conteúdo atual da área de transferência para o controle de edição na posição atual do cursor.</span><span class="sxs-lookup"><span data-stu-id="3a44f-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="3a44f-107">Os dados só serão inseridos se a área de transferência contiver dados no formato de [**\_ texto do CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="3a44f-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="3a44f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a44f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a44f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a44f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a44f-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3a44f-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a44f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a44f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a44f-112">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3a44f-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a44f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a44f-113">Return value</span></span>

<span data-ttu-id="3a44f-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3a44f-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a44f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a44f-115">Remarks</span></span>

<span data-ttu-id="3a44f-116">Quando enviado para uma caixa de combinação, a mensagem de **\_ colagem do WM** é tratada por seu controle de edição.</span><span class="sxs-lookup"><span data-stu-id="3a44f-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="3a44f-117">Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3a44f-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a44f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a44f-118">Requirements</span></span>



| <span data-ttu-id="3a44f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a44f-119">Requirement</span></span> | <span data-ttu-id="3a44f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3a44f-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a44f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a44f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a44f-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a44f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3a44f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a44f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a44f-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3a44f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3a44f-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3a44f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a44f-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a44f-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a44f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a44f-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a44f-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="3a44f-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a44f-129">**limpeza do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a44f-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="3a44f-130">**cópia do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a44f-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="3a44f-131">**recorte do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a44f-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="3a44f-132">**desfazer o WM \_**</span><span class="sxs-lookup"><span data-stu-id="3a44f-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="3a44f-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="3a44f-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3a44f-134">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="3a44f-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

