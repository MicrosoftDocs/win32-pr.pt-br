---
title: LVN_BEGINSCROLL código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem é iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454695"
---
# <a name="lvn_beginscroll-notification-code"></a><span data-ttu-id="d7674-105">Código de notificação do LVN \_ BEGINSCROLL</span><span class="sxs-lookup"><span data-stu-id="d7674-105">LVN\_BEGINSCROLL notification code</span></span>

<span data-ttu-id="d7674-106">Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem é iniciada.</span><span class="sxs-lookup"><span data-stu-id="d7674-106">Notifies a list-view control's parent window when a scrolling operation starts.</span></span> <span data-ttu-id="d7674-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d7674-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="d7674-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7674-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7674-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7674-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7674-110">Ponteiro para uma estrutura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contém a posição horizontal ou vertical de onde a operação de rolagem é iniciada.</span><span class="sxs-lookup"><span data-stu-id="d7674-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation starts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7674-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7674-111">Return value</span></span>

<span data-ttu-id="d7674-112">Valor de retorno não usado.</span><span class="sxs-lookup"><span data-stu-id="d7674-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7674-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7674-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d7674-114">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="d7674-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d7674-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d7674-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7674-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7674-116">Requirements</span></span>



| <span data-ttu-id="d7674-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7674-117">Requirement</span></span> | <span data-ttu-id="d7674-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d7674-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7674-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7674-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d7674-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7674-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7674-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7674-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d7674-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7674-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7674-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7674-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7674-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7674-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





