---
title: Mensagem de WM_ADSPROP_NOTIFY_PAGEHWND (Adsprop. h)
description: Uma extensão de folha de propriedades do serviço de diretório Active Directory chama o ADsPropSetHwnd para informar o objeto de notificação do identificador da janela da página de propriedades.
ms.assetid: eb8bf525-cd7f-44d0-a0f9-43178a29c443
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_PAGEHWND Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEHWND
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74ef2db993d2a3daf10f69687b8f3525ef80a87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086201"
---
# <a name="wm_adsprop_notify_pagehwnd-message"></a><span data-ttu-id="3b87e-104">\_Mensagem do \_ PAGEHWND de notificação do WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="3b87e-104">WM\_ADSPROP\_NOTIFY\_PAGEHWND message</span></span>

<span data-ttu-id="3b87e-105">Uma extensão de folha de propriedades do serviço de diretório Active Directory chama o [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) para informar o objeto de notificação do identificador da janela da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b87e-105">An Active Directory directory service property sheet extension calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) to inform the notification object of the property page window handle.</span></span> <span data-ttu-id="3b87e-106">A função **ADsPropSetHwnd** envia a mensagem **PAGEHWND do WM \_ ADSPROP \_ Notify \_** para o objeto de notificação, que informa o objeto de notificação do identificador da janela da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b87e-106">The **ADsPropSetHwnd** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEHWND** message to the notification object, which informs the notification object of the property page window handle.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEHWND

    WPARAM hPage
    LPARAM ptzTitle
    
```



## <a name="parameters"></a><span data-ttu-id="3b87e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b87e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b87e-108">*hNotifyObj*</span><span class="sxs-lookup"><span data-stu-id="3b87e-108">*hNotifyObj*</span></span> 
</dt> <dd>

<span data-ttu-id="3b87e-109">O identificador do objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="3b87e-109">The handle of the notification object.</span></span> <span data-ttu-id="3b87e-110">Para obter esse identificador, chame [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="3b87e-110">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="3b87e-111">*hPage*</span><span class="sxs-lookup"><span data-stu-id="3b87e-111">*hPage*</span></span> 
</dt> <dd>

<span data-ttu-id="3b87e-112">Um identificador de janela da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b87e-112">A window handle of the property page.</span></span>

</dd> <dt>

<span data-ttu-id="3b87e-113">*ptzTitle*</span><span class="sxs-lookup"><span data-stu-id="3b87e-113">*ptzTitle*</span></span> 
</dt> <dd>

<span data-ttu-id="3b87e-114">Ponteiro para um buffer **WCHAR** com terminação nula que contém o título da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3b87e-114">Pointer to a NULL-terminated **WCHAR** buffer that contains the title of the property page.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b87e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b87e-115">Return value</span></span>

<span data-ttu-id="3b87e-116">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3b87e-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b87e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b87e-117">Remarks</span></span>

<span data-ttu-id="3b87e-118">Uma extensão de folha de propriedades Active Directory normalmente chama a função [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) durante o processamento da mensagem [**\_ INITDIALOG do WM**](../dlgbox/wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="3b87e-118">An Active Directory property sheet extension normally calls the [**ADsPropSetHwnd**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd) function while processing the [**WM\_INITDIALOG**](../dlgbox/wm-initdialog.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b87e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b87e-119">Requirements</span></span>



| <span data-ttu-id="3b87e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b87e-120">Requirement</span></span> | <span data-ttu-id="3b87e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3b87e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3b87e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b87e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3b87e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b87e-123">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="3b87e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b87e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3b87e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b87e-125">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="3b87e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b87e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b87e-127"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b87e-127"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b87e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b87e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b87e-129">Mensagens em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="3b87e-129">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="3b87e-130">**ADsPropSetHwnd**</span><span class="sxs-lookup"><span data-stu-id="3b87e-130">**ADsPropSetHwnd**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropsethwnd)
</dt> <dt>

[<span data-ttu-id="3b87e-131">**ADsPropCreateNotifyObj**</span><span class="sxs-lookup"><span data-stu-id="3b87e-131">**ADsPropCreateNotifyObj**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)
</dt> <dt>

[<span data-ttu-id="3b87e-132">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3b87e-132">**WM\_INITDIALOG**</span></span>](../dlgbox/wm-initdialog.md)
</dt> </dl>

 

