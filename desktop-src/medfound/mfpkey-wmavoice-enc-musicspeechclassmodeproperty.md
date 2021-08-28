---
description: Especifica o modo do codec de voz.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Propriedade MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303a86adbf9c443149ff78a47d19922284e38d2c0aeb56dcc13a74ca20cd54a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113116"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>\_Propriedade MFPKEY WMAVOICE \_ ENC \_ MusicSpeechClassMode

Especifica o modo do codec de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACMusicSpeechClassMode

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

1

## <a name="remarks"></a>Comentários

Um valor de 1 informa ao codec que o conteúdo é somente de voz, um valor de 2 tem o codec determinar o modo automaticamente e qualquer outro valor informa o codec para usar o modo de música.

Se o modo automático não estiver codificando voz mista e música corretamente, você poderá especificar a codificação para seções individuais do arquivo usando a propriedade [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




