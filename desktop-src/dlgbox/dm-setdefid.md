---
title: Mensagem de DM_SETDEFID (WinUser. h)
description: Altera o identificador do botão de ação padrão de uma caixa de diálogo.
ms.assetid: 30720fa1-48cb-42d4-8370-87bdbaa34600
keywords:
- Caixas de diálogo de DM_SETDEFID mensagem
topic_type:
- apiref
api_name:
- DM_SETDEFID
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ceda9ac9e8fd399604e9c55431b8fcd74646f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499741"
---
# <a name="dm_setdefid-message"></a><span data-ttu-id="15172-104">\_Mensagem DM SETDEFID</span><span class="sxs-lookup"><span data-stu-id="15172-104">DM\_SETDEFID message</span></span>

<span data-ttu-id="15172-105">Altera o identificador do botão de ação padrão de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="15172-105">Changes the identifier of the default push button for a dialog box.</span></span>


```C++
#define WM_USER              0x0400
#define DM_SETDEFID         (WM_USER+1)
```



## <a name="parameters"></a><span data-ttu-id="15172-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15172-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15172-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="15172-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15172-108">O identificador de um controle de botão de ação que se tornará o padrão.</span><span class="sxs-lookup"><span data-stu-id="15172-108">The identifier of a push button control that will become the default.</span></span>

</dd> <dt>

<span data-ttu-id="15172-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15172-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15172-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="15172-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15172-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15172-111">Return value</span></span>

<span data-ttu-id="15172-112">O valor de retorno é sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="15172-112">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="15172-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="15172-113">Remarks</span></span>

<span data-ttu-id="15172-114">Essa mensagem é processada pela função [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) .</span><span class="sxs-lookup"><span data-stu-id="15172-114">This message is processed by the [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) function.</span></span> <span data-ttu-id="15172-115">Para definir o botão de ação padrão, a função pode enviar mensagens do [**WM \_ GETDLGCODE**](wm-getdlgcode.md) e do [**BM \_ SetStyle**](../controls/bm-setstyle.md) para o controle especificado e o botão de push padrão atual.</span><span class="sxs-lookup"><span data-stu-id="15172-115">To set the default push button, the function can send [**WM\_GETDLGCODE**](wm-getdlgcode.md) and [**BM\_SETSTYLE**](../controls/bm-setstyle.md) messages to the specified control and the current default push button.</span></span>

<span data-ttu-id="15172-116">O uso da mensagem **DM \_ SETDEFID** pode fazer com que mais de um botão pareça ter o estado padrão do botão de ação.</span><span class="sxs-lookup"><span data-stu-id="15172-116">Using the **DM\_SETDEFID** message can result in more than one button appearing to have the default push button state.</span></span> <span data-ttu-id="15172-117">Quando o sistema abre uma caixa de diálogo, ele desenha o primeiro botão de ação no modelo de caixa de diálogo com a borda de estado padrão.</span><span class="sxs-lookup"><span data-stu-id="15172-117">When the system brings up a dialog, it draws the first push button in the dialog template with the default state border.</span></span> <span data-ttu-id="15172-118">O envio de uma mensagem **DM \_ SETDEFID** para alterar o botão padrão nem sempre removerá a borda do estado padrão do primeiro botão de ação.</span><span class="sxs-lookup"><span data-stu-id="15172-118">Sending a **DM\_SETDEFID** message to change the default button will not always remove the default state border from the first push button.</span></span> <span data-ttu-id="15172-119">Nesses casos, o aplicativo deve enviar uma mensagem [**\_ SetStyle BM**](../controls/bm-setstyle.md) para alterar o primeiro estilo de borda do botão de ação.</span><span class="sxs-lookup"><span data-stu-id="15172-119">In these cases, the application should send a [**BM\_SETSTYLE**](../controls/bm-setstyle.md) message to change the first push button border style.</span></span>

## <a name="requirements"></a><span data-ttu-id="15172-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15172-120">Requirements</span></span>



| <span data-ttu-id="15172-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="15172-121">Requirement</span></span> | <span data-ttu-id="15172-122">Valor</span><span class="sxs-lookup"><span data-stu-id="15172-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15172-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15172-123">Minimum supported client</span></span><br/> | <span data-ttu-id="15172-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15172-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="15172-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15172-125">Minimum supported server</span></span><br/> | <span data-ttu-id="15172-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="15172-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="15172-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="15172-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="15172-128"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15172-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15172-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="15172-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="15172-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="15172-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="15172-131">**DefDlgProc**</span><span class="sxs-lookup"><span data-stu-id="15172-131">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
</dt> <dt>

[<span data-ttu-id="15172-132">**\_GETDEFID DM**</span><span class="sxs-lookup"><span data-stu-id="15172-132">**DM\_GETDEFID**</span></span>](dm-getdefid.md)
</dt> <dt>

[<span data-ttu-id="15172-133">**GETDLGCODE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="15172-133">**WM\_GETDLGCODE**</span></span>](wm-getdlgcode.md)
</dt> <dt>

<span data-ttu-id="15172-134">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="15172-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15172-135">Caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="15172-135">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="15172-136">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="15172-136">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="15172-137">**SetStyle BM \_**</span><span class="sxs-lookup"><span data-stu-id="15172-137">**BM\_SETSTYLE**</span></span>](../controls/bm-setstyle.md)
</dt> <dt>

[<span data-ttu-id="15172-138">**em \_ SETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="15172-138">**EM\_SETLIMITTEXT**</span></span>](../controls/em-setlimittext.md)
</dt> </dl>

 

