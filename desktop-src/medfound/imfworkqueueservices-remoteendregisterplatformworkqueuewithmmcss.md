---
description: 'Versão remota do método IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: cb15129e-a3ad-4351-a7d6-dd4b883437bd
title: RemoteEndRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673281a8ed4e4c4174ecd2d874e7032776ea44c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646574"
---
# <a name="remoteendregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="d2640-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="d2640-103">RemoteEndRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="d2640-104">Versão remota do método [**IMFWorkQueueServices:: EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="d2640-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndRegisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult,
    DWORD *pdwTaskId
);
```

## <a name="remarks"></a><span data-ttu-id="d2640-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2640-105">Remarks</span></span>

<span data-ttu-id="d2640-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="d2640-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="d2640-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="d2640-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="d2640-108">Se [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="d2640-108">If [**EndRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2640-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2640-109">Requirements</span></span>



| <span data-ttu-id="d2640-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2640-110">Requirement</span></span> | <span data-ttu-id="d2640-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d2640-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2640-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2640-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d2640-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2640-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d2640-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2640-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d2640-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d2640-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d2640-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2640-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2640-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2640-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="d2640-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d2640-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2640-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d2640-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d2640-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2640-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2640-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="d2640-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




