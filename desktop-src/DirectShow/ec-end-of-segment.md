---
description: O fim de um segmento foi atingido.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757250"
---
# <a name="ec_end_of_segment"></a>\_fim \_ do \_ segmento do EC

O fim de um segmento foi atingido.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

( **\_ tempo de referência** const \* ) ponteiro para um valor de **\_ tempo de referência** que especifica o tempo de fluxo acumulado desde o início do segmento, em unidades de 100 nanossegundos.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Número do segmento (baseado em zero).

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

O Gerenciador de gráfico de filtro verifica o número de eventos de **\_ fim \_ de \_ segmento do EC** em relação ao número de eventos de [**segmento do EC \_ \_ iniciados**](ec-segment-started.md) . Se eles corresponderem, ele encaminha **o \_ fim \_ do evento de \_ segmento do EC** para o aplicativo. Os aplicativos não podem substituir a ação padrão para este evento.

## <a name="remarks"></a>Comentários

Esse código de evento dá suporte a loop contínuo. Quando uma chamada para o método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) inclui o \_ sinalizador de segmento de busca \_ , o filtro de origem envia esse código de evento em vez de chamar [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 




