---
description: Contém um ponteiro para os atributos de fluxo do fluxo conectado em uma MFT (transformação Media Foundation hardware).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2289b8f1e8d5d751f7aa69564b8bbd26d865b43efedb474529147385b1851bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722562"
---
# <a name="mft_connected_stream_attribute-attribute"></a>Atributo MFT \_ CONNECTED \_ STREAM \_ ATTRIBUTE

Contém um ponteiro para os atributos de fluxo do fluxo conectado em uma MFT (transformação Media Foundation hardware).

## <a name="data-type"></a>Tipo de dados

**IMFAttributes \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos não usam esse atributo.

Esse atributo é usado para MFTs que atuam como proxies para um dispositivo de hardware. Para obter detalhes, consulte [Hardware MFTs](hardware-mfts.md).

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos UWP da área \| de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT \_ CONECTADO AO FLUXO \_ \_ \_ HW](mft-connected-to-hw-stream.md)
</dt> <dt>

[Hardware MFTs](hardware-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




