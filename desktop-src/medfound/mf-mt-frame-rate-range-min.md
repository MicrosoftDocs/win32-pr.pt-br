---
description: A taxa mínima de quadros suportada por um dispositivo de captura de vídeo, em quadros por segundo.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: Atributo MF_MT_FRAME_RATE_RANGE_MIN (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829603"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a>\_ \_ \_ \_ Atributo min do intervalo de taxa de quadros MF MT \_

A taxa mínima de quadros suportada por um dispositivo de captura de vídeo, em quadros por segundo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para definir esse atributo, chame [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Comentários

A taxa de quadros é expressa como uma taxa. Os bits superiores de 32 do valor do atributo contêm o numerador e os bits 32 inferiores contêm o denominador. Por exemplo, se a taxa de quadros for de 30 quadros por segundo (FPS), a taxa será 30/1.

Se o dispositivo de captura relatar uma taxa de quadros mínima, a fonte de mídia definirá esse atributo no tipo de mídia. A taxa máxima de quadros é fornecida no [atributo \_ \_ máximo do \_ \_ intervalo de \_ taxa de quadros MF MT](mf-mt-frame-rate-range-max.md) . O dispositivo não tem garantia de suporte a cada incremento nesse intervalo.

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

[intervalo de taxa de quadros do MF \_ MT \_ \_ \_ \_ máx.](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 




