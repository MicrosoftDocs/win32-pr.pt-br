---
title: Mensagem de WM_CUT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de recorte do WM para um controle de edição ou caixa de combinação para excluir (recortar) a seleção atual, se houver, no controle de edição e copiar o texto excluído para a área de transferência no \_ formato de texto cf.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- Troca de dados de mensagem WM_CUT
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754237"
---
# <a name="wm_cut-message"></a><span data-ttu-id="a9d5b-104">\_Mensagem de recorte do WM</span><span class="sxs-lookup"><span data-stu-id="a9d5b-104">WM\_CUT message</span></span>

<span data-ttu-id="a9d5b-105">Um aplicativo envia uma mensagem de **\_ recorte do WM** para um controle de edição ou caixa de combinação para excluir (recortar) a seleção atual, se houver, no controle de edição e copiar o texto excluído para a área de transferência no formato de [**\_ texto CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d5b-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="a9d5b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9d5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9d5b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9d5b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d5b-108">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a9d5b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9d5b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9d5b-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9d5b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9d5b-111">Return value</span></span>

<span data-ttu-id="a9d5b-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9d5b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9d5b-113">Remarks</span></span>

<span data-ttu-id="a9d5b-114">A exclusão realizada pela mensagem **de \_ recorte do WM** pode ser desfeita enviando o controle de edição uma mensagem em [**\_ desfazer**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d5b-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="a9d5b-115">Para excluir a seleção atual sem colocar o texto excluído na área de transferência, use a mensagem de [**\_ limpeza do WM**](wm-clear.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d5b-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="a9d5b-116">Quando enviado para uma caixa de combinação, a mensagem de **\_ recorte do WM** é tratada por seu controle de edição.</span><span class="sxs-lookup"><span data-stu-id="a9d5b-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="a9d5b-117">Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a9d5b-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d5b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9d5b-118">Requirements</span></span>



| <span data-ttu-id="a9d5b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d5b-119">Requirement</span></span> | <span data-ttu-id="a9d5b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a9d5b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d5b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9d5b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d5b-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a9d5b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a9d5b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9d5b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d5b-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a9d5b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9d5b-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a9d5b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d5b-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9d5b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d5b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9d5b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a9d5b-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a9d5b-129">**limpeza do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="a9d5b-130">**cópia do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="a9d5b-131">**colar do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="a9d5b-132">**desfazer o WM \_**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="a9d5b-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a9d5b-134">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="a9d5b-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="a9d5b-135">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a9d5b-136">**em \_ desfazer**</span><span class="sxs-lookup"><span data-stu-id="a9d5b-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

