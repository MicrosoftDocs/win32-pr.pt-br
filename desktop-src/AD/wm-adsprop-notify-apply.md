---
title: Mensagem de WM_ADSPROP_NOTIFY_APPLY (Adsprop. h)
description: Uma extensão de folha de propriedades do serviço de diretório Active Directory envia a \_ \_ mensagem de aplicação notificar ADSPROP do WM \_ para o objeto de notificação se o manipulador da página de propriedades PSN \_ Apply for executado com sucesso.
ms.assetid: 3536054b-83ee-4cfa-ab54-c0af3a46289e
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_APPLY Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_APPLY
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0ccd5bb95e3f092634d54ba0534e81ded6701bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756090"
---
# <a name="wm_adsprop_notify_apply-message"></a><span data-ttu-id="7da64-104">\_Mensagem de \_ aplicação de notificação do WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="7da64-104">WM\_ADSPROP\_NOTIFY\_APPLY message</span></span>

<span data-ttu-id="7da64-105">Uma extensão de folha de propriedades do serviço de diretório Active Directory envia a mensagem de **\_ \_ \_ aplicação notificar ADSPROP do WM** para o objeto de notificação se o manipulador da página de propriedades PSN \_ Apply for executado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="7da64-105">An Active Directory directory service property sheet extension sends the **WM\_ADSPROP\_NOTIFY\_APPLY** message to the notification object if the property page PSN\_APPLY handler succeeds.</span></span>


```C++
WM_ADSPROP_NOTIFY_APPLY

    WPARAM wParam
    LPARAM lParam
    
```



## <a name="parameters"></a><span data-ttu-id="7da64-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7da64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da64-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="7da64-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7da64-108">O identificador do objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="7da64-108">The handle of the notification object.</span></span> <span data-ttu-id="7da64-109">Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="7da64-109">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="7da64-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7da64-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7da64-111">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7da64-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="7da64-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7da64-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7da64-113">Não usado.</span><span class="sxs-lookup"><span data-stu-id="7da64-113">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da64-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7da64-114">Return value</span></span>

<span data-ttu-id="7da64-115">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7da64-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7da64-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7da64-116">Remarks</span></span>

<span data-ttu-id="7da64-117">Ao adicionar páginas ao snap-in do MMC do Active Directory Manager, Active Directory folhas de propriedades do MMC criam os objetos de notificação por uma chamada à função [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) e, em seguida, passa o identificador do objeto de notificação para cada página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7da64-117">When adding pages to the Active Directory Manager MMC snap-in, Active Directory MMC property sheets create the notification objects by a call to the [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj) function, and then passes the notification object handle to each property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da64-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7da64-118">Requirements</span></span>



| <span data-ttu-id="7da64-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7da64-119">Requirement</span></span> | <span data-ttu-id="7da64-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7da64-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7da64-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7da64-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7da64-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7da64-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="7da64-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7da64-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7da64-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7da64-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="7da64-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7da64-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da64-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da64-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7da64-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7da64-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da64-128">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="7da64-128">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="7da64-129">Mensagens em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="7da64-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> </dl>

 

 





