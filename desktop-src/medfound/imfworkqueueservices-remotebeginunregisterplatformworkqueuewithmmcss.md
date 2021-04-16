---
description: 'Versão remota do método IMFWorkQueueServices:: BeginUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: c3117086-268e-4e52-acfb-2c8167adaa07
title: RemoteBeginUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab364f041d6bc8d0f6275879c82a937e98f463b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761194"
---
# <a name="remotebeginunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="ac363-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="ac363-103">RemoteBeginUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="ac363-104">Versão remota do método [**IMFWorkQueueServices:: BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="ac363-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginUnregisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="ac363-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac363-105">Remarks</span></span>

<span data-ttu-id="ac363-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="ac363-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="ac363-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="ac363-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="ac363-108">Se [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="ac363-108">If [**BeginUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac363-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac363-109">Requirements</span></span>



| <span data-ttu-id="ac363-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac363-110">Requirement</span></span> | <span data-ttu-id="ac363-111">Valor</span><span class="sxs-lookup"><span data-stu-id="ac363-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac363-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac363-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ac363-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac363-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ac363-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac363-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ac363-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ac363-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ac363-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac363-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac363-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac363-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ac363-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ac363-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="ac363-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac363-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ac363-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac363-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac363-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="ac363-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




