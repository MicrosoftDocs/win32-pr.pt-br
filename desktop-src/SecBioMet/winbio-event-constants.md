---
title: Constantes de WINBIO_EVENT (WinBio \_ Types. h)
description: Especifique os tipos de notificações de eventos do provedor de serviços a serem monitorados.
ms.assetid: 73805413-a8d9-4682-aa21-7032451d750a
topic_type:
- apiref
api_name:
- WINBIO_EVENT_FP_UNCLAIMED
- WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a871022c51a906bd078125ae6aa6aa30c2e97024279f3309ca4ece58c00a88f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910654"
---
# <a name="winbio_event-constants"></a>\_Constantes de evento WINBIO

As constantes a seguir podem ser usadas na função [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para especificar os tipos de notificações de eventos do provedor de serviços a serem monitorados.



| Constante                                                                                                                                                                                                                        | Descrição                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span><dl> <dt>**\_evento WINBIO \_ FP não \_ reclamado**</dt> </dl>                             | O sensor detectou um dedo de dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco. o Windows Biometric Framework chama sua função de retorno de chamada para indicar que um dedo dedo ocorreu, mas não tenta identificar a impressão digital.<br/> |
| <span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span><dl> <dt>**\_identificação não \_ reivindicada de FP do evento \_ WINBIO \_**</dt> </dl> | O sensor detectou um dedo de dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco. o Windows Biometric Framework tenta identificar a impressão digital e passa o resultado desse processo para sua função de retorno de chamada.<br/>                        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





