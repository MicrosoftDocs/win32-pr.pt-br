---
description: Sinaliza que o número de botões de menu de DVD foi alterado ou que a seleção do botão foi alterada.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 61e74a967df18d5ba105eda1609a72c0db9770868bbd967c7a90f5e920dc954d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652742"
---
# <a name="ec_dvd_button_change"></a>ALTERAÇÃO \_ DO BOTÃO DE DVD DE \_ \_ EC

Sinaliza que o número de botões de menu de DVD foi alterado ou que a seleção do botão foi alterada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

**Valor DWORD** que indica o número de botões disponíveis.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valor DWORD** que indica o número do botão selecionado no momento. O número do botão selecionado zero implica que nenhum botão está selecionado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os números de botão variam de 1 a 36.

O botão selecionado no momento pode ser alterado automaticamente com um comando de navegação gerado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Esse evento pode sinalizar qualquer um dos números de botão disponíveis. Esses números nem sempre correspondem aos números de botão usados para [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) porque esse método pode ativar apenas um subconjunto de botões.

Esse evento é gerado em todos os domínios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdevcode.h (inclua Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificação de evento de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




