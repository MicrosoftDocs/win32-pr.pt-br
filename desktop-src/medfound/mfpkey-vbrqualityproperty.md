---
description: Especifica o nível de qualidade real para codificação VBR (taxa de bits variável) baseada em qualidade (1 passagem).
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: MFPKEY_VBRQUALITY propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e95320d7306d9167f2f4e433f0661ef3c895646c6a36aab7ffeaff26d2afbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343986"
---
# <a name="mfpkey_vbrquality-property"></a>Propriedade MFPKEY \_ VBRQUALITY

Especifica o nível de qualidade real para codificação VBR (taxa de bits variável) baseada em qualidade (1 passagem).

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="remarks"></a>Comentários

Nem todos os valores no intervalo têm um significado exclusivo. Os valores que representam um avanço na qualidade do nível anterior são: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 e 100.

Para objetos do codificador de áudio, os modos de qualidade são fornecidos na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) dos tipos de saída recuperados usando [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerando tipos de áudio para modos de codificação específicos](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 
