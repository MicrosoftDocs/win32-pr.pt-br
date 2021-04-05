---
title: RBN_CHILDSIZE código de notificação (commctrl. h)
description: Enviado por um controle rebar quando a janela filho de uma banda é redimensionada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ba64d21a-e568-4894-8007-be644ae4f54a
keywords:
- RBN_CHILDSIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_CHILDSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d505d13048d96783d53b9b1a821d80712597da4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824516"
---
# <a name="rbn_childsize-notification-code"></a><span data-ttu-id="23fc3-105">Código de notificação do RBN \_ CHILDSIZE</span><span class="sxs-lookup"><span data-stu-id="23fc3-105">RBN\_CHILDSIZE notification code</span></span>

<span data-ttu-id="23fc3-106">Enviado por um controle rebar quando a janela filho de uma banda é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="23fc3-106">Sent by a rebar control when a band's child window is resized.</span></span> <span data-ttu-id="23fc3-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="23fc3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHILDSIZE

    lprbcs = (LPNMREBARCHILDSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="23fc3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23fc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23fc3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23fc3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23fc3-110">Ponteiro para uma estrutura [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="23fc3-110">Pointer to an [**NMREBARCHILDSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchildsize) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23fc3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23fc3-111">Return value</span></span>

<span data-ttu-id="23fc3-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="23fc3-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="23fc3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23fc3-113">Requirements</span></span>



| <span data-ttu-id="23fc3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23fc3-114">Requirement</span></span> | <span data-ttu-id="23fc3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="23fc3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23fc3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fc3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23fc3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23fc3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23fc3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23fc3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23fc3-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="23fc3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23fc3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23fc3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="23fc3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23fc3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





