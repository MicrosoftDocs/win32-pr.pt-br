---
description: As \_ constantes de áudio espacial \_ xxx definem valores relacionados a recursos de som espaciais.
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: Constantes de SPATIAL_AUDIO_XXX (SpatialAudioMetadata. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db363260b21f47676c12aeb5eaf3c10149b571ed2771a4d9f907e98b0ba17aed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018244"
---
# <a name="spatial_audio_xxx-constants"></a>\_Constantes de áudio espacial \_ xxx

As \_ constantes de áudio espacial \_ xxx definem valores relacionados a recursos de som espaciais.



| Constante/valor                                                                                                                                                                                                                                                                                       | Descrição                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**Espacial \_ \_Posição de áudio**</dt> <dt>200</dt> </dl>                                                   | Um comando padrão de metadados de áudio espacial definido pela Microsoft que representa a posição do ouvinte no modelo padrão usado por [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) , em que a cabeça do ouvinte é a posição em coordenadas (0, 0, 0), definida em metros.<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**Espacial \_ Posição de áudio- \_ \_ \_ contagem de bytes**</dt> <dt>sizeof (float) \* 3</dt> </dl> | Especifica o tamanho do valor **da \_ \_ posição de áudio espacial** .<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**Espacial \_ \_Comandos padrão de áudio \_ \_ início**</dt> <dt>200</dt> </dl>    | Especifica o início do intervalo de comandos de metadados de áudio espacial reservado da Microsoft. Os comandos de metadados personalizados são restritos às IDs de comando 0-199. Os comandos 200-255 são reservados para uso da Microsoft.<br/>                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>SpatialAudioMetadata. h</dt> </dl> |



 

 




