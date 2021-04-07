---
title: Mensagem de WM_ADSPROP_NOTIFY_EXIT (Adsprop. h)
description: Uma Active Directory extensão de folha de propriedades envia a mensagem de saída de notificação do WM \_ ADSPROP \_ \_ para o objeto de notificação quando o objeto de notificação não é mais necessário.
ms.assetid: b0f58c73-8953-412d-b801-bf34967fe0b4
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_EXIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_EXIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d74ef4b7dfa525cfb77a6d89499837cbfac8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918993"
---
# <a name="wm_adsprop_notify_exit-message"></a><span data-ttu-id="eeb7d-104">\_Mensagem de \_ saída de notificação do WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="eeb7d-104">WM\_ADSPROP\_NOTIFY\_EXIT message</span></span>

<span data-ttu-id="eeb7d-105">Uma Active Directory extensão de folha de propriedades envia a mensagem de **\_ saída de \_ notificação \_ do WM ADSPROP** para o objeto de notificação quando o objeto de notificação não é mais necessário.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-105">An Active Directory property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_EXIT** message to the notification object when the notification object is no longer required.</span></span>


```C++
WM_ADSPROP_NOTIFY_EXIT

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="eeb7d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eeb7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeb7d-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-108">O identificador do objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-108">The handle of the notification object.</span></span> <span data-ttu-id="eeb7d-109">Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="eeb7d-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="eeb7d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="eeb7d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeb7d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeb7d-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeb7d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eeb7d-114">Return value</span></span>

<span data-ttu-id="eeb7d-115">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeb7d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="eeb7d-116">Remarks</span></span>

<span data-ttu-id="eeb7d-117">O objeto de notificação será excluído em resposta a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-117">The notification object will delete itself in response to this message.</span></span> <span data-ttu-id="eeb7d-118">Quando essa mensagem é enviada, o identificador do objeto de notificação deve ser considerado inválido.</span><span class="sxs-lookup"><span data-stu-id="eeb7d-118">When this message has been sent, the notification object handle should be considered invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb7d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeb7d-119">Requirements</span></span>



| <span data-ttu-id="eeb7d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeb7d-120">Requirement</span></span> | <span data-ttu-id="eeb7d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="eeb7d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb7d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeb7d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb7d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eeb7d-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="eeb7d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="eeb7d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb7d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eeb7d-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="eeb7d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eeb7d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeb7d-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeb7d-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeb7d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="eeb7d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb7d-129">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="eeb7d-129">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="eeb7d-130">Mensagens em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="eeb7d-130">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





