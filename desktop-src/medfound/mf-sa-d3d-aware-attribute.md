---
description: Especifica se uma Media Foundation transformação (MFT) dá suporte a DXVA (aceleração de vídeo do DirectX). Esse atributo se aplica somente a MFTs de vídeo.
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: Atributo MF_SA_D3D_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762441"
---
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="8a314-104">\_Atributo de \_ reconhecimento de D3D SA do MF \_</span><span class="sxs-lookup"><span data-stu-id="8a314-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="8a314-105">Especifica se uma Media Foundation transformação (MFT) dá suporte a DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="8a314-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="8a314-106">Esse atributo se aplica somente a MFTs de vídeo.</span><span class="sxs-lookup"><span data-stu-id="8a314-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="8a314-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8a314-107">Data type</span></span>

<span data-ttu-id="8a314-108">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8a314-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="8a314-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a314-109">Remarks</span></span>

<span data-ttu-id="8a314-110">Para consultar esse atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributo global do MFT.</span><span class="sxs-lookup"><span data-stu-id="8a314-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="8a314-111">Se **GetAttributes** tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8a314-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8a314-112">Esse atributo informa ao cliente se o MFT pode usar o vídeo do Direct3D 9:</span><span class="sxs-lookup"><span data-stu-id="8a314-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="8a314-113">Se o atributo for diferente de zero, o cliente poderá dar ao MFT um ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="8a314-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="8a314-114">Para fazer isso, o cliente envia a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)</span><span class="sxs-lookup"><span data-stu-id="8a314-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="8a314-115">O cliente não é necessário para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8a314-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="8a314-116">Se esse atributo for zero (**false**), o MFT não oferecerá suporte ao vídeo do Direct3D 9 e o cliente não deverá enviar a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)</span><span class="sxs-lookup"><span data-stu-id="8a314-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="8a314-117">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="8a314-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="8a314-118">Trate este atributo como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a314-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="8a314-119">Não altere o valor; o MFT ignorará as alterações no valor.</span><span class="sxs-lookup"><span data-stu-id="8a314-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="8a314-120">Para obter mais informações sobre como implementar esse atributo em uma MFT personalizada, consulte [MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="8a314-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="8a314-121">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8a314-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="8a314-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a314-122">Examples</span></span>

<span data-ttu-id="8a314-123">O código a seguir testa se uma MFT dá suporte a DXVA.</span><span class="sxs-lookup"><span data-stu-id="8a314-123">The following code tests whether an MFT supports DXVA.</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a><span data-ttu-id="8a314-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a314-124">Requirements</span></span>



| <span data-ttu-id="8a314-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a314-125">Requirement</span></span> | <span data-ttu-id="8a314-126">Valor</span><span class="sxs-lookup"><span data-stu-id="8a314-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a314-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a314-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8a314-128">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="8a314-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="8a314-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a314-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8a314-130">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8a314-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="8a314-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a314-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a314-132"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a314-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a314-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a314-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a314-134">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a314-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a314-135">MFTs com reconhecimento de Direct3D</span><span class="sxs-lookup"><span data-stu-id="8a314-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="8a314-136">Suporte a DXVA 2,0 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a314-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="8a314-137">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8a314-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="8a314-138">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="8a314-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="8a314-139">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="8a314-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="8a314-140">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="8a314-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="8a314-141">\_modo de \_ DXVA da topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="8a314-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




