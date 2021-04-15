---
description: 'Versão remota do método IMFWorkQueueServices:: EndRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: RemoteEndRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760992"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="55c24-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="55c24-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="55c24-104">Versão remota do método [**IMFWorkQueueServices:: EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="55c24-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="55c24-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="55c24-105">Remarks</span></span>

<span data-ttu-id="55c24-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="55c24-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="55c24-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="55c24-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="55c24-108">Se [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="55c24-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c24-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55c24-109">Requirements</span></span>



| <span data-ttu-id="55c24-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="55c24-110">Requirement</span></span> | <span data-ttu-id="55c24-111">Valor</span><span class="sxs-lookup"><span data-stu-id="55c24-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c24-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c24-112">Minimum supported client</span></span><br/> | <span data-ttu-id="55c24-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55c24-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55c24-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55c24-114">Minimum supported server</span></span><br/> | <span data-ttu-id="55c24-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55c24-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="55c24-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55c24-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="55c24-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55c24-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="55c24-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55c24-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="55c24-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55c24-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="55c24-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="55c24-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c24-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="55c24-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




