---
title: Constantes de WINBIO_OPERATION_TYPE (WinBio \_ Types. h)
description: Especifique o tipo de operação assíncrona que está sendo executada.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39dd6e2656ad73623df9d6a92d514e90371bc3761563e5f24c41211680c2455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909945"
---
# <a name="winbio_operation_type-constants"></a>Constantes do tipo de \_ operação WINBIO \_

as constantes a seguir podem ser retornadas pelo Windows Biometric Framework em [**um \_ \_ resultado assíncrono WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para especificar o tipo de operação assíncrona que está sendo executada.

<dl> <dt>

<span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**\_operação WINBIO \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Nenhuma operação foi identificada.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_operação WINBIO \_ aberta**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Uma sessão biométrica foi aberta. Para obter mais informações, consulte [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**\_fechamento da operação WINBIO \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Uma sessão biométrica foi fechada. Para obter mais informações, consulte [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**\_verificação da operação do WINBIO \_**
</dt> <dd> <dl> <dt>

3
</dt> <dt>



Um exemplo biométrico foi verificado em relação a uma identidade de usuário. Para obter mais informações, consulte [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO de \_ operação de \_ identificação**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Um exemplo biométrico foi capturado e comparado a um modelo existente. Para obter mais informações, consulte [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**\_operação WINBIO \_ localizar \_ sensor**
</dt> <dd> <dl> <dt>

5
</dt> <dt>



O número de ID de uma unidade biométrica foi recuperado. Para obter mais informações, consulte [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**\_início do \_ registro da operação WINBIO \_**
</dt> <dd> <dl> <dt>

6
</dt> <dt>



Uma sequência de registro biométrica foi iniciada. Para obter mais informações, consulte [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**\_captura de \_ registro de operação WINBIO \_**
</dt> <dd> <dl> <dt>

7
</dt> <dt>



Um exemplo biométrico foi capturado e adicionado ao modelo. Para obter mais informações, consulte [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**\_confirmação de \_ registro da operação WINBIO \_**
</dt> <dd> <dl> <dt>

8
</dt> <dt>



Um modelo biométrico pendente foi finalizado. Para obter mais informações, consulte [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**\_descartar registro de operação WINBIO \_ \_**
</dt> <dd> <dl> <dt>

9
</dt> <dt>



Um modelo biométrico pendente foi Descartado. Para obter mais informações, consulte [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_registros de \_ enumeração de operação WINBIO \_**
</dt> <dd> <dl> <dt>

10
</dt> <dt>



Os subfatores para um determinado modelo foram enumerados. Para obter mais informações, consulte [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ operação \_ excluir \_ modelo**
</dt> <dd> <dl> <dt>

11
</dt> <dt>



Um modelo biométrico foi excluído da loja. Para obter mais informações, consulte [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_exemplo de \_ captura de operação WINBIO \_**
</dt> <dd> <dl> <dt>

12
</dt> <dt>



Um exemplo biométrico foi capturado. Para obter mais informações, consulte [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_propriedade de \_ obtenção de operação WINBIO \_**
</dt> <dd> <dl> <dt>

13
</dt> <dt>



Uma sessão biométrica, unidade ou propriedade de modelo foi recuperada. Para obter mais informações, consulte [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_Propriedade do \_ conjunto de operações WINBIO \_**
</dt> <dd> <dl> <dt>

14
</dt> <dt>



Uma sessão biométrica, unidade, modelo ou propriedade de conta foi definida. Para obter mais informações, consulte [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ evento Get da operação WINBIO \_**
</dt> <dd> <dl> <dt>

15
</dt> <dt>



Não usado.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_unidade de \_ bloqueio de operação WINBIO \_**
</dt> <dd> <dl> <dt>

16
</dt> <dt>



Uma unidade biométrica foi bloqueada para uso exclusivo por uma sessão. Para obter mais informações, consulte [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unidade de \_ desbloqueio de operação WINBIO \_**
</dt> <dd> <dl> <dt>

17
</dt> <dt>



O bloqueio de sessão em uma unidade biométrica foi liberado. Para obter mais informações, consulte [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_unidade de \_ controle da operação WINBIO \_**
</dt> <dd> <dl> <dt>

18
</dt> <dt>



As operações definidas pelo fornecedor foram executadas em uma unidade de controle. Para obter mais informações, consulte [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_unidade de controle de operação WINBIO \_ \_ \_ privilegiada**
</dt> <dd> <dl> <dt>

19
</dt> <dt>



As operações definidas pelo fornecedor com privilégios foram executadas em uma unidade de controle. Para obter mais informações, consulte [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ operação \_ abrir \_ estrutura**
</dt> <dd> <dl> <dt>

20
</dt> <dt>



Um identificador para a estrutura biométrica foi aberto.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**\_estrutura de \_ fechamento da operação WINBIO \_**
</dt> <dd> <dl> <dt>

21
</dt> <dt>



Um identificador para a estrutura biométrica foi fechado. Para obter mais informações, consulte [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_provedores de \_ serviço de enumeração de operação WINBIO \_ \_**
</dt> <dd> <dl> <dt>

22
</dt> <dt>



Os provedores de serviços biométricos instalados foram enumerados. Para obter mais informações, consulte [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**\_ \_ \_ unidades biométricas de enumeração de operação WINBIO \_**
</dt> <dd> <dl> <dt>

23
</dt> <dt>



As unidades biométricas conectadas foram enumeradas. Para obter mais informações, consulte [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_banco de \_ dados de enumeração de operação WINBIO \_**
</dt> <dd> <dl> <dt>

24
</dt> <dt>



Os bancos de dados registrados foram enumerados. Para obter mais informações, consulte [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**\_chegada da \_ unidade de operação WINBIO \_**
</dt> <dd> <dl> <dt>

25
</dt> <dt>



Uma unidade biométrica foi criada. Para obter mais informações, consulte [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**\_remoção da \_ unidade de operação WINBIO \_**
</dt> <dd> <dl> <dt>

26
</dt> <dt>



Uma unidade biométrica foi excluída. Para obter mais informações, consulte [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_operação WINBIO \_ identificar \_ e \_ liberar o \_ tíquete**
</dt> <dd> <dl> <dt>

27
</dt> <dt>



Reservado. Esse valor tem suporte a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_ \_ \_ tíquete de verificação e \_ liberação \_ de operação WINBIO**
</dt> <dd> <dl> <dt>

28
</dt> <dt>



Reservado. Esse valor tem suporte a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_presença do \_ Monitor de operação WINBIO \_**
</dt> <dd> <dl> <dt>

29
</dt> <dt>



O mecanismo de reconhecimento facial ou de monitoramento de íris foi ativado. Para obter mais informações, consulte [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence). Esse valor tem suporte a partir de Windows 10.


</dt> </dl> </dd> <dt>

<span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO \_ de \_ registro de operação \_ Select**
</dt> <dd> <dl> <dt>

30
</dt> <dt>



Um indivíduo de um grupo de indivíduos que são representados por dados no buffer de exemplo foi especificado como o indivíduo a ser registrado. Para obter mais informações, consulte [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect). Esse valor tem suporte a partir de Windows 10.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de aplicativo cliente](client-application-constants.md)
</dt> </dl>

 

 





