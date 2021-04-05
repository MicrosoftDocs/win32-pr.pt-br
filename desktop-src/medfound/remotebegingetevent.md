---
description: 'Versão remota do método IMFMediaEventGenerator:: BeginGetEvent.'
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: RemoteBeginGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827538"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="0b107-103">RemoteBeginGetEvent</span><span class="sxs-lookup"><span data-stu-id="0b107-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="0b107-104">Versão remota do método [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) .</span><span class="sxs-lookup"><span data-stu-id="0b107-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="0b107-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b107-105">Remarks</span></span>

<span data-ttu-id="0b107-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="0b107-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="0b107-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="0b107-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="0b107-108">Se [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="0b107-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b107-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b107-109">Requirements</span></span>



| <span data-ttu-id="0b107-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b107-110">Requirement</span></span> | <span data-ttu-id="0b107-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0b107-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b107-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b107-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0b107-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="0b107-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="0b107-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0b107-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0b107-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0b107-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="0b107-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b107-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b107-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b107-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="0b107-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b107-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0b107-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0b107-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="0b107-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b107-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b107-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="0b107-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




