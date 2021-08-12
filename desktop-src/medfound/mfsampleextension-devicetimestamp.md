---
description: Contém o carimbo de data/hora do driver de dispositivo.
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: Atributo MFSampleExtension_DeviceTimestamp (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3322f295908ae2bbdc095a21ab57ee2e0f2ed10dd2267eaea227b9248ddc226b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241121"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>\_Atributo MFSampleExtension DeviceTimestamp

Contém o carimbo de data/hora do driver de dispositivo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Esse atributo é definido em amostras de mídia criadas por uma fonte de mídia para um dispositivo de captura. O valor desse atributo está no domínio [**MFTIME**](mftime.md) , compartilhando uma época com tempo de QPC (contador de desempenho de consulta) e sempre expresso em unidades de 100ns. Esse atributo está disponível para MFTs inserido no pipeline de captura.

Para obter o carimbo de data/hora em relação ao início do streaming, chame o método [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) .

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo no Media Foundation](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> </dl>

 

 




