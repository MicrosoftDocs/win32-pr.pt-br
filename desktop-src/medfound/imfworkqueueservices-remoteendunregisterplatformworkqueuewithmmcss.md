---
description: 'Versão remota do método IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836895"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="040cb-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="040cb-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="040cb-104">Versão remota do método [**IMFWorkQueueServices:: EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="040cb-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="040cb-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="040cb-105">Remarks</span></span>

<span data-ttu-id="040cb-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="040cb-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="040cb-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="040cb-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="040cb-108">Se [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="040cb-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="040cb-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="040cb-109">Requirements</span></span>



| <span data-ttu-id="040cb-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="040cb-110">Requirement</span></span> | <span data-ttu-id="040cb-111">Valor</span><span class="sxs-lookup"><span data-stu-id="040cb-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="040cb-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="040cb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="040cb-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="040cb-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="040cb-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="040cb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="040cb-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="040cb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="040cb-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="040cb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="040cb-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="040cb-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="040cb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="040cb-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="040cb-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="040cb-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="040cb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="040cb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040cb-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="040cb-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




