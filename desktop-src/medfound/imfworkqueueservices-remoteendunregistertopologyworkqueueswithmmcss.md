---
description: 'Versão remota do método IMFWorkQueueServices:: EndUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798012"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="6fb16-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="6fb16-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="6fb16-104">Versão remota do método [**IMFWorkQueueServices:: EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="6fb16-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="6fb16-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fb16-105">Remarks</span></span>

<span data-ttu-id="6fb16-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="6fb16-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6fb16-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="6fb16-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6fb16-108">Se [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="6fb16-108">If [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fb16-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fb16-109">Requirements</span></span>



| <span data-ttu-id="6fb16-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fb16-110">Requirement</span></span> | <span data-ttu-id="6fb16-111">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb16-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb16-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fb16-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb16-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fb16-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6fb16-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fb16-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb16-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fb16-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6fb16-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fb16-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fb16-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6fb16-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6fb16-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fb16-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fb16-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fb16-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6fb16-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fb16-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb16-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="6fb16-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




