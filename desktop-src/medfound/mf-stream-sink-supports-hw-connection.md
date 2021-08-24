---
description: Indica se um sink de mídia dá suporte ao fluxo de dados de hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9f663c492e5ae15590cc9240762e90298122790fa350fae51d09dd1199f6d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714367"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>O MF \_ STREAM SINK DÁ SUPORTE ao atributo DE CONEXÃO \_ \_ \_ \_ HW

Indica se um sink de mídia dá suporte ao fluxo de dados de hardware.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo é usado quando um sink de mídia proxies um dispositivo de hardware e é capaz de receber dados em um barramento de hardware. Por exemplo, um decodificador de áudio de hardware pode enviar dados de áudio diretamente para o hardware de renderização de áudio.

Nesse cenário, o decodificador e o sink ainda são [](media-foundation-transforms.md) representados no Microsoft Media Foundation por uma transformação Media Foundation (MFT) e um sink de mídia. No entanto, nenhum fluxo de dados entre esses dois objetos na camada de pipeline, somente na camada de hardware, conforme mostrado no diagrama a seguir.

![um diagrama que mostra uma fonte de proxy de hardware.](images/proxy-mft4.png)

A conexão entre o MFT e o sink de mídia é negociada da seguinte forma.

1.  O pipeline verifica se o MFT é um proxy de hardware, verificando o atributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) no MFT. Para obter detalhes, consulte [Hardware MFTs](hardware-mfts.md).
2.  O pipeline obtém um ponteiro para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) do sink de fluxo no sink de mídia.
3.  O pipeline usa o [**ponteiro IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) para consultar o atributo MF \_ STREAM SINK SUPPORTS \_ \_ \_ HW \_ CONNECTION. Se esse atributo estiver presente e for igual a **TRUE,** a fonte de mídia será compatível com conexões de hardware.
4.  O pipeline define o [atributo MFT \_ CONNECTED STREAM \_ \_ ATTRIBUTE](mft-connected-stream-attribute.md) no sink de fluxo. O valor desse atributo é o [**ponteiro IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) do MFT.
5.  O pipeline define o [atributo MFT \_ CONNECTED TO \_ \_ HW \_ STREAM](mft-connected-to-hw-stream.md) **como TRUE** no sink do fluxo e no MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




