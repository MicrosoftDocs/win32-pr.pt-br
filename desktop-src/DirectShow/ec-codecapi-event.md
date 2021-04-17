---
description: 'O \_ evento de evento CODECAPI do EC \_ é enviado por um codificador para sinalizar um evento de codificação. O cliente registra o evento de codificador chamando o método ICodecAPI:: RegisterForEvent.'
ms.assetid: 88924ba9-707b-41a7-9bca-c630b4a9c4c8
title: EC_CODECAPI_EVENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c24ece20a0c729b251c56b50b5b44fc9f7fa98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770079"
---
# <a name="ec_codecapi_event"></a>\_evento de CODECAPI do EC \_

O \_ evento de evento CODECAPI do EC \_ é enviado por um codificador para sinalizar um evento de codificação. O cliente registra o evento de codificador chamando o método [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Dados do usuário. O valor desse parâmetro é o ponteiro que o chamador especificou no parâmetro *UserData* do método [**RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ponteiro para os dados do evento. Esses dados são alocados pelo codificador e devem ser liberados pelo aplicativo, usando a função **CoTaskMemFree** . O bloco de dados começa com uma estrutura [**CodecAPIEventData**](/windows/desktop/api/strmif/ns-strmif-codecapieventdata) ; Converta o parâmetro *lParam2* em um ponteiro para essa estrutura.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhuma ação padrão.

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

 

 




