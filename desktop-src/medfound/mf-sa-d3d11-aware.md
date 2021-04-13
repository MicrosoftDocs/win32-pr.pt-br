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
# <a name="mf_sa_d3d11_aware-attribute"></a>\_Atributo de \_ reconhecimento de D3D11 do MF SA \_

Especifica se uma Media Foundation de transformação (MFT) dá suporte ao Microsoft Direct3D 11.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica somente a MFTs de vídeo. Para consultar esse atributo, chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obter o repositório de atributos de MFT. Se **GetAttributes** tiver sucesso, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Se o atributo for diferente de zero, o cliente poderá dar ao MFT um ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) antes de o streaming começar. Para fazer isso, o cliente envia a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md) O cliente não é necessário para enviar esta mensagem.
-   Se esse atributo for zero (**false**), o MFT não oferecerá suporte a Direct3D 11 e o cliente não deverá enviar a mensagem do Gerenciador de D3D do conjunto de mensagens do MFT para o MFT. [**\_ \_ \_ \_**](mft-message-set-d3d-manager.md)

O valor padrão desse atributo é **false**. Trate este atributo como somente leitura. Não altere o valor; o MFT ignorará as alterações no valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Dando suporte à decodificação de vídeo do Direct3D 11 no Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




