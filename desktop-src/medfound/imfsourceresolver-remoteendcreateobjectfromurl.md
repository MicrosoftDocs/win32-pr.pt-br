---
description: 'Versão remota do método IMFSourceResolver:: EndCreateObjectFromURL.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797980"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="794ce-103">RemoteEndCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="794ce-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="794ce-104">Versão remota do método [**IMFSourceResolver:: EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="794ce-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="794ce-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="794ce-105">Remarks</span></span>

<span data-ttu-id="794ce-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="794ce-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="794ce-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="794ce-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="794ce-108">Se [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="794ce-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="794ce-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="794ce-109">Requirements</span></span>



| <span data-ttu-id="794ce-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="794ce-110">Requirement</span></span> | <span data-ttu-id="794ce-111">Valor</span><span class="sxs-lookup"><span data-stu-id="794ce-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="794ce-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="794ce-112">Minimum supported client</span></span><br/> | <span data-ttu-id="794ce-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="794ce-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="794ce-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="794ce-114">Minimum supported server</span></span><br/> | <span data-ttu-id="794ce-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="794ce-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="794ce-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="794ce-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="794ce-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="794ce-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="794ce-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="794ce-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="794ce-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="794ce-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="794ce-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="794ce-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="794ce-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="794ce-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




