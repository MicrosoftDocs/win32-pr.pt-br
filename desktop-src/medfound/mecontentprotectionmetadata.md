---
description: O fluxo de mídia usa esse evento para enviar metadados específicos do sistema de proteção para o decodificador.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827419"
---
# <a name="mecontentprotectionmetadata-event"></a>Evento MEContentProtectionMetadata

O fluxo de mídia usa esse evento para enviar metadados específicos do sistema de proteção para o decodificador.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                                              | Descrição                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [\_KEYDATA de \_ metadados do fluxo de eventos MF \_ \_](mf-event-stream-metadata-keydata.md)<br/>                | Esse é um atributo opcional. Dados específicos do sistema de proteção.<br/> <br/>              |
| [\_KEYIDS de \_ conteúdo de metadados de fluxo de eventos MF \_ \_ \_](mf-event-stream-metadata-content-keyids.md)<br/> | IDs de chave de conteúdo com as quais o evento está associado.<br/> <br/>                          |
| [\_metadados do fluxo de eventos MF \_ \_ \_ SystemId](mf-event-stream-metadata-systemid.md)<br/>              | Esse é um atributo opcional. ID do sistema para o qual os dados de chave se destinam.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é usado, por exemplo, para comunicar o evento de rotação de chaves. Nesse caso, ele deve ser enviado o mais cedo possível para dar o tempo decodificador para se preparar antes que os exemplos criptografados com o novo ID de chave comecem a chegar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




