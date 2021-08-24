---
description: Especifica se uma Media Foundation de transformação baseada em hardware (MFT) está conectada a outra MFT baseada em hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Atributo MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ff2a2dea2fcb67cff776ba02c43193b571a382df57a5d0562f3f2cd1fb7248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602866"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ conectado \_ ao \_ atributo de fluxo de HW \_

Especifica se uma Media Foundation de transformação baseada em hardware (MFT) está conectada a outra MFT baseada em hardware.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos não usam esse atributo.

Esse atributo é usado com MFTs com base em hardware. Quando dois MFTs de hardware são conectados em uma topologia, o carregador de topologia define esse atributo como **true** nos seguintes objetos:

-   O fluxo de saída do MFT de upstream
-   O fluxo de entrada do MFT downstream

Para obter o repositório de atributos para o fluxo de saída, o carregador de topologia chama [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) no MFT upstream. Para obter o repositório de atributos para o fluxo de entrada, o carregador de topologia chama [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) no MFT downstream.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




