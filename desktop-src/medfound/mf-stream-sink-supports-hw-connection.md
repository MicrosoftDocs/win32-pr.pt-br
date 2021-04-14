---
description: Indica se um coletor de mídia dá suporte ao fluxo de dados de hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Atributo MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461181"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>O \_ coletor de fluxo MF \_ \_ dá suporte ao \_ atributo de \_ conexão HW

Indica se um coletor de mídia dá suporte ao fluxo de dados de hardware.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo é usado quando um coletor de mídia proxies de um dispositivo de hardware e é capaz de receber dados em um barramento de hardware. Por exemplo, um decodificador de áudio de hardware pode enviar dados de áudio diretamente para o hardware de renderização de áudio.

Nesse cenário, o decodificador e o coletor ainda são representados no Microsoft Media Foundation por uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) e um coletor de mídia. No entanto, nenhum fluxo de dados entre esses dois objetos na camada de pipeline, somente na camada de hardware, conforme mostrado no diagrama a seguir.

![um diagrama que mostra uma origem de proxy de hardware.](images/proxy-mft4.png)

A conexão entre o MFT e o coletor de mídia é negociada da seguinte maneira.

1.  O pipeline verifica se o MFT é um proxy de hardware, verificando o atributo de [ \_ \_ \_ \_ atributo URL de hardware de enumeração de MFT](mft-enum-hardware-url-attribute.md) no MFT. Para obter detalhes, consulte [hardware MFTs](hardware-mfts.md).
2.  O pipeline Obtém um ponteiro para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) do coletor de fluxo no coletor de mídia.
3.  O pipeline usa o ponteiro [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) para consultar o coletor de \_ fluxo MF que \_ \_ dá suporte ao \_ atributo de conexão HW \_ . Se esse atributo estiver presente e for igual a **true**, a fonte de mídia dará suporte a conexões de hardware.
4.  O pipeline define o atributo de [ \_ atributo de \_ fluxo \_ do MFT conectado](mft-connected-stream-attribute.md) no coletor de fluxo. O valor desse atributo é o ponteiro [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do MFT.
5.  O pipeline define o [MFT \_ conectado \_ ao \_ \_](mft-connected-to-hw-stream.md) atributo de fluxo de HW como **true** no coletor de fluxo e no MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




