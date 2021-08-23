---
description: Especifica o carimbo de data/hora da etapa de quadro mais recente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4d3cc09d286f6955dda30aeb77288b75e90e8c66777a5f9f16246507f64b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686086"
---
# <a name="ec_scrub_time"></a>TEMPO \_ DE LIMPEZA DE \_ EC

Especifica o carimbo de data/hora da etapa de quadro mais recente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

(**DWORD**) 32 bits inferiores do carimbo de data/hora.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) 32 bits superiores do carimbo de data/hora.

</dd> </dl>

## <a name="default-action"></a>Ação Padrão

Nenhum.

## <a name="remarks"></a>Comentários

O apresentador do [**filtro**](enhanced-video-renderer-filter.md) EVR (Renderizador de Vídeo Aprimorado) envia essa mensagem para o EVR quando ele conclui uma etapa de quadro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de notificação de eventos](event-notification-codes.md)
</dt> </dl>

 

 




