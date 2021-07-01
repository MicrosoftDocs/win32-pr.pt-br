---
description: Os GUIDs a seguir são suportados por APIs de vídeo do Direct3D 11.
ms.assetid: CF2F3058-328A-4128-B5C6-29723B49AB1E
title: GUIDs de vídeo do Direct3D 11 (D3d11.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16f5277123c3d174427debc3f0ad5e184e49a6c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118631"
---
# <a name="direct3d-11-video-guids"></a>GUIDs de vídeo do Direct3D 11

Os GUIDs a seguir são suportados por APIs de vídeo do Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION**
</dt> <dd> <dl> <dt>



Indica que o decodificador receberá dados de um componente DRM baseado em hardware

**D3D11 \_ KEY \_ EXCHANGE \_ HW \_ PROTECTION** pode ser especificado no parâmetro *pKeyExchangeType* da função [**ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para indicar que a interface [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) será usada puramente para comunicação entre um componente DRM no modo de usuário e o ambiente de execução segura.

Quando esse GUID é especificado, os seguintes métodos não devem ser chamados:

-   [**ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 \_ DECODER \_ ENCRYPTION \_ HW \_ CENC**
</dt> <dd> <dl> <dt>



Indica que o decodificador receberá dados de um componente DRM baseado em hardware

Definir esse GUID no membro **guidConfigBitstreamEncryption** da estrutura [**D3D11 \_ VIDEO \_ DECODER \_ CONFIG**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passado para a [**ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) API indica que os seguintes parâmetros serão passados na chamada [**ID3D11VideoDevice::D ecoderBeginFrame:**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe)



| Valor                 | Descrição                                                                                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contém o tamanho da estrutura [**D3D11 \_ VIDEO \_ DECODER \_ BEGIN FRAME CRYPTO \_ \_ \_ SESSION.**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session)                                                                                                  |
| *pContentKey*    | Um ponteiro para uma SESSÃO DE CRIPTOGRAFIA BEGIN FRAME DO [**\_ \_ DECODIFICADOR \_ \_ \_ \_ DE VÍDEO D3D11**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) que fornece a [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e as informações de chave necessárias para descriptografar o quadro. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Somente aplicativos da área de trabalho do Windows Server 2016 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>D3d11.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




