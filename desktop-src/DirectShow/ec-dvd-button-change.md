---
description: Sinaliza que o número de botões de menu do DVD foi alterado ou que a seleção do botão foi alterada.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode. h)
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
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750278"
---
# <a name="ec_dvd_button_change"></a>\_alteração do \_ botão de DVD do EC \_

Sinaliza que o número de botões de menu do DVD foi alterado ou que a seleção do botão foi alterada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica o número de botões disponíveis.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **DWORD** que indica o número do botão atualmente selecionado. O botão selecionado número zero implica que nenhum botão está selecionado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os números de botão variam de 1 a 36.

O botão selecionado no momento pode ser alterado automaticamente com um comando de navegação criado no disco, bem como por meio do controle de aplicativo usando a interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) .

Esse evento pode sinalizar qualquer um dos números de botão disponíveis. Esses números nem sempre correspondem aos números de botão usados para [**IDvdControl2:: SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) porque esse método pode ativar apenas um subconjunto de botões.

Esse evento é gerado em todos os domínios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificação de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




