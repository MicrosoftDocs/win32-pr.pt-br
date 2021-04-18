---
description: 'Versão remota do método IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: RemoteBeginRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763479"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="98ad8-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="98ad8-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="98ad8-104">Versão remota do método [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="98ad8-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a><span data-ttu-id="98ad8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="98ad8-105">Remarks</span></span>

<span data-ttu-id="98ad8-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="98ad8-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="98ad8-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="98ad8-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="98ad8-108">Se [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="98ad8-108">If [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="98ad8-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98ad8-109">Requirements</span></span>



| <span data-ttu-id="98ad8-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="98ad8-110">Requirement</span></span> | <span data-ttu-id="98ad8-111">Valor</span><span class="sxs-lookup"><span data-stu-id="98ad8-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ad8-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98ad8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="98ad8-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98ad8-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="98ad8-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98ad8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="98ad8-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98ad8-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98ad8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98ad8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="98ad8-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98ad8-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="98ad8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98ad8-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="98ad8-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="98ad8-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="98ad8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="98ad8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ad8-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="98ad8-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




