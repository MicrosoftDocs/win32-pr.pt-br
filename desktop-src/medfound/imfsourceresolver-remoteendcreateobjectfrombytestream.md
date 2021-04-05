---
description: 'Versão remota do método IMFSourceResolver:: EndCreateObjectFromByteStream.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: RemoteEndCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba53b7d22ed79cb97edba034dc4c61d9aa27fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090871"
---
# <a name="remoteendcreateobjectfrombytestream"></a><span data-ttu-id="1d6df-103">RemoteEndCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="1d6df-103">RemoteEndCreateObjectFromByteStream</span></span>

<span data-ttu-id="1d6df-104">Versão remota do método [**IMFSourceResolver:: EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="1d6df-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="1d6df-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d6df-105">Remarks</span></span>

<span data-ttu-id="1d6df-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="1d6df-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="1d6df-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="1d6df-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="1d6df-108">Se [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="1d6df-108">If [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6df-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d6df-109">Requirements</span></span>



| <span data-ttu-id="1d6df-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d6df-110">Requirement</span></span> | <span data-ttu-id="1d6df-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1d6df-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6df-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d6df-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1d6df-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="1d6df-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="1d6df-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d6df-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1d6df-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1d6df-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="1d6df-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d6df-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d6df-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d6df-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="1d6df-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d6df-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d6df-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d6df-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="1d6df-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d6df-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6df-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="1d6df-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




