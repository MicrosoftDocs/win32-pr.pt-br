---
description: O evento \_ EC CODECAPI \_ EVENT é enviado por um codificador para sinalizar um evento de codificação. O cliente se registra para o evento do codificador chamando o método ICodecAPI::RegisterForEvent.
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5765c2a1156653e66c5d3685cacfdd551cd22032eea34463f5450dc6d4fbea3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965936"
---
# <a name="ec_codecapi_event"></a>EVENTO \_ EC CODECAPI \_

O evento \_ EC CODECAPI \_ EVENT é enviado por um codificador para sinalizar um evento de codificação. O cliente se registra para o evento do codificador chamando o [**método ICodecAPI::RegisterForEvent.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Dados do usuário. O valor desse parâmetro é o ponteiro especificado pelo chamador no *parâmetro userData* do [**método RegisterForEvent.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ponteiro para os dados do evento. Esses dados são alocados pelo codificador e devem ser liberados pelo aplicativo, usando a **função CoTaskMemFree.** O bloco de dados começa com uma [**estrutura CodecAPIEventData;**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) cast o *parâmetro lParam2* em um ponteiro para essa estrutura.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhuma ação padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




