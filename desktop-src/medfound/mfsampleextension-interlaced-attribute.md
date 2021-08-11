---
description: Indica se um quadro de vídeo é entrelaçado ou progressivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: MFSampleExtension_Interlaced atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36d928d42fc2399536d5beee4f4af87cbacaa82171048ad191a4e9fc7ef3e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240643"
---
# <a name="mfsampleextension_interlaced-attribute"></a>Atributo entrelaçado MFSampleExtension \_

Indica se um quadro de vídeo é entrelaçado ou progressivo. Se **TRUE**, o quadro será entrelaçado. Se **FALSE**, o quadro será progressivo. Se não estiver definido, o tipo de mídia descreverá o entrelaçamento. Esse atributo se aplica a exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Para conteúdo de vídeo que contém quadros progressivos e entrelaçados mistos, de definido o tipo de mídia como entrelaçado e use esse atributo em cada quadro para indicar se o quadro é progressivo ou entrelaçado.

Para o conteúdo de vídeo totalmente entrelaçado, de definir o tipo de mídia como entrelaçado e omitir esse atributo ou defini-lo como **TRUE** em cada exemplo.

Para conteúdo de vídeo totalmente progressivo, de definido o tipo de mídia como progressivo e omiti-lo ou defini-lo como **FALSE** em cada exemplo.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Exemplos de mídia](media-samples.md)
</dt> <dt>

[Entrelaçamento de vídeo](video-interlacing.md)
</dt> </dl>

 

 




