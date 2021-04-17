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
# <a name="mft_message_set_d3d_manager"></a>Conjunto de mensagens do MFT \_ \_ \_ Gerenciador de D3D \_

Define ou limpa o [Gerenciador de dispositivos Direct3D](direct3d-device-manager.md) para o DirectX Video ACCERERATION (DXVA).

## <a name="message-parameter"></a>Parâmetro de mensagem

Quando o streaming começa, o parâmetro *ulParam* contém um ponteiro **IUnknown** . O MFT consultará esse ponteiro para a interface [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) para Direct3D 9 e a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) para Direct3D 11. Quando o streaming é interrompido, o *ulParameter* contém o valor **NULL**.

## <a name="remarks"></a>Comentários

Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).

Esta mensagem se aplica somente a transformações de vídeo. O cliente não deve enviar essa mensagem, a menos que o MFT retorne **verdadeiro** para o atributo de [**reconhecimento de \_ D3D da SA \_ \_ MF**](mf-sa-d3d-aware-attribute.md) ([MF \_ SA \_ D3D11 \_ ciente](mf-sa-d3d11-aware.md) para o Direct3D 11).

Não envie essa mensagem para um MFT com vários saídas.

### <a name="implementation"></a>Implementação

Um MFT deve dar suporte a essa mensagem somente se o MFT usar a aceleração de vídeo do DirectX para processamento ou decodificação de vídeo.

Se uma MFT oferecer suporte a essa mensagem, ela também deverá implementar o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) e retornar o valor **true** para o atributo de [**reconhecimento de \_ D3D da SA \_ \_ MF**](mf-sa-d3d-aware-attribute.md) (([MF \_ SA \_ D3D11 \_ ciente](mf-sa-d3d11-aware.md) para o Direct3D 11). Esse atributo informa ao cliente que o cliente deve enviar a mensagem do **\_ Gerenciador de \_ \_ D3D \_ do conjunto de mensagens do MFT** para o MFT antes do início do streaming.

Se uma MFT não oferecer suporte a essa mensagem, ela deverá retornar **E \_ NOTIMPL** de [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage). Essa é uma exceção à regra geral de que uma MFT pode retornar **S \_ OK** de qualquer mensagem que ignorar.

Para obter mais informações, consulte [MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md)
</dt> <dt>

[Suporte a DXVA 2,0 no Media Foundation](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[Dando suporte à decodificação de vídeo do Direct3D 11 no Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**\_tipo de mensagem MFT \_**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




