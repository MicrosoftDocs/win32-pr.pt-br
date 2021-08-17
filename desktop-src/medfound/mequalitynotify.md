---
description: Fornece comentários para o Gerenciador de qualidade sobre a qualidade da reprodução.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd019db55a0791ec5464cf67c7ee4d3e4a86f918efc2b4e87f4ddde2f3574ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061871"
---
# <a name="mequalitynotify-event"></a>Evento MEQualityNotify

Fornece comentários para o Gerenciador de qualidade sobre a qualidade da reprodução.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                         |
|-------------------|-------------------------------------|
| VT \_ i8<br/> | Consulte Observações.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é gerado por alguns componentes de pipeline. A sessão de mídia encaminha o evento para o Gerenciador de qualidade chamando o método [**IMFQualityManager:: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .

O tipo estendido do evento indica o significado dos dados do evento.



| Tipo estendido                            | Dados de evento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_latência de \_ processamento de notificação de qualidade MF \_ \_ | Latência de processamento aproximada introduzida pelo componente, em unidades de 100 a nanossegundos.<br/> A latência de processamento é a quantidade de latência que um componente apresenta ao pipeline processando um exemplo. Em alguns casos, a latência não pode ser derivada simplesmente observando as chamadas para [**IMFQualityManager:: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) e [**IMFQualityManager:: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput). Por exemplo, pode não haver uma correspondência um-para-um entre exemplos de entrada e exemplos de saída. Nesse caso, o componente pode enviar um evento MEQualityNotify com a latência de processamento. Se a latência de processamento for alterada, o componente poderá enviar um novo evento a qualquer momento durante o streaming.<br/> |
| \_atraso de \_ amostra de notificação de qualidade MF \_ \_         | Tempo de retardo para o exemplo, em unidades de 100 nanossegundos. Se o valor for positivo, o exemplo foi atrasado. Se o valor for negativo, o exemplo foi antecipado.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Para obter o tipo estendido, chame [**IMFMediaEvent:: getextendedattribute**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

Os componentes de pipeline não são necessários para enviar este evento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




