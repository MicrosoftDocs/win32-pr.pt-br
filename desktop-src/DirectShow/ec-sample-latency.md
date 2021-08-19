---
description: Especifica o quanto o agendamento de um componente é muito atrasado para o processamento de exemplos.
ms.assetid: 8bd202fb-3015-41a2-ad14-862f64cb252f
title: EC_SAMPLE_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 612c553916dc19685224bb512f6627363dba439883553d82c59f153324f5eda7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686146"
---
# <a name="ec_sample_latency"></a>\_latência de exemplo de EC \_

Especifica o quanto o agendamento de um componente é muito atrasado para o processamento de exemplos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(o **\_ tempo de referência const** \* ) o quanto o componente está muito atrás, em unidades de 100 nanossegundos. Se esse valor for positivo, o componente estará atrás do agendamento. Se esse valor for negativo, o componente está à frente da agenda.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Um apresentador personalizado para o filtro EVR ( [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) ) pode enviar essa mensagem para o EVR para notificar o EVR se o apresentador está atrasado ou adiantado.

A maneira mais simples de calcular *lParam1* é: *QPC agora*   *QPC Target*, em que *QPC agora* é o tempo de relógio agora, e *QPC Target* é o tempo de apresentação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> <dt>

[Como escrever um apresentador EVR](/windows/desktop/medfound/how-to-write-an-evr-presenter)
</dt> </dl>

 

