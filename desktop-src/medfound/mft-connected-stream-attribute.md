---
description: Contém um ponteiro para os atributos de fluxo do fluxo conectado em um MFT (Media Foundation baseado em hardware).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Atributo MFT_CONNECTED_STREAM_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827811"
---
# <a name="mft_connected_stream_attribute-attribute"></a>\_Atributo de \_ atributo de fluxo conectado ao MFT \_

Contém um ponteiro para os atributos de fluxo do fluxo conectado em um MFT (Media Foundation baseado em hardware).

## <a name="data-type"></a>Tipo de dados

**IMFAttributes \** _ armazenado como _*IUnknown \**_

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

Normalmente, os aplicativos não usam esse atributo.

Esse atributo é usado para MFTs que atuam como proxies para um dispositivo de hardware. Para obter detalhes, consulte [hardware MFTs](hardware-mfts.md).

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

[MFT \_ conectado \_ ao \_ fluxo de HW \_](mft-connected-to-hw-stream.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




