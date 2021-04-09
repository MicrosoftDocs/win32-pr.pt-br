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
# <a name="direct3d-11-video-guids"></a>GUIDs de vídeo do Direct3D 11

Os GUIDs a seguir dão suporte a APIs de vídeo do Direct3D 11.

<dl> <dt>

<span id="D3D11_KEY_EXCHANGE_HW_PROTECTION"></span><span id="d3d11_key_exchange_hw_protection"></span>**\_Proteção de \_ HW de troca de chave D3D11 \_ \_**
</dt> <dd> <dl> <dt>



Indica que o decodificador receberá dados de um componente DRM baseado em hardware

**D3D11 \_ A \_ \_ \_ proteção de HW de troca de chave** pode ser especificada no parâmetro *pKeyExchangeType* da função [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para indicar que a interface [**ID3D11CRYPTOSESSION**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) será usada apenas para comunicação entre um componente DRM do modo de usuário e o ambiente de execução seguro.

Quando esse GUID é especificado, os seguintes métodos não devem ser chamados:

-   [**ID3D11CryptoSession:: getcertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize)
-   [**ID3D11CryptoSession:: getcertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate)
-   [**ID3D11VideoContext::EncryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-encryptionblt)
-   [**ID3D11VideoContext::D ecryptionBlt**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decryptionblt)
-   [**ID3D11VideoContext::StartSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-startsessionkeyrefresh)
-   [**ID3D11VideoContext::FinishSessionKeyRefresh**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-finishsessionkeyrefresh)
-   [**ID3D11VideoContext::GetEncryptionBltKey**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getencryptionbltkey)


</dt> </dl> </dd> <dt>

<span id="D3D11_DECODER_ENCRYPTION_HW_CENC"></span><span id="d3d11_decoder_encryption_hw_cenc"></span>**D3D11 de \_ hardware de criptografia do decodificador do \_ \_ \_ Cenc**
</dt> <dd> <dl> <dt>



Indica que o decodificador receberá dados de um componente DRM baseado em hardware

Definir esse GUID no membro **guidConfigBitstreamEncryption** da estrutura de [**\_ \_ \_ configuração do decodificador de vídeo D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config) passado para a API [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder) indica que os seguintes parâmetros serão passados na chamada [**ID3D11VideoDevice::D ecoderbeginframe**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe) :



|                  |                                                                                                                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ContentKeySize* | Contém o tamanho do [**\_ decodificador de vídeo D3D11 iniciar estrutura de \_ \_ sessão de \_ \_ criptografia \_ do quadro**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) .                                                                                                  |
| *pContentKey*    | Um ponteiro para um [**\_ \_ decodificador de vídeo D3D11 \_ começa a \_ \_ \_ sessão de criptografia de quadro**](/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_decoder_begin_frame_crypto_session) fornecendo o [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) e as informações de chave necessárias para descriptografar o quadro. |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>D3d11. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[APIs de vídeo do Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 




