---
title: Tipo de privacidade (Wininet. h)
description: Especifica que as configurações de privacidade são para cookies primários ou de terceiros.
ms.assetid: 7d0846d4-fd81-4af9-b7e6-05c4c1438770
topic_type:
- apiref
api_name:
- PRIVACY_TYPE_FIRST_PARTY
- PRIVACY_TYPE_THIRD_PARTY
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38583d5f0c5cee148353f98f5d2be2d4f1a50216
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824809"
---
# <a name="privacy-type"></a><span data-ttu-id="d18d5-103">Tipo de privacidade</span><span class="sxs-lookup"><span data-stu-id="d18d5-103">Privacy Type</span></span>

<span data-ttu-id="d18d5-104">Especifica que as configurações de privacidade são para cookies primários ou de terceiros.</span><span class="sxs-lookup"><span data-stu-id="d18d5-104">Specifies that privacy settings are for either first-party or third-party cookies.</span></span>

<dl> <dt>

<span data-ttu-id="d18d5-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**tipo de privacidade- \_ \_ primeira \_ entidade**</span><span class="sxs-lookup"><span data-stu-id="d18d5-105"><span id="PRIVACY_TYPE_FIRST_PARTY"></span><span id="privacy_type_first_party"></span>**PRIVACY\_TYPE\_FIRST\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18d5-106">0</span><span class="sxs-lookup"><span data-stu-id="d18d5-106">0</span></span>
</dt> <dt>



<span data-ttu-id="d18d5-107">Refere-se às configurações de privacidade para cookies de primeira entidade.</span><span class="sxs-lookup"><span data-stu-id="d18d5-107">Refers to privacy settings for first party cookies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d18d5-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**tipo de privacidade de \_ \_ terceiros \_**</span><span class="sxs-lookup"><span data-stu-id="d18d5-108"><span id="PRIVACY_TYPE_THIRD_PARTY"></span><span id="privacy_type_third_party"></span>**PRIVACY\_TYPE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d18d5-109">1</span><span class="sxs-lookup"><span data-stu-id="d18d5-109">1</span></span>
</dt> <dt>



<span data-ttu-id="d18d5-110">Refere-se às configurações de privacidade para cookies de terceiros.</span><span class="sxs-lookup"><span data-stu-id="d18d5-110">Refers to privacy settings for third party cookies.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d18d5-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d18d5-111">Remarks</span></span>

<span data-ttu-id="d18d5-112">Os cookies são categorizados como primários e de terceiros.</span><span class="sxs-lookup"><span data-stu-id="d18d5-112">Cookies are categorized as first-party and third-party.</span></span> <span data-ttu-id="d18d5-113">Um cookie primário é aquele originado do domínio do host.</span><span class="sxs-lookup"><span data-stu-id="d18d5-113">A first-party cookie is one that originates from the host domain.</span></span> <span data-ttu-id="d18d5-114">Se " https://www.blueyonderairlines.com " for encontrado na barra de endereços do Microsoft Internet Explorer, "www.blueyonderairlines.com" será o domínio do host.</span><span class="sxs-lookup"><span data-stu-id="d18d5-114">If "https://www.blueyonderairlines.com" is found in the Microsoft Internet Explorer address bar, "www.blueyonderairlines.com" is the host domain.</span></span> <span data-ttu-id="d18d5-115">Ao visitar essa página, se um cookie for definido de um domínio diferente de "www.blueyonderairlines.com", como "www.fourthcoffee.com", esse cookie será considerado um cookie de terceiros.</span><span class="sxs-lookup"><span data-stu-id="d18d5-115">While visiting this page, if a cookie is set from a domain other than "www.blueyonderairlines.com", such as "www.fourthcoffee.com", this cookie is considered a third-party cookie.</span></span>

> [!Note]  
> <span data-ttu-id="d18d5-116">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="d18d5-116">WinINet does not support server implementations.</span></span> <span data-ttu-id="d18d5-117">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="d18d5-117">In addition, it should not be used from a service.</span></span> <span data-ttu-id="d18d5-118">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="d18d5-118">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d18d5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d18d5-119">Requirements</span></span>



| <span data-ttu-id="d18d5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d18d5-120">Requirement</span></span> | <span data-ttu-id="d18d5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d18d5-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d18d5-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d18d5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d18d5-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d18d5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d18d5-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d18d5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d18d5-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d18d5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d18d5-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d18d5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d18d5-127"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="d18d5-127"><dt>Wininet.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d18d5-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d18d5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d18d5-129">**PrivacyGetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="d18d5-129">**PrivacyGetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacygetzonepreferencew)
</dt> <dt>

[<span data-ttu-id="d18d5-130">**PrivacySetZonePreferenceW**</span><span class="sxs-lookup"><span data-stu-id="d18d5-130">**PrivacySetZonePreferenceW**</span></span>](/windows/win32/api/winineti/nf-winineti-privacysetzonepreferencew)
</dt> </dl>

 

