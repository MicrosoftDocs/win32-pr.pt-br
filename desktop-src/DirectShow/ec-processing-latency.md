---
description: Indica a quantidade de tempo que um componente está levando para processar cada amostra.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb107dd4c895f9819d268e6112c22c0c514e480bf778692f28bc87853aee9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792616"
---
# <a name="ec_processing_latency"></a>LATÊNCIA \_ DE \_ PROCESSAMENTO DE EC

Indica a quantidade de tempo que um componente está levando para processar cada amostra.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**const REFERENCE \_ TIME**) A quantidade de tempo para processar cada amostra, em unidades de \* 100 nanossegundos.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

Um apresentador do [](enhanced-video-renderer-filter.md) filtro EVR (Renderizador de Vídeo Aprimorado) pode enviar essa mensagem para o EVR para notificar a EVR sobre a latência de processamento do apresentador.

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

 

 




