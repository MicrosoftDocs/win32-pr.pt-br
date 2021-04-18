---
description: 'Versão remota do método IMFSourceResolver:: BeginCreateObjectFromURL.'
ms.assetid: 3c0b0aaf-832b-4708-bed9-6f448770ee77
title: RemoteBeginCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9d9a72ab5522b56fc0b78238f6a1dbc9aae0c6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814148"
---
# <a name="remotebegincreateobjectfromurl"></a><span data-ttu-id="49ddb-103">RemoteBeginCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="49ddb-103">RemoteBeginCreateObjectFromURL</span></span>

<span data-ttu-id="49ddb-104">Versão remota do método [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="49ddb-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromURL)]
HRESULT RemoteBeginCreateObjectFromURL(
    LPCWSTR pwszURL,
    DWORD dwFlags,
    IPropertyStore *pProps,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="49ddb-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="49ddb-105">Remarks</span></span>

<span data-ttu-id="49ddb-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="49ddb-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="49ddb-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="49ddb-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="49ddb-108">Se [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="49ddb-108">If [**BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="49ddb-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49ddb-109">Requirements</span></span>



| <span data-ttu-id="49ddb-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="49ddb-110">Requirement</span></span> | <span data-ttu-id="49ddb-111">Valor</span><span class="sxs-lookup"><span data-stu-id="49ddb-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49ddb-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49ddb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="49ddb-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="49ddb-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="49ddb-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49ddb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="49ddb-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="49ddb-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="49ddb-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49ddb-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="49ddb-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49ddb-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="49ddb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49ddb-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="49ddb-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49ddb-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="49ddb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="49ddb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49ddb-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="49ddb-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




