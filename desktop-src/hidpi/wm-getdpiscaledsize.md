---
title: Mensagem de WM_GETDPISCALEDSIZE (WinUser. h)
description: Essa mensagem informa ao sistema operacional que a janela será dimensionada para dimensões que não sejam o padrão.
ms.assetid: 038CAA21-0944-45D3-8C40-A6498F36D9E4
keywords:
- DPI alta de mensagem de WM_GETDPISCALEDSIZE
topic_type:
- apiref
api_name:
- WM_GETDPISCALEDSIZE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95631e51247d7919307f36dd0af10c72621a612
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455193"
---
# <a name="wm_getdpiscaledsize-message"></a><span data-ttu-id="35678-104">Mensagem do WM \_ GETDPISCALEDSIZE</span><span class="sxs-lookup"><span data-stu-id="35678-104">WM\_GETDPISCALEDSIZE message</span></span>

<span data-ttu-id="35678-105">Essa mensagem informa ao sistema operacional que a janela será dimensionada para dimensões que não sejam o padrão.</span><span class="sxs-lookup"><span data-stu-id="35678-105">This message tells the operating system that the window will be sized to dimensions other than the default.</span></span>

<span data-ttu-id="35678-106">Essa mensagem é enviada para janelas de nível superior com um [ \_ \_ contexto de reconhecimento de DPI](dpi-awareness-context.md) de por monitor v2 antes de uma mensagem de [**\_ DPICHANGED do WM**](wm-dpichanged.md) ser enviada e permite que a janela computasse seu tamanho desejado para a alteração de DPI pendente.</span><span class="sxs-lookup"><span data-stu-id="35678-106">This message is sent to top-level windows with a [DPI\_AWARENESS\_CONTEXT](dpi-awareness-context.md) of Per Monitor v2 before a [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent, and allows the window to compute its desired size for the pending DPI change.</span></span> <span data-ttu-id="35678-107">Como o dimensionamento de DPI linear é o comportamento padrão, isso só é útil em cenários em que a janela deseja dimensionar de forma não linear.</span><span class="sxs-lookup"><span data-stu-id="35678-107">As linear DPI scaling is the default behavior, this is only useful in scenarios where the window wants to scale non-linearly.</span></span> <span data-ttu-id="35678-108">Se o aplicativo responder a essa mensagem, o tamanho resultante será o retângulo candidato enviar para o **WM \_ DPICHANGED**.</span><span class="sxs-lookup"><span data-stu-id="35678-108">If the application responds to this message, the resulting size will be the candidate rectangle send to **WM\_DPICHANGED**.</span></span>

<span data-ttu-id="35678-109">Use esta mensagem para alterar o tamanho do Rect fornecido com o [**WM \_ DPICHANGED**](wm-dpichanged.md).</span><span class="sxs-lookup"><span data-stu-id="35678-109">Use this message to alter the size of the rect that is provided with [**WM\_DPICHANGED**](wm-dpichanged.md).</span></span>


```C++
#define WM_GETDPISCALEDSIZE       0x02E4
```



## <a name="parameters"></a><span data-ttu-id="35678-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35678-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35678-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35678-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35678-112">WPARAM contém um valor de DPI.</span><span class="sxs-lookup"><span data-stu-id="35678-112">The WPARAM contains a DPI value.</span></span> <span data-ttu-id="35678-113">O tamanho da janela dimensionada que o aplicativo definiria precisa ser computado como se a janela fosse mudar para esse DPI.</span><span class="sxs-lookup"><span data-stu-id="35678-113">The scaled window size that the application would set needs to be computed as if the window were to switch to this DPI.</span></span>

</dd> <dt>

<span data-ttu-id="35678-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35678-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35678-115">O LPARAM é um ponteiro de entrada/saída para uma estrutura de tamanho.</span><span class="sxs-lookup"><span data-stu-id="35678-115">The LPARAM is an in/out pointer to a SIZE struct.</span></span> <span data-ttu-id="35678-116">O \_ \_ valor in no lParam é o tamanho pendente da janela após uma movimentação iniciada pelo usuário ou uma chamada para [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span><span class="sxs-lookup"><span data-stu-id="35678-116">The \_In\_ value in the LPARAM is the pending size of the window after a user-initiated move or a call to [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="35678-117">Se a janela estiver sendo redimensionada, esse tamanho não será necessariamente o mesmo que o tamanho atual da janela no momento em que essa mensagem for recebida.</span><span class="sxs-lookup"><span data-stu-id="35678-117">If the window is being resized, this size is not necessarily the same as the window's current size at the time this message is received.</span></span>

<span data-ttu-id="35678-118">O \_ \_ valor out no lParam deve ser gravado pelo aplicativo para especificar o tamanho de janela dimensionado desejado correspondente ao valor de DPI fornecido no wParam.</span><span class="sxs-lookup"><span data-stu-id="35678-118">The \_Out\_ value in the LPARAM should be written to by the application to specify the desired scaled window size corresponding to the provided DPI value in the WPARAM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35678-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35678-119">Return value</span></span>

<span data-ttu-id="35678-120">A função retorna um BOOL.</span><span class="sxs-lookup"><span data-stu-id="35678-120">The function returns a BOOL.</span></span> <span data-ttu-id="35678-121">Retornar TRUE indica que um novo tamanho foi computado.</span><span class="sxs-lookup"><span data-stu-id="35678-121">Returning TRUE indicates that a new size has been computed.</span></span> <span data-ttu-id="35678-122">Retornar FALSE indica que a mensagem não será tratada e o dimensionamento de DPI linear padrão será aplicado à janela.</span><span class="sxs-lookup"><span data-stu-id="35678-122">Returning FALSE indicates that the message will not be handled, and the default linear DPI scaling will apply to the window.</span></span>

## <a name="remarks"></a><span data-ttu-id="35678-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35678-123">Remarks</span></span>

<span data-ttu-id="35678-124">Esta mensagem é enviada somente para janelas de nível superior que têm um contexto de reconhecimento de DPI de por monitor v2.</span><span class="sxs-lookup"><span data-stu-id="35678-124">This message is only sent to top-level windows which have a DPI awareness context of Per Monitor v2.</span></span>

<span data-ttu-id="35678-125">Esse evento é necessário para facilitar o dimensionamento não linear normal e garante que a posição do Windows permaneça constante em relação ao cursor e ao mover-se para frente e para trás entre monitores.</span><span class="sxs-lookup"><span data-stu-id="35678-125">This event is necessary to facilitate graceful non-linear scaling, and ensures that the windows's position remains constant in relationship to the cursor and when moving back and forth across monitors.</span></span>

<span data-ttu-id="35678-126">Não há nenhum tratamento padrão específico dessa mensagem em [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="35678-126">There is no specific default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="35678-127">Como para todas as mensagens que ele não manipula explicitamente, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) retornará zero para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="35678-127">As for all messages it does not explicitly handle, [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will return zero for this message.</span></span> <span data-ttu-id="35678-128">Conforme observado acima, esse retorno informa ao sistema para usar o comportamento linear padrão.</span><span class="sxs-lookup"><span data-stu-id="35678-128">As noted above, this return tells the system to use the default linear behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="35678-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35678-129">Requirements</span></span>



| <span data-ttu-id="35678-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="35678-130">Requirement</span></span> | <span data-ttu-id="35678-131">Valor</span><span class="sxs-lookup"><span data-stu-id="35678-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="35678-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35678-132">Minimum supported client</span></span><br/> | <span data-ttu-id="35678-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="35678-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="35678-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="35678-134">Minimum supported server</span></span><br/> | <span data-ttu-id="35678-135">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="35678-135">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="35678-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35678-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="35678-137"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="35678-137"><dt>Winuser.h</dt></span></span> </dl> |



 

