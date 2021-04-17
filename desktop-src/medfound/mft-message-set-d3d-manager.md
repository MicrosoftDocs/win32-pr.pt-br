---
description: Define ou limpa o Gerenciador de Dispositivos Direct3D para o DirectX Video Accereration (DXVA).
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: MFT_MESSAGE_SET_D3D_MANAGER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791616"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="c5cdc-103">Conjunto de mensagens do MFT \_ \_ \_ Gerenciador de D3D \_</span><span class="sxs-lookup"><span data-stu-id="c5cdc-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="c5cdc-104">Define ou limpa o [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md) para o DirectX Video ACCERERATION (DXVA).</span><span class="sxs-lookup"><span data-stu-id="c5cdc-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="c5cdc-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="c5cdc-105">Message Parameter</span></span>

<span data-ttu-id="c5cdc-106">Quando o streaming começa, o parâmetro *ulParam* contém um ponteiro **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="c5cdc-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="c5cdc-107">O MFT consultará esse ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) para Direct3D 9 e a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) para Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="c5cdc-108">Quando o streaming é interrompido, o *ulParameter* contém o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5cdc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5cdc-109">Remarks</span></span>

<span data-ttu-id="c5cdc-110">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="c5cdc-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="c5cdc-111">Esta mensagem se aplica somente a transformações de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-111">This message applies only to video transforms.</span></span> <span data-ttu-id="c5cdc-112">O cliente não deve enviar essa mensagem, a menos que o MFT retorne **verdadeiro** para o atributo de [**reconhecimento de \_ D3D da SA \_ \_ MF**](mf-sa-d3d-aware-attribute.md) ([MF \_ SA \_ D3D11 \_ ciente](mf-sa-d3d11-aware.md) para o Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="c5cdc-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="c5cdc-113">Não envie essa mensagem para um MFT com vários saídas.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="c5cdc-114">Implementação</span><span class="sxs-lookup"><span data-stu-id="c5cdc-114">Implementation</span></span>

<span data-ttu-id="c5cdc-115">Um MFT deve dar suporte a essa mensagem somente se o MFT usar a aceleração de vídeo do DirectX para processamento ou decodificação de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="c5cdc-116">Se uma MFT oferecer suporte a essa mensagem, ela também deverá implementar o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) e retornar o valor **true** para o atributo de [**reconhecimento de \_ D3D da SA \_ \_ MF**](mf-sa-d3d-aware-attribute.md) (([MF \_ SA \_ D3D11 \_ ciente](mf-sa-d3d11-aware.md) para o Direct3D 11).</span><span class="sxs-lookup"><span data-stu-id="c5cdc-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="c5cdc-117">Esse atributo informa ao cliente que o cliente deve enviar a mensagem do **\_ Gerenciador de \_ \_ D3D \_ do conjunto de mensagens do MFT** para o MFT antes do início do streaming.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="c5cdc-118">Se uma MFT não oferecer suporte a essa mensagem, ela deverá retornar **E \_ NOTIMPL** de [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="c5cdc-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="c5cdc-119">Essa é uma exceção à regra geral de que uma MFT pode retornar **S \_ OK** de qualquer mensagem que ignorar.</span><span class="sxs-lookup"><span data-stu-id="c5cdc-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="c5cdc-120">Para obter mais informações, consulte [MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="c5cdc-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5cdc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5cdc-121">Requirements</span></span>



| <span data-ttu-id="c5cdc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5cdc-122">Requirement</span></span> | <span data-ttu-id="c5cdc-123">Valor</span><span class="sxs-lookup"><span data-stu-id="c5cdc-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5cdc-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5cdc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c5cdc-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5cdc-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5cdc-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5cdc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c5cdc-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5cdc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c5cdc-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5cdc-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5cdc-129"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5cdc-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5cdc-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5cdc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5cdc-131">MFTs com reconhecimento de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c5cdc-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="c5cdc-132">Suporte a DXVA 2,0 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5cdc-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c5cdc-133">Dando suporte à decodificação de vídeo do Direct3D 11 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5cdc-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="c5cdc-134">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="c5cdc-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




