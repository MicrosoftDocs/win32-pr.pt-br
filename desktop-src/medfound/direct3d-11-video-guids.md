---
description: Os GUIDs a seguir dão suporte a APIs de vídeo do Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUIDs de vídeo do Direct3D 11 (D3d11. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d97a43285a59cf5196584b9be04fc36b02e5243f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010315"
---
# <a name="direct3d-11-video-guids"></a><span data-ttu-id="e08e3-103">GUIDs de vídeo do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e08e3-103">Direct3D 11 Video GUIDs</span></span>

<span data-ttu-id="e08e3-104">Os GUIDs a seguir dão suporte a APIs de vídeo do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e08e3-104">The following GUIDs support Direct3D 11 Video APIs.</span></span>

<dl> <dt>

<span data-ttu-id="e08e3-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Proteção de \_ HW de troca de chave D3D11 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e08e3-105"><span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e08e3-106">Indica que o decodificador receberá dados de um componente DRM baseado em hardware</span><span class="sxs-lookup"><span data-stu-id="e08e3-106">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="e08e3-107">**D3D11 \_ A \_ \_ \_ proteção de HW de troca de chave** pode ser especificada no parâmetro *pKeyExchangeType* da função [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para indicar que a interface [**ID3D11CRYPTOSESSION**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) será usada apenas para comunicação entre um componente DRM do modo de usuário e o ambiente de execução seguro.</span><span class="sxs-lookup"><span data-stu-id="e08e3-107">**D3D11\_KEY\_EXCHANGE\_HW\_PROTECTION** can be specified in the *pKeyExchangeType* parameter of the [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) function to indicate that the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) interface will be used purely for communication between a user mode DRM component and the secure execution environment.</span></span>

<span data-ttu-id="e08e3-108">Quando esse GUID é especificado, os seguintes métodos não devem ser chamados:</span><span class="sxs-lookup"><span data-stu-id="e08e3-108">When this GUID is specified, the following methods should not be called:</span></span>

-   [<span data-ttu-id="e08e3-109">**ID3D11CryptoSession:: getcertificate**</span><span class="sxs-lookup"><span data-stu-id="e08e3-109">**ID3D11CryptoSession::GetCertificateSize**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [<span data-ttu-id="e08e3-110">**ID3D11CryptoSession:: getcertificate**</span><span class="sxs-lookup"><span data-stu-id="e08e3-110">**ID3D11CryptoSession::GetCertificate**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [<span data-ttu-id="e08e3-111">**ID3D11VideoContext::EncryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="e08e3-111">**ID3D11VideoContext::EncryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [<span data-ttu-id="e08e3-112">**ID3D11VideoContext::D ecryptionBlt**</span><span class="sxs-lookup"><span data-stu-id="e08e3-112">**ID3D11VideoContext::DecryptionBlt**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [<span data-ttu-id="e08e3-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="e08e3-113">**ID3D11VideoContext::StartSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [<span data-ttu-id="e08e3-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span><span class="sxs-lookup"><span data-stu-id="e08e3-114">**ID3D11VideoContext::FinishSessionKeyRefresh**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [<span data-ttu-id="e08e3-115">**ID3D11VideoContext::GetEncryptionBltKey**</span><span class="sxs-lookup"><span data-stu-id="e08e3-115">**ID3D11VideoContext::GetEncryptionBltKey**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span data-ttu-id="e08e3-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 de \_ hardware de criptografia do decodificador do \_ \_ \_ Cenc**</span><span class="sxs-lookup"><span data-stu-id="e08e3-116"><span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11\_DECODER\_ENCRYPTION\_HW\_CENC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e08e3-117">Indica que o decodificador receberá dados de um componente DRM baseado em hardware</span><span class="sxs-lookup"><span data-stu-id="e08e3-117">Indicates that the decoder will receive data from a hardware-based DRM component</span></span>

<span data-ttu-id="e08e3-118">Definir esse GUID no membro **guidConfigBitstreamEncryption** da estrutura de [**\_ \_ \_ configuração do decodificador de vídeo D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passado para a API [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica que os seguintes parâmetros serão passados na chamada [**ID3D11VideoDevice::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :</span><span class="sxs-lookup"><span data-stu-id="e08e3-118">Setting this GUID in the **guidConfigBitstreamEncryption** member of the [**D3D11\_VIDEO\_DECODER\_CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) structure passed to the [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indicates that the following parameters will be passed in the [**ID3D11VideoDevice::DecoderBeginFrame**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) call:</span></span>



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08e3-119">*ContentKeySize*</span><span class="sxs-lookup"><span data-stu-id="e08e3-119">*ContentKeySize*</span></span> | <span data-ttu-id="e08e3-120">Contém o tamanho do [**\_ decodificador de vídeo D3D11 iniciar estrutura de \_ \_ sessão de \_ \_ criptografia \_ do quadro**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .</span><span class="sxs-lookup"><span data-stu-id="e08e3-120">Contains the size of the [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) structure.</span></span>                                                                                                  |
| <span data-ttu-id="e08e3-121">*pContentKey*</span><span class="sxs-lookup"><span data-stu-id="e08e3-121">*pContentKey*</span></span>    | <span data-ttu-id="e08e3-122">Um ponteiro para um [**\_ \_ decodificador de vídeo D3D11 \_ começa a \_ \_ \_ sessão de criptografia de quadro**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) fornecendo o [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e as informações de chave necessárias para descriptografar o quadro.</span><span class="sxs-lookup"><span data-stu-id="e08e3-122">A pointer to a [**D3D11\_VIDEO\_DECODER\_BEGIN\_FRAME\_CRYPTO\_SESSION**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) providing the [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) and the key information needed to decrypt the frame.</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e08e3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08e3-123">Requirements</span></span>



| <span data-ttu-id="e08e3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08e3-124">Requirement</span></span> | <span data-ttu-id="e08e3-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e08e3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e08e3-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e08e3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e08e3-127">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e08e3-127">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e08e3-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e08e3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e08e3-129">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e08e3-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e08e3-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e08e3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08e3-131"><dt>D3d11. h</dt></span><span class="sxs-lookup"><span data-stu-id="e08e3-131"><dt>D3d11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e08e3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e08e3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08e3-133">APIs de vídeo do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e08e3-133">Direct3D 11 Video APIs</span></span>](direct3d-11-video-apis.md)
</dt> </dl>

 

 




