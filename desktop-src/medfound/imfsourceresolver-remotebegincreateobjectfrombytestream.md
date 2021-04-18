---
description: 'Versão remota do método IMFSourceResolver:: BeginCreateObjectFromByteStream.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: RemoteBeginCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797981"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="3f3bd-103">RemoteBeginCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="3f3bd-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="3f3bd-104">Versão remota do método [**IMFSourceResolver:: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="3f3bd-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="3f3bd-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f3bd-105">Remarks</span></span>

<span data-ttu-id="3f3bd-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3f3bd-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3f3bd-108">Se [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="3f3bd-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3bd-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f3bd-109">Requirements</span></span>



| <span data-ttu-id="3f3bd-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f3bd-110">Requirement</span></span> | <span data-ttu-id="3f3bd-111">Valor</span><span class="sxs-lookup"><span data-stu-id="3f3bd-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3bd-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f3bd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3bd-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="3f3bd-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="3f3bd-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f3bd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3bd-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3f3bd-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="3f3bd-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f3bd-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f3bd-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f3bd-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3f3bd-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f3bd-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3f3bd-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f3bd-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3f3bd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f3bd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3bd-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="3f3bd-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




