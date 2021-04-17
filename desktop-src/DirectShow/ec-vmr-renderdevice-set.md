---
description: Enviado quando o VMR seleciona seu mecanismo de renderização.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760748"
---
# <a name="ec_vmr_renderdevice_set"></a>conjunto de RENDERDEVICE do EC \_ VMR \_ \_

Enviado quando o VMR seleciona seu mecanismo de renderização.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Pode ser um dos seguintes valores:



| Valor                        | Significado                                                  |
|------------------------------|----------------------------------------------------------|
| sobreposição de dispositivo de renderização do VMR \_ \_ \_ | O VMR será renderizado para a superfície de sobreposição (somente VMR-7). |
| \_VIDMEM de \_ dispositivo de renderização VMR \_  | O VMR será renderizado para a memória de vídeo.                     |
| \_SYSMEM de \_ dispositivo de renderização VMR \_  | O VMR será renderizado para a memória do sistema (somente VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento é enviado pelo VMR-7 e pelo VMR-9 e é encaminhado para aplicativos. Observe que o VMR-9 oferece suporte apenas a destinos de renderização de memória de vídeo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




