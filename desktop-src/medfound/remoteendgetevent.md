---
description: 'Versão remota do método IMFMediaEventGenerator:: EndGetEvent.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: RemoteEndGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647745"
---
# <a name="remoteendgetevent"></a><span data-ttu-id="99b99-103">RemoteEndGetEvent</span><span class="sxs-lookup"><span data-stu-id="99b99-103">RemoteEndGetEvent</span></span>

<span data-ttu-id="99b99-104">Versão remota do método [**IMFMediaEventGenerator:: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) .</span><span class="sxs-lookup"><span data-stu-id="99b99-104">Remotable version of the [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) method.</span></span>

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a><span data-ttu-id="99b99-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="99b99-105">Remarks</span></span>

<span data-ttu-id="99b99-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="99b99-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="99b99-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="99b99-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="99b99-108">Se [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="99b99-108">If [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="99b99-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99b99-109">Requirements</span></span>



| <span data-ttu-id="99b99-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="99b99-110">Requirement</span></span> | <span data-ttu-id="99b99-111">Valor</span><span class="sxs-lookup"><span data-stu-id="99b99-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99b99-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b99-112">Minimum supported client</span></span><br/> | <span data-ttu-id="99b99-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="99b99-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="99b99-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="99b99-114">Minimum supported server</span></span><br/> | <span data-ttu-id="99b99-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="99b99-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="99b99-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99b99-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b99-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99b99-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="99b99-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99b99-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="99b99-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b99-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="99b99-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="99b99-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b99-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="99b99-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




