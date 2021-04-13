---
title: Mensagem de WM_ADSPROP_NOTIFY_PAGEINIT (Adsprop. h)
description: Uma Active Directory extensão de folha de propriedades chama o ADsPropGetInitInfo para obter dados sobre o objeto de diretório ao qual a extensão de folha de propriedades se aplica.
ms.assetid: 473c5a75-d0d9-4d12-b855-63683e8cdf3f
ms.tgt_platform: multiple
keywords:
- Mensagem de WM_ADSPROP_NOTIFY_PAGEINIT Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_NOTIFY_PAGEINIT
api_location:
- Adsprop.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2718ee30cdbecec7c4e0954636aa14c75f13027
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499315"
---
# <a name="wm_adsprop_notify_pageinit-message"></a><span data-ttu-id="f1b33-104">\_Mensagem do \_ PAGEINIT de notificação do WM ADSPROP \_</span><span class="sxs-lookup"><span data-stu-id="f1b33-104">WM\_ADSPROP\_NOTIFY\_PAGEINIT message</span></span>

<span data-ttu-id="f1b33-105">Uma Active Directory extensão de folha de propriedades chama o [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) para obter dados sobre o objeto de diretório ao qual a extensão de folha de propriedades se aplica.</span><span class="sxs-lookup"><span data-stu-id="f1b33-105">An Active Directory property sheet extension calls the [**ADsPropGetInitInfo**](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo) to obtain data about regarding the directory object that the property sheet extension applies to.</span></span> <span data-ttu-id="f1b33-106">A função **ADsPropGetInitInfo** envia a mensagem **PAGEINIT do WM \_ ADSPROP \_ Notify \_** para o objeto de notificação para obter esse resultado.</span><span class="sxs-lookup"><span data-stu-id="f1b33-106">The **ADsPropGetInitInfo** function sends the **WM\_ADSPROP\_NOTIFY\_PAGEINIT** message to the notification object to achieve this result.</span></span>


```C++
WM_ADSPROP_NOTIFY_PAGEINIT

    WPARAM wParam
    LPARAM pADsPropInitParams
    
```



## <a name="parameters"></a><span data-ttu-id="f1b33-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1b33-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b33-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f1b33-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b33-109">Identificador do objeto de notificação.</span><span class="sxs-lookup"><span data-stu-id="f1b33-109">Handle of the notification object.</span></span> <span data-ttu-id="f1b33-110">Esse é o parâmetro *hNotifyObject* obtido por uma chamada para [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="f1b33-110">This is the *hNotifyObject* parameter obtained by a call to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="f1b33-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f1b33-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b33-112">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f1b33-112">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="f1b33-113">*pADsPropInitParams*</span><span class="sxs-lookup"><span data-stu-id="f1b33-113">*pADsPropInitParams*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b33-114">Ponteiro para uma estrutura [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) que recebe as informações do objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="f1b33-114">Pointer to an [**ADSPROPINITPARAMS**](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams) structure that receives the directory object information.</span></span> <span data-ttu-id="f1b33-115">Esse é o parâmetro *pInitParams* passado para [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="f1b33-115">This is the *pInitParams* parameter passed to [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b33-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1b33-116">Return value</span></span>

<span data-ttu-id="f1b33-117">Esta mensagem não tem nenhum valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f1b33-117">This message has no return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b33-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1b33-118">Requirements</span></span>



| <span data-ttu-id="f1b33-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b33-119">Requirement</span></span> | <span data-ttu-id="f1b33-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f1b33-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1b33-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1b33-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b33-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1b33-122">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="f1b33-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1b33-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b33-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1b33-124">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="f1b33-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1b33-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b33-126"><dt>Adsprop. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b33-126"><dt>Adsprop.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b33-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1b33-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b33-128">Mensagens em Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="f1b33-128">Messages in Active Directory Domain Services</span></span>](messages-in-active-directory-domain-services.md)
</dt> <dt>

[<span data-ttu-id="f1b33-129">**ADsPropGetInitInfo**</span><span class="sxs-lookup"><span data-stu-id="f1b33-129">**ADsPropGetInitInfo**</span></span>](/windows/desktop/api/Adsprop/nf-adsprop-adspropgetinitinfo)
</dt> <dt>

[<span data-ttu-id="f1b33-130">**ADSPROPINITPARAMS**</span><span class="sxs-lookup"><span data-stu-id="f1b33-130">**ADSPROPINITPARAMS**</span></span>](/windows/desktop/api/Adsprop/ns-adsprop-adspropinitparams)
</dt> </dl>

 

 





