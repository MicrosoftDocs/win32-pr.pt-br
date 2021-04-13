---
description: Especifica se uma Media Foundation de transformação (MFT) dá suporte ao Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: Atributo MF_SA_D3D11_AWARE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296484"
---
# <a name="mf_sa_d3d11_aware-attribute"></a><span data-ttu-id="62ba1-103">\_Atributo de \_ reconhecimento de D3D11 do MF SA \_</span><span class="sxs-lookup"><span data-stu-id="62ba1-103">MF\_SA\_D3D11\_AWARE attribute</span></span>

<span data-ttu-id="62ba1-104">Especifica se uma Media Foundation de transformação (MFT) dá suporte ao Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="62ba1-104">Specifies whether a Media Foundation transform (MFT) supports Microsoft Direct3D 11.</span></span>

## <a name="data-type"></a><span data-ttu-id="62ba1-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="62ba1-105">Data type</span></span>

<span data-ttu-id="62ba1-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="62ba1-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="62ba1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="62ba1-107">Remarks</span></span>

<span data-ttu-id="62ba1-108">Esse atributo se aplica somente a MFTs de vídeo.</span><span class="sxs-lookup"><span data-stu-id="62ba1-108">This attribute applies only to video MFTs.</span></span> <span data-ttu-id="62ba1-109">Para consultar esse atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributos de MFT.</span><span class="sxs-lookup"><span data-stu-id="62ba1-109">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT attribute store.</span></span> <span data-ttu-id="62ba1-110">Se **GetAttributes** tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="62ba1-110">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

-   <span data-ttu-id="62ba1-111">Se o atributo for diferente de zero, o cliente poderá dar ao MFT um ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="62ba1-111">If the attribute is nonzero, the client can give the MFT a pointer to the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface before streaming starts.</span></span> <span data-ttu-id="62ba1-112">Para fazer isso, o cliente envia a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)</span><span class="sxs-lookup"><span data-stu-id="62ba1-112">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="62ba1-113">O cliente não é necessário para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="62ba1-113">The client is not required to send this message.</span></span>
-   <span data-ttu-id="62ba1-114">Se esse atributo for zero (**false**), o MFT não oferecerá suporte a Direct3D 11 e o cliente não deverá enviar a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)</span><span class="sxs-lookup"><span data-stu-id="62ba1-114">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 11, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="62ba1-115">O valor padrão desse atributo é **false**.</span><span class="sxs-lookup"><span data-stu-id="62ba1-115">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="62ba1-116">Trate este atributo como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="62ba1-116">Treat this attribute as read-only.</span></span> <span data-ttu-id="62ba1-117">Não altere o valor; o MFT ignorará as alterações no valor.</span><span class="sxs-lookup"><span data-stu-id="62ba1-117">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ba1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62ba1-118">Requirements</span></span>



| <span data-ttu-id="62ba1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ba1-119">Requirement</span></span> | <span data-ttu-id="62ba1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="62ba1-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ba1-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62ba1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="62ba1-122">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="62ba1-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="62ba1-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62ba1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="62ba1-124">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="62ba1-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="62ba1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62ba1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ba1-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="62ba1-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ba1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="62ba1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ba1-128">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62ba1-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="62ba1-129">Dando suporte à decodificação de vídeo do Direct3D 11 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="62ba1-129">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




