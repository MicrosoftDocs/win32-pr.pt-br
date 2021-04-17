---
title: TsViewCookie (Textstor. h)
description: O tipo de dados TsViewCookie identifica uma exibição de contexto.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759977"
---
# <a name="tsviewcookie"></a><span data-ttu-id="dbab7-104">TsViewCookie</span><span class="sxs-lookup"><span data-stu-id="dbab7-104">TsViewCookie</span></span>

<span data-ttu-id="dbab7-105">O tipo de dados **TsViewCookie** identifica uma exibição de contexto.</span><span class="sxs-lookup"><span data-stu-id="dbab7-105">The **TsViewCookie** data type identifies a context view.</span></span>


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a><span data-ttu-id="dbab7-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbab7-106">Remarks</span></span>

<span data-ttu-id="dbab7-107">Um aplicativo deve fornecer um valor **TsViewCookie** exclusivo para cada exibição que ele cria.</span><span class="sxs-lookup"><span data-stu-id="dbab7-107">An application must supply a unique **TsViewCookie** value for each view it creates.</span></span>

<span data-ttu-id="dbab7-108">O Gerenciador de TSF obtém esse valor do aplicativo chamando [ITextStoreACP:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) ou [ITextStoreAnchor:: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span><span class="sxs-lookup"><span data-stu-id="dbab7-108">The TSF manager obtains this value from the application by calling [ITextStoreACP::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) or [ITextStoreAnchor::GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview).</span></span> <span data-ttu-id="dbab7-109">O Gerenciador de TSF usa esse valor para identificar a exibição ao chamar vários métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) ou [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .</span><span class="sxs-lookup"><span data-stu-id="dbab7-109">The TSF manager uses this value to identify the view when calling various [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) or [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbab7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbab7-110">Requirements</span></span>



| <span data-ttu-id="dbab7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbab7-111">Requirement</span></span> | <span data-ttu-id="dbab7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="dbab7-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbab7-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbab7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dbab7-114">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dbab7-114">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="dbab7-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbab7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dbab7-116">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="dbab7-116">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="dbab7-117">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="dbab7-117">Redistributable</span></span><br/>          | <span data-ttu-id="dbab7-118">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dbab7-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="dbab7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbab7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbab7-120"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbab7-120"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbab7-121">INSERI</span><span class="sxs-lookup"><span data-stu-id="dbab7-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dbab7-122"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dbab7-122"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbab7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbab7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbab7-124">**ITextStoreACP**</span><span class="sxs-lookup"><span data-stu-id="dbab7-124">**ITextStoreACP**</span></span>](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[<span data-ttu-id="dbab7-125">**ITextStoreACP:: GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="dbab7-125">**ITextStoreACP::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[<span data-ttu-id="dbab7-126">**ITextStoreAnchor::GetActiveView**</span><span class="sxs-lookup"><span data-stu-id="dbab7-126">**ITextStoreAnchor::GetActiveView**</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





