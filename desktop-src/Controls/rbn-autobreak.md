---
title: Mensagem de RBN_AUTOBREAK (commctrl. h)
description: Notifica o pai de um rebar de que uma quebra aparecerá na barra. O pai determina se a interrupção deve ser feita. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Controles de RBN_AUTOBREAK de mensagens do Windows
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824791"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="679f6-106">\_Mensagem de quebra automática de RBN</span><span class="sxs-lookup"><span data-stu-id="679f6-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="679f6-107">Notifica o pai [de um rebar](rebar-controls.md) de que uma quebra aparecerá na barra.</span><span class="sxs-lookup"><span data-stu-id="679f6-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="679f6-108">O pai determina se a interrupção deve ser feita.</span><span class="sxs-lookup"><span data-stu-id="679f6-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="679f6-109">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="679f6-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="679f6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="679f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="679f6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="679f6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="679f6-112">Ponteiro para uma estrutura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="679f6-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="679f6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="679f6-113">Return value</span></span>

<span data-ttu-id="679f6-114">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="679f6-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="679f6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="679f6-115">Remarks</span></span>

<span data-ttu-id="679f6-116">O valor no membro **fAutoBreak** da estrutura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indica se uma interrupção deve ocorrer no Rebar.</span><span class="sxs-lookup"><span data-stu-id="679f6-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="679f6-117">Para usar esse código de notificação, especifique Comctl32.dll versão 6 no manifesto.</span><span class="sxs-lookup"><span data-stu-id="679f6-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="679f6-118">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="679f6-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="679f6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="679f6-119">Requirements</span></span>



| <span data-ttu-id="679f6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="679f6-120">Requirement</span></span> | <span data-ttu-id="679f6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="679f6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="679f6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="679f6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="679f6-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="679f6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="679f6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="679f6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="679f6-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="679f6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="679f6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="679f6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="679f6-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="679f6-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





