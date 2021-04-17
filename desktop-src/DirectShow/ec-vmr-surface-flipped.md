---
description: Enviado quando o apresentador de alocador VMR-7's chamou o método flip do DirectDraw na superfície apresentada. Isso permite que o VMR mantenha sua tabela DirectXVA de superfícies sincronizadas com a cadeia de inversão do DirectDraw.
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: EC_VMR_SURFACE_FLIPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feafaa58f0cacdafde04591d494dbb9a9eb258e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749005"
---
# <a name="ec_vmr_surface_flipped"></a>superfície do EC \_ VMR \_ \_ invertida

Enviado quando o apresentador de alocador VMR-7's chamou o método flip do DirectDraw na superfície apresentada. Isso permite que o VMR mantenha sua tabela DirectXVA de superfícies sincronizadas com a cadeia de inversão do DirectDraw.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Código de status retornado do método flip do DirectDraw.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Alocador personalizado-os apresentadores para o VMR-7 devem enviar esse evento. Este evento não é encaminhado para aplicativos e não é usado com os apresentadores de alocador para o VMR-9.

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

 

 




