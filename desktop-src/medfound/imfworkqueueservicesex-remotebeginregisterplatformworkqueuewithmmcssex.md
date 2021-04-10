---
description: 'Versão remota do IMFWorkQueueServicesEX:: BeginRegisterPlatformWorkQueueWithMMCSSEx.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171609"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="1a85b-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span><span class="sxs-lookup"><span data-stu-id="1a85b-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="1a85b-104">Versão remota do [**IMFWorkQueueServicesEX:: BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span><span class="sxs-lookup"><span data-stu-id="1a85b-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="1a85b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a85b-105">Remarks</span></span>

<span data-ttu-id="1a85b-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="1a85b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="1a85b-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="1a85b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="1a85b-108">Se [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="1a85b-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a85b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a85b-109">Requirements</span></span>



| <span data-ttu-id="1a85b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a85b-110">Requirement</span></span> | <span data-ttu-id="1a85b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1a85b-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1a85b-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a85b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1a85b-113">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1a85b-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1a85b-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a85b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1a85b-115">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1a85b-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1a85b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a85b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a85b-117"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a85b-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a85b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a85b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a85b-119">**IMFWorkQueueServicesEx**</span><span class="sxs-lookup"><span data-stu-id="1a85b-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




