---
title: Funções de retorno de chamada do aplicativo cliente
description: Dois tipos de assinaturas de retorno de chamada.
ms.assetid: 5569BFF3-9EEC-42E6-8F63-0C569C68FA74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f3e052df1821a5fd85bbba4ebbea3e6672d9e625b7d4258110fb19a5c234f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977096"
---
# <a name="client-application-callback-functions"></a>Funções de retorno de chamada do aplicativo cliente

O Windows Biometric Framework dá suporte a dois tipos de assinaturas de retorno de chamada. Começando com Windows 8, há suporte para o retorno de chamada a seguir. Recomendamos que você implemente esse retorno de chamada para todos os novos aplicativos. No entanto, esse retorno de chamada não pode ser usado Windows 7.



| Callback                                                                                     | Descrição                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RETORNO DE CHAMADA DE \_ CONCLUSÃO ASSÍNCRONA PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_async_completion_callback)<br/> | Notifica o aplicativo cliente de que uma operação assíncrona iniciada usando [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession) ou [**WinBioAsyncOpenFramework**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopenframework) foi concluída.<br/> |



 

As funções de retorno de chamada a seguir foram introduzidas Windows 7. Recomendamos que você não os implemente para novos aplicativos destinados Windows 8 sistemas operacionais posteriores.



| Callback                                                                                 | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**RETORNO DE CHAMADA DE CAPTURA PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_capture_callback)<br/>                | Retorna resultados da função [**WinBioCaptureSampleWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesamplewithcallback) assíncrona.<br/> |
| [**RETORNO DE CHAMADA DE CAPTURA DE REGISTRO PWINBIO \_ \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_enroll_capture_callback)<br/> | Retorna resultados da função [**WinBioEnrollCaptureWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapturewithcallback) assíncrona.<br/> |
| [**RETORNO DE CHAMADA DE EVENTO PWINBIO \_ \_**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_event_callback)<br/>                    | Retorna os resultados da função [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) assíncrona.<br/>           |
| [**PWINBIO \_ IDENTIFICAR RETORNO DE \_ CHAMADA**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_identify_callback)<br/>              | Retorna resultados da função [**WinBioIdentifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioidentifywithcallback) assíncrona.<br/>           |
| [**PWINBIO \_ LOCALIZE \_ O RETORNO DE CHAMADA \_ DO SENSOR**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_locate_sensor_callback)<br/>   | Retorna resultados da função [**WinBioLocateSensorWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensorwithcallback) assíncrona.<br/>   |
| [**PWINBIO \_ VERIFY \_ CALLBACK**](/windows/desktop/api/Winbio/nc-winbio-pwinbio_verify_callback)<br/>                  | Retorna os resultados da função [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback) assíncrona.<br/>               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de aplicativo cliente](client-application-reference.md)
</dt> </dl>

 

 





