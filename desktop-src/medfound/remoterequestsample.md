---
description: 'Versão remota do método IMFMediaStream:: RequestSample.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: RemoteRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781451"
---
# <a name="remoterequestsample"></a><span data-ttu-id="d68ec-103">RemoteRequestSample</span><span class="sxs-lookup"><span data-stu-id="d68ec-103">RemoteRequestSample</span></span>

<span data-ttu-id="d68ec-104">Versão remota do método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="d68ec-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="d68ec-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d68ec-105">Remarks</span></span>

<span data-ttu-id="d68ec-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="d68ec-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="d68ec-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="d68ec-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="d68ec-108">Se [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="d68ec-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="d68ec-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d68ec-109">Requirements</span></span>



| <span data-ttu-id="d68ec-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d68ec-110">Requirement</span></span> | <span data-ttu-id="d68ec-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d68ec-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68ec-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d68ec-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d68ec-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="d68ec-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="d68ec-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d68ec-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d68ec-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d68ec-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="d68ec-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d68ec-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d68ec-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d68ec-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="d68ec-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d68ec-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="d68ec-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d68ec-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d68ec-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d68ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68ec-121">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="d68ec-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




