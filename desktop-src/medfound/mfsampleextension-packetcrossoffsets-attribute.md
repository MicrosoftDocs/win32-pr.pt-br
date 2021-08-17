---
description: Especifica os deslocamentos para os limites de carga em um quadro para exemplos protegidos.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Atributo MFSampleExtension_PacketCrossOffsets (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39abdcaf0dfb5888c1705a0a76a19c3a55be522b82405f5a77345efe0d8f13e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119102302"
---
# <a name="mfsampleextension_packetcrossoffsets-attribute"></a>\_Atributo MFSampleExtension PacketCrossOffsets

Especifica os deslocamentos para os limites de carga em um quadro para exemplos protegidos.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para definir esse atributo, chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

esse atributo se aplica a amostras de mídia protegidas pelo DRM (Rights Management Digital Windows media). O valor do atributo é uma matriz de **DWORD** s. Cada entrada na matriz é o deslocamento de um limite de carga, em relação ao início do quadro. Um aplicativo pode usar esses valores ao descriptografar e reconstruir os quadros.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Divisor de ASF](asf-splitter.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> </dl>

 

 




