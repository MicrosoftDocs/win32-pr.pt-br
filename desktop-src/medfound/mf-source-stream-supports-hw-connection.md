---
description: Indica se uma fonte de mídia dá suporte ao fluxo de dados de hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Atributo MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659672b11cbcaa51f543eec8239f56ba792584a4b1ac44af25ed76016cdeb2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955137"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>O \_ fluxo de origem MF \_ \_ dá suporte ao \_ atributo de \_ conexão HW

Indica se uma fonte de mídia dá suporte ao fluxo de dados de hardware.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo é usado quando um proxy de origem de mídia um dispositivo de hardware e é capaz de transferir dados downstream em um barramento de hardware, sem enviar dados para a CPU. Por exemplo, uma webcam pode entregar o vídeo codificado por H. 264 diretamente a um decodificador de hardware integrado.

Nesse cenário, a origem e o decodificador ainda são representados no Microsoft Media Foundation por um objeto de [origem de mídia](media-sources.md) e uma [Media Foundation transformação](media-foundation-transforms.md) (MFT). No entanto, nenhum fluxo de dados entre esses dois objetos na camada de pipeline, somente na camada de hardware, conforme mostrado no diagrama a seguir.

![um diagrama que mostra uma origem de proxy de hardware.](images/proxy-mft3.png)

A conexão entre a origem de mídia e a MFT é negociada da seguinte maneira.

1.  O pipeline consulta a origem de mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) . (Essa interface é opcional para que as fontes de mídia ofereçam suporte.)
2.  O pipeline chama [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  As consultas de pipeline para o \_ fluxo de origem MF \_ \_ dão suporte ao \_ atributo de \_ conexão HW. Se o atributo estiver presente e for igual a **true**, a fonte de mídia dará suporte a conexões de hardware.
4.  O pipeline verifica se o MFT também é um proxy de hardware, verificando o atributo de [ \_ \_ \_ \_ atributo URL de hardware de enumeração de MFT](mft-enum-hardware-url-attribute.md) no MFT. Para obter detalhes, consulte [hardware MFTs](hardware-mfts.md).
5.  O pipeline define o atributo de [ \_ atributo de \_ fluxo \_ do MFT conectado](mft-connected-stream-attribute.md) na MFT. O valor desse atributo é o ponteiro [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtido da origem de mídia na etapa 2.
6.  O pipeline define o [MFT \_ conectado \_ ao \_ \_](mft-connected-to-hw-stream.md) atributo de fluxo de HW como **true** na origem da mídia e no MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> </dl>

 

 




