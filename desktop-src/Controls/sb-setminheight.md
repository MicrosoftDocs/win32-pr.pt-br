---
title: Mensagem de SB_SETMINHEIGHT (commctrl. h)
description: Define a altura mínima da área de desenho de uma janela de status.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- Controles de SB_SETMINHEIGHT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918866"
---
# <a name="sb_setminheight-message"></a><span data-ttu-id="2c450-104">\_Mensagem de SETMINHEIGHT SB</span><span class="sxs-lookup"><span data-stu-id="2c450-104">SB\_SETMINHEIGHT message</span></span>

<span data-ttu-id="2c450-105">Define a altura mínima da área de desenho de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="2c450-105">Sets the minimum height of a status window's drawing area.</span></span>

## <a name="parameters"></a><span data-ttu-id="2c450-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c450-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c450-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c450-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c450-108">Altura mínima, em pixels, da janela.</span><span class="sxs-lookup"><span data-stu-id="2c450-108">Minimum height, in pixels, of the window.</span></span>

</dd> <dt>

<span data-ttu-id="2c450-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c450-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2c450-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2c450-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c450-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c450-111">Return value</span></span>

<span data-ttu-id="2c450-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2c450-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c450-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c450-113">Remarks</span></span>

<span data-ttu-id="2c450-114">A altura mínima é a soma de *wParam* e o dobro da largura, em pixels, da borda vertical da janela de status.</span><span class="sxs-lookup"><span data-stu-id="2c450-114">The minimum height is the sum of *wParam* and twice the width, in pixels, of the vertical border of the status window.</span></span> <span data-ttu-id="2c450-115">Um aplicativo deve enviar a mensagem de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para a janela de status para redesenhar a janela.</span><span class="sxs-lookup"><span data-stu-id="2c450-115">An application must send the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to the status window to redraw the window.</span></span> <span data-ttu-id="2c450-116">Os parâmetros *wParam* e *lParam* da mensagem **de \_ tamanho do WM** devem ser definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="2c450-116">The *wParam* and *lParam* parameters of the **WM\_SIZE** message should be set to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c450-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c450-117">Requirements</span></span>



| <span data-ttu-id="2c450-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c450-118">Requirement</span></span> | <span data-ttu-id="2c450-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2c450-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c450-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c450-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2c450-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c450-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c450-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c450-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2c450-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c450-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c450-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2c450-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c450-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c450-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

