---
description: 'Versão remota do método IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 158497a9-9d66-4e58-919d-e35765fd29e4
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7009def4e86a97720bc4b94eb2c9edb477afe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836897"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="0035e-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="0035e-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="0035e-104">Versão remota do método [**IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="0035e-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSS(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="0035e-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0035e-105">Remarks</span></span>

<span data-ttu-id="0035e-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="0035e-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="0035e-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="0035e-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="0035e-108">Se [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="0035e-108">If [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="0035e-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0035e-109">Requirements</span></span>



| <span data-ttu-id="0035e-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0035e-110">Requirement</span></span> | <span data-ttu-id="0035e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0035e-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0035e-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0035e-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0035e-113">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0035e-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0035e-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0035e-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0035e-115">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0035e-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0035e-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0035e-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0035e-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0035e-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="0035e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0035e-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0035e-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0035e-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0035e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0035e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0035e-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="0035e-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




