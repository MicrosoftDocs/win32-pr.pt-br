---
description: Especifica se uma transformação Media Foundation (MFT) dá suporte ao Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59a996493ace387d1c6e93c734110772274986c6e5490b9e0e08567024d47c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955396"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>Atributo MF \_ SA \_ D3D11 \_ AWARE

Especifica se uma transformação Media Foundation (MFT) dá suporte ao Microsoft Direct3D 11.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica somente a MFTs de vídeo. Para consultar esse atributo, chame [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o armazenamento de atributos MFT. Se **GetAttributes for** bem-sucedido, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Se o atributo for diferente de zero, o cliente poderá dar ao MFT um ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) antes do início do streaming. Para fazer isso, o cliente envia a [**mensagem MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) para o MFT. O cliente não é necessário para enviar essa mensagem.
-   Se esse atributo for zero (**FALSE),** o MFT não dá suporte ao Direct3D 11 e o cliente não deve enviar a mensagem [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) para o MFT.

O valor padrão desse atributo é **FALSE.** Trate esse atributo como somente leitura. Não altere o valor; O MFT ignorará as alterações no valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Suporte à decodificação de vídeo do Direct3D 11 Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




