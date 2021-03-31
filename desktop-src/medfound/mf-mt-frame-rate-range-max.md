---
description: A taxa máxima de quadros suportada por um dispositivo de captura de vídeo, em quadros por segundo.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Atributo MF_MT_FRAME_RATE_RANGE_MAX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921268"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>\_ \_ \_ \_ Atributo máximo do intervalo de taxa de quadros MF MT \_

A taxa máxima de quadros suportada por um dispositivo de captura de vídeo, em quadros por segundo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para definir esse atributo, chame [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Comentários

A taxa de quadros é expressa como uma taxa. Os bits superiores de 32 do valor do atributo contêm o numerador e os bits 32 inferiores contêm o denominador. Por exemplo, se a taxa de quadros for de 30 quadros por segundo (FPS), a taxa será 30/1.

Se o dispositivo de captura relatar uma taxa máxima de quadros, a fonte de mídia definirá esse atributo no tipo de mídia. A taxa de quadros mínima é fornecida no [atributo \_ \_ min de \_ \_ intervalo de \_ taxa de quadros MF MT](mf-mt-frame-rate-range-min.md) . O dispositivo não tem garantia de suporte a cada incremento nesse intervalo.

Para definir a taxa de quadros do dispositivo, primeiro modifique o valor do atributo de [**\_ taxa de \_ quadros \_ MF MT**](mf-mt-frame-rate-attribute.md) no tipo de mídia. Em seguida, defina o tipo de mídia na origem da mídia.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Como definir a taxa de quadros de captura de vídeo](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




