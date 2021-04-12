---
title: Funções de retorno de chamada de aplicativo cliente
description: Dois tipos de assinaturas de retorno de chamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371edd162c4cbd1332764c7b3e9e70bf114270e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364301"
---
# <a name="client-application-callback-functions"></a>Funções de retorno de chamada de aplicativo cliente

O Windows Biometric Framework dá suporte a dois tipos de assinaturas de retorno de chamada. A partir do Windows 8, há suporte para o retorno de chamada a seguir. Recomendamos que você implemente esse retorno de chamada para todos os novos aplicativos. No entanto, esse retorno de chamada não pode ser usado no Windows 7.



| Callback                                                                                     | Descrição                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_retorno de \_ chamada de conclusão ASsíncrona PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica o aplicativo cliente de que uma operação assíncrona iniciou usando [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) ou [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) foi concluída.<br/> |



 

As seguintes funções de retorno de chamada foram introduzidas no Windows 7. Recomendamos que você não os implemente para novos aplicativos direcionados para o Windows 8 e sistemas operacionais posteriores.



| Callback                                                                                 | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**retorno de chamada de \_ captura PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Retorna os resultados da função assíncrona [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) .<br/> |
| [**\_retorno de \_ chamada de captura de registro do PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Retorna os resultados da função assíncrona [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) .<br/> |
| [**retorno de chamada de \_ evento PWINBIO \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Retorna os resultados da função assíncrona [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) .<br/>           |
| [**PWINBIO \_ identificar \_ retorno de chamada**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Retorna os resultados da função assíncrona [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) .<br/>           |
| [**PWINBIO \_ localizar \_ retorno de chamada do sensor \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Retorna os resultados da função assíncrona [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) .<br/>   |
| [**PWINBIO \_ verificar \_ retorno de chamada**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Retorna os resultados da função assíncrona [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) .<br/>               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de aplicativo cliente](client-application-reference.md)
</dt> </dl>

 

 





