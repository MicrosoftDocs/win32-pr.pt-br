---
description: Enviado a um ícone quando o usuário solicita que a janela seja restaurada para seu tamanho e posição anteriores.
ms.assetid: 6e14d5fd-6598-4d2e-a463-2b153c9c2aa3
title: Mensagem de WM_QUERYOPEN (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 582fcfce280c0bf98fdf92234b7fab8aaa103a91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011039"
---
# <a name="wm_queryopen-message"></a><span data-ttu-id="02ca6-103">Mensagem do WM \_ QUERYOPEN</span><span class="sxs-lookup"><span data-stu-id="02ca6-103">WM\_QUERYOPEN message</span></span>

<span data-ttu-id="02ca6-104">Enviado a um ícone quando o usuário solicita que a janela seja restaurada para seu tamanho e posição anteriores.</span><span class="sxs-lookup"><span data-stu-id="02ca6-104">Sent to an icon when the user requests that the window be restored to its previous size and position.</span></span>

<span data-ttu-id="02ca6-105">Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="02ca6-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_QUERYOPEN                    0x0013
```



## <a name="parameters"></a><span data-ttu-id="02ca6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02ca6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02ca6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02ca6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02ca6-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="02ca6-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="02ca6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02ca6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02ca6-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="02ca6-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02ca6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02ca6-111">Return value</span></span>

<span data-ttu-id="02ca6-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="02ca6-112">Type: **LRESULT**</span></span>

<span data-ttu-id="02ca6-113">Se o ícone puder ser aberto, um aplicativo que processa essa mensagem deverá retornar **true**; caso contrário, ele deve retornar **false** para impedir que o ícone seja aberto.</span><span class="sxs-lookup"><span data-stu-id="02ca6-113">If the icon can be opened, an application that processes this message should return **TRUE**; otherwise, it should return **FALSE** to prevent the icon from being opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="02ca6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="02ca6-114">Remarks</span></span>

<span data-ttu-id="02ca6-115">Por padrão, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="02ca6-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns **TRUE**.</span></span>

<span data-ttu-id="02ca6-116">Ao processar essa mensagem, o aplicativo não deve executar nenhuma ação que cause uma alteração de ativação ou de foco (por exemplo, criando uma caixa de diálogo).</span><span class="sxs-lookup"><span data-stu-id="02ca6-116">While processing this message, the application should not perform any action that would cause an activation or focus change (for example, creating a dialog box).</span></span>

## <a name="requirements"></a><span data-ttu-id="02ca6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02ca6-117">Requirements</span></span>



| <span data-ttu-id="02ca6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02ca6-118">Requirement</span></span> | <span data-ttu-id="02ca6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="02ca6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ca6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02ca6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02ca6-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="02ca6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="02ca6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="02ca6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02ca6-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="02ca6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="02ca6-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="02ca6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02ca6-125"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02ca6-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02ca6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="02ca6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="02ca6-127">**Referência**</span><span class="sxs-lookup"><span data-stu-id="02ca6-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="02ca6-128">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="02ca6-128">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="02ca6-129">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="02ca6-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="02ca6-130">Windows</span><span class="sxs-lookup"><span data-stu-id="02ca6-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
