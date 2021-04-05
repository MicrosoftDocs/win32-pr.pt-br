---
title: Mensagem de WM_CTLCOLORLISTBOX (WinUser. h)
description: Enviado para a janela pai de uma caixa de listagem antes de o sistema desenhar a caixa de listagem. Ao responder a essa mensagem, a janela pai pode definir o texto e as cores de plano de fundo da caixa de listagem usando o identificador de contexto do dispositivo de exibição especificado.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Controles de WM_CTLCOLORLISTBOX de mensagens do Windows
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085497"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="0080f-105">Mensagem do WM \_ CTLCOLORLISTBOX</span><span class="sxs-lookup"><span data-stu-id="0080f-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="0080f-106">Enviado para a janela pai de uma caixa de listagem antes de o sistema desenhar a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0080f-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="0080f-107">Ao responder a essa mensagem, a janela pai pode definir o texto e as cores de plano de fundo da caixa de listagem usando o identificador de contexto do dispositivo de exibição especificado.</span><span class="sxs-lookup"><span data-stu-id="0080f-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0080f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0080f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0080f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0080f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0080f-110">Identificador para o contexto do dispositivo da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0080f-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="0080f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0080f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0080f-112">Identificador para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0080f-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0080f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0080f-113">Return value</span></span>

<span data-ttu-id="0080f-114">Se um aplicativo processar essa mensagem, ele deverá retornar um identificador para um pincel.</span><span class="sxs-lookup"><span data-stu-id="0080f-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="0080f-115">O sistema usa o pincel para pintar o plano de fundo da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0080f-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="0080f-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0080f-116">Remarks</span></span>

<span data-ttu-id="0080f-117">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) seleciona as cores padrão do sistema para a caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="0080f-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="0080f-118">A mensagem do **WM \_ CTLCOLORLISTBOX** nunca é enviada entre threads.</span><span class="sxs-lookup"><span data-stu-id="0080f-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="0080f-119">Ele é enviado somente dentro de um thread.</span><span class="sxs-lookup"><span data-stu-id="0080f-119">It is sent only within one thread.</span></span>

<span data-ttu-id="0080f-120">Se um procedimento de caixa de diálogo tratar essa mensagem, ele deverá converter o valor de retorno desejado para um **int \_ PTR** e retornar o valor diretamente.</span><span class="sxs-lookup"><span data-stu-id="0080f-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="0080f-121">Se o procedimento da caixa de diálogo retornar **false**, a manipulação de mensagens padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="0080f-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="0080f-122">O valor de **\_ MSGRESULT DWL** definido pela função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) é ignorado.</span><span class="sxs-lookup"><span data-stu-id="0080f-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0080f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0080f-123">Requirements</span></span>



| <span data-ttu-id="0080f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0080f-124">Requirement</span></span> | <span data-ttu-id="0080f-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0080f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0080f-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0080f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0080f-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0080f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0080f-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0080f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0080f-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0080f-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0080f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0080f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0080f-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0080f-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0080f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0080f-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0080f-133">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="0080f-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="0080f-134">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="0080f-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="0080f-135">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="0080f-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="0080f-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="0080f-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

