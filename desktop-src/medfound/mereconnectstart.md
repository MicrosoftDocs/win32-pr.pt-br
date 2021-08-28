---
description: Sinaliza que uma fonte de mídia está tentando se reconectar ao servidor.
ms.assetid: c5975279-c710-4046-9152-d1e1c62eb785
title: Evento MEReconnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc365acf5d91796b6d9c3fe371b9a0ec54435769381c41f0bf45cedb73003660
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114006"
---
# <a name="mereconnectstart-event"></a>Evento MEReconnectStart

Sinaliza que uma fonte de mídia está tentando se reconectar ao servidor.

Gerado por uma fonte de mídia no início de uma tentativa de reconexão. A origem da rede gerará esse evento se tentar se reconectar ao servidor. A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




