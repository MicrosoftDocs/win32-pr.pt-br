---
title: Mensagem de WM_COPY (WinUser. h)
description: Um aplicativo envia a mensagem de cópia do WM \_ para um controle de edição ou caixa de combinação para copiar a seleção atual para a área de transferência no formato de texto do CF \_ .
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Troca de dados de mensagem WM_COPY
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "105773004"
---
# <a name="wm_copy-message"></a><span data-ttu-id="95abe-104">Mensagem de cópia do WM \_</span><span class="sxs-lookup"><span data-stu-id="95abe-104">WM\_COPY message</span></span>

<span data-ttu-id="95abe-105">Um aplicativo envia a mensagem de **\_ cópia do WM** para um controle de edição ou caixa de combinação para copiar a seleção atual para a área de transferência no formato de [**\_ texto do CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="95abe-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="95abe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95abe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95abe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95abe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95abe-108">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95abe-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="95abe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95abe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95abe-110">Esse parâmetro não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95abe-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95abe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95abe-111">Return value</span></span>

<span data-ttu-id="95abe-112">Retorna um valor diferente de zero em caso de êxito, mais zero.</span><span class="sxs-lookup"><span data-stu-id="95abe-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="95abe-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="95abe-113">Remarks</span></span>

<span data-ttu-id="95abe-114">Quando enviado para uma caixa de combinação, a mensagem de **\_ cópia do WM** é manipulada por seu controle de edição.</span><span class="sxs-lookup"><span data-stu-id="95abe-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="95abe-115">Esta mensagem não tem nenhum efeito quando enviada para uma caixa de combinação com o estilo de [**CBS \_**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="95abe-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="95abe-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95abe-116">Requirements</span></span>



| <span data-ttu-id="95abe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="95abe-117">Requirement</span></span> | <span data-ttu-id="95abe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="95abe-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95abe-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95abe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="95abe-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95abe-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="95abe-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95abe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="95abe-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="95abe-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95abe-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="95abe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="95abe-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95abe-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95abe-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="95abe-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="95abe-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="95abe-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="95abe-127">**limpeza do WM \_**</span><span class="sxs-lookup"><span data-stu-id="95abe-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="95abe-128">**recorte do WM \_**</span><span class="sxs-lookup"><span data-stu-id="95abe-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="95abe-129">**colar do WM \_**</span><span class="sxs-lookup"><span data-stu-id="95abe-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="95abe-130">**desfazer o WM \_**</span><span class="sxs-lookup"><span data-stu-id="95abe-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="95abe-131">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="95abe-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="95abe-132">Área de transferência</span><span class="sxs-lookup"><span data-stu-id="95abe-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

