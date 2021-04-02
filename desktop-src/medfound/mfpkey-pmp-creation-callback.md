---
description: Define um retorno de chamada que cria a sessão de mídia do PMP durante a resolução da origem.
ms.assetid: 7277C5E0-BB91-4EEA-9529-64E66D179CDC
title: Propriedade MFPKEY_PMP_Creation_Callback (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b18e04a15e035a9e4dc04a4039ce230342031a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165379"
---
# <a name="mfpkey_pmp_creation_callback-property"></a><span data-ttu-id="43a51-103">\_Propriedade de \_ retorno de chamada de criação do MFPKEY PMP \_</span><span class="sxs-lookup"><span data-stu-id="43a51-103">MFPKEY\_PMP\_Creation\_Callback property</span></span>

<span data-ttu-id="43a51-104">Define um retorno de chamada que cria a [sessão de mídia do PMP](pmp-media-session.md) durante a resolução da origem.</span><span class="sxs-lookup"><span data-stu-id="43a51-104">Sets a callback that creates the [PMP Media Session](pmp-media-session.md) during source resolution.</span></span>



<span data-ttu-id="43a51-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="43a51-105">Data type</span></span>

<span data-ttu-id="43a51-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="43a51-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="43a51-107">Membro PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="43a51-107">PROPVARIANT member</span></span>

<span data-ttu-id="43a51-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="43a51-108">\**IUnknown\** _</span></span>

<span data-ttu-id="43a51-109">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="43a51-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="43a51-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="43a51-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="43a51-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="43a51-111">Remarks</span></span>

<span data-ttu-id="43a51-112">Um conteúdo protegido pode exigir o uso dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="43a51-112">Some protected content might require the use of this property.</span></span> <span data-ttu-id="43a51-113">Nesse caso, o processo de resolução de origem falha com o código de erro **MF \_ E a \_ resolução \_ requer o retorno de chamada de \_ \_ criação \_ de PMP**.</span><span class="sxs-lookup"><span data-stu-id="43a51-113">If so, the source resolution process fails with the error code **MF\_E\_RESOLUTION\_REQUIRES\_PMP\_CREATION\_CALLBACK**.</span></span>

<span data-ttu-id="43a51-114">Para usar essa propriedade, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="43a51-114">To use this property, do the following.</span></span>

1.  <span data-ttu-id="43a51-115">Chame [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para criar um repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="43a51-115">Call [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) to create a property store.</span></span>
2.  <span data-ttu-id="43a51-116">Implemente a interface de retorno de chamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="43a51-116">Implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback interface.</span></span>
3.  <span data-ttu-id="43a51-117">Defina a propriedade de retorno de chamada de criação do MFPKEY \_ PMP \_ \_ no repositório de propriedades.</span><span class="sxs-lookup"><span data-stu-id="43a51-117">Set the MFPKEY\_PMP\_Creation\_Callback property on the property store.</span></span> <span data-ttu-id="43a51-118">O valor é um ponteiro para a implementação de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="43a51-118">The value is a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) implementation.</span></span>
4.  <span data-ttu-id="43a51-119">Chame [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span><span class="sxs-lookup"><span data-stu-id="43a51-119">Call [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl).</span></span> <span data-ttu-id="43a51-120">Passe um ponteiro para o repositório de propriedades no parâmetro *pProps* .</span><span class="sxs-lookup"><span data-stu-id="43a51-120">Pass in a pointer to the property store in the *pProps* parameter.</span></span>

<span data-ttu-id="43a51-121">No método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) da sua interface de retorno de chamada, faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="43a51-121">In the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of your callback interface, do the following.</span></span>

1.  <span data-ttu-id="43a51-122">Chame [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) para criar a [sessão de mídia do PMP](pmp-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="43a51-122">Call [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) to create the [PMP Media Session](pmp-media-session.md).</span></span>
2.  <span data-ttu-id="43a51-123">Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) na sessão de mídia do PMP para um ponteiro para a interface [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) .</span><span class="sxs-lookup"><span data-stu-id="43a51-123">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) on the PMP Media Session to a pointer to the [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) interface.</span></span>
3.  <span data-ttu-id="43a51-124">Chame [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) no objeto result que é passado no parâmetro *pAsyncResult* de [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="43a51-124">Call [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate) on the result object that is passed in the *pAsyncResult* parameter of [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="43a51-125">Consulte o ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retornado para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="43a51-125">Query the returned [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer for the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>
4.  <span data-ttu-id="43a51-126">Chame [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) com os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="43a51-126">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) with the following parameters:</span></span>
    -   <span data-ttu-id="43a51-127">*dwQueue*: **MFASYNC de \_ fila de retorno de chamada \_ \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="43a51-127">*dwQueue*: **MFASYNC\_CALLBACK\_QUEUE\_STANDARD**</span></span>
    -   <span data-ttu-id="43a51-128">*pCallback*: o ponteiro [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) obtido na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="43a51-128">*pCallback*: The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) pointer obtained in step 3.</span></span>
    -   <span data-ttu-id="43a51-129">*pState*: o ponteiro [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) obtido na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="43a51-129">*pState*: The [**IMFPMPHost**](/windows/desktop/api/mfidl/nn-mfidl-imfpmphost) pointer obtained in step 2.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a51-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a51-130">Requirements</span></span>



| <span data-ttu-id="43a51-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a51-131">Requirement</span></span> | <span data-ttu-id="43a51-132">Valor</span><span class="sxs-lookup"><span data-stu-id="43a51-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43a51-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a51-133">Minimum supported client</span></span><br/> | <span data-ttu-id="43a51-134">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="43a51-134">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="43a51-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a51-135">Minimum supported server</span></span><br/> | <span data-ttu-id="43a51-136">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="43a51-136">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="43a51-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43a51-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a51-138"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a51-138"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a51-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a51-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a51-140">Propriedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="43a51-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="43a51-141">Sessão de mídia do PMP</span><span class="sxs-lookup"><span data-stu-id="43a51-141">PMP Media Session</span></span>](pmp-media-session.md)
</dt> <dt>

[<span data-ttu-id="43a51-142">Caminho de mídia protegido</span><span class="sxs-lookup"><span data-stu-id="43a51-142">Protected Media Path</span></span>](protected-media-path.md)
</dt> <dt>

[<span data-ttu-id="43a51-143">Resolvedor de origem</span><span class="sxs-lookup"><span data-stu-id="43a51-143">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 
