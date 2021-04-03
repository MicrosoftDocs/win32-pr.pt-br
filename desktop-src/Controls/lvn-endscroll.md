---
title: Mensagem de LVN_ENDSCROLL (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem termina. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- Controles de LVN_ENDSCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824861"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="060d9-105">\_Mensagem de ENDrolagem do LVN</span><span class="sxs-lookup"><span data-stu-id="060d9-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="060d9-106">Notifica uma janela pai do controle de exibição de lista quando uma operação de rolagem termina.</span><span class="sxs-lookup"><span data-stu-id="060d9-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="060d9-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="060d9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="060d9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="060d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="060d9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="060d9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="060d9-110">Ponteiro para uma estrutura [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) que contém a posição horizontal ou vertical de onde a operação de rolagem termina.</span><span class="sxs-lookup"><span data-stu-id="060d9-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="060d9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="060d9-111">Return value</span></span>

<span data-ttu-id="060d9-112">Valor de retorno não usado.</span><span class="sxs-lookup"><span data-stu-id="060d9-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="060d9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="060d9-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="060d9-114">Para usar esse código de notificação, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="060d9-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="060d9-115">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="060d9-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="060d9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="060d9-116">Requirements</span></span>



| <span data-ttu-id="060d9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="060d9-117">Requirement</span></span> | <span data-ttu-id="060d9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="060d9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="060d9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="060d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="060d9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="060d9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="060d9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="060d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="060d9-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="060d9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="060d9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="060d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="060d9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="060d9-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





