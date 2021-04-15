---
description: Especifica se uma Media Foundation de transformação baseada em hardware (MFT) está conectada a outra MFT baseada em hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Atributo MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753879"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




