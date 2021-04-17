---
description: Especifica os deslocamentos para os limites de carga em um quadro para exemplos protegidos.
ms.assetid: 8aa25afd-efa8-4fe0-92d4-8432f9d633c9
title: Atributo MFSampleExtension_PacketCrossOffsets (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d416f41fef9caab3d73c2bdd015d345452ccbd69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808353"
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

Esse atributo se aplica a amostras de mídia protegidas pelo Windows Media Digital Rights Management (DRM). O valor do atributo é uma matriz de **DWORD** s. Cada entrada na matriz é o deslocamento de um limite de carga, em relação ao início do quadro. Um aplicativo pode usar esses valores ao descriptografar e reconstruir os quadros.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Wmcontainer. h</dt> </dl> |



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

 

 




