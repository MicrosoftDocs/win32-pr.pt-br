---
description: 'Versão remota do método IMFMediaSource:: CreatePresentationDescriptor.'
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: RemoteCreatePresentationDescriptor (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091037"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="8a302-103">RemoteCreatePresentationDescriptor</span><span class="sxs-lookup"><span data-stu-id="8a302-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="8a302-104">Versão remota do método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="8a302-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="8a302-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a302-105">Remarks</span></span>

<span data-ttu-id="8a302-106">Os aplicativos não podem chamar esse método diretamente e os objetos não implementam esse método.</span><span class="sxs-lookup"><span data-stu-id="8a302-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="8a302-107">O método não aparece no vtable para a interface.</span><span class="sxs-lookup"><span data-stu-id="8a302-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="8a302-108">Se [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) for chamado entre limites de processo, a dll Media Foundation proxy/stub converterá a chamada em uma chamada para o método remoto e a converterá de volta.</span><span class="sxs-lookup"><span data-stu-id="8a302-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a302-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a302-109">Requirements</span></span>



| <span data-ttu-id="8a302-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a302-110">Requirement</span></span> | <span data-ttu-id="8a302-111">Valor</span><span class="sxs-lookup"><span data-stu-id="8a302-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a302-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a302-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8a302-113">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a302-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="8a302-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a302-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8a302-115">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8a302-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="8a302-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a302-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a302-117"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a302-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="8a302-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a302-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a302-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a302-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8a302-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a302-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a302-121">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="8a302-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




