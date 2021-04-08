---
description: Um elemento lógico que representa uma unidade de trabalho a ser executada, como um script ou um trabalho de impressão. Um trabalho é diferente de um processo porque um trabalho pode ser agendado ou enfileirado e sua execução não está limitada a um único sistema.
ms.assetid: 35e35c3f-617b-429b-b68f-fa0c0c330e92
title: Classe CIM_Job (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job
- CIM_Job.JobStatus
- CIM_Job.TimeSubmitted
- CIM_Job.ScheduledStartTime
- CIM_Job.StartTime
- CIM_Job.ElapsedTime
- CIM_Job.JobRunTimes
- CIM_Job.RunMonth
- CIM_Job.RunDay
- CIM_Job.RunDayOfWeek
- CIM_Job.RunStartInterval
- CIM_Job.LocalOrUtcTime
- CIM_Job.UntilTime
- CIM_Job.Notify
- CIM_Job.Owner
- CIM_Job.Priority
- CIM_Job.PercentComplete
- CIM_Job.DeleteOnCompletion
- CIM_Job.ErrorCode
- CIM_Job.ErrorDescription
- CIM_Job.RecoveryAction
- CIM_Job.OtherRecoveryAction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6b59a162d36ee677ad00c8cc574282f970bc1d80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922257"
---
# <a name="cim_job-class-hyper-v-management"></a>Classe CIM_Job (gerenciamento do Hyper-V)

Um elemento lógico que representa uma unidade de trabalho a ser executada, como um script ou um trabalho de impressão. Um trabalho é diferente de um processo porque um trabalho pode ser agendado ou enfileirado e sua execução não está limitada a um único sistema.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Job : CIM_LogicalElement
{
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes = 1;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
};
```

## <a name="members"></a>Membros

A classe de **\_ trabalho CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ trabalho CIM** tem esses métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="cim-job-killjob.md"><strong>KillJob</strong></a></td>
<td style="text-align: left;">Esse método é preterido. Em vez disso, use o método <strong>RequestStateChange</strong> .<br/>
<blockquote>
[!Note]<br />
Descrição preterida: desliga um trabalho.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriedades

A classe de **\_ trabalho CIM** tem essas propriedades.

<dl> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

**True** para excluir o trabalho após a conclusão; caso contrário, **false**.

> [!Note]  
> Essa propriedade não excluirá trabalhos concluídos antes que essa propriedade seja definida como **true**.

 

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A duração pela qual o trabalho foi executado.

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**ErrorDescription**")
</dt> </dl>

Um código de erro específico do fornecedor que captura informações de processamento para trabalhos recorrentes. O valor deve ser definido como zero se o trabalho for concluído sem erros.

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**ErrorCode**")
</dt> </dl>

Uma cadeia de caracteres de forma livre que contém uma descrição do código de erro correspondente na propriedade **ErrorCode** .

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O número de vezes para executar o trabalho.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).**OperationalStatus**")
</dt> </dl>

Uma cadeia de caracteres de forma livre que representa o status do trabalho.

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se os horários nas propriedades **RunStartInterval** e **UntilTime** representam horários locais ou horários UTC.

<dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>

**Hora local** (1)


</dt> <dd></dd> <dt>

<span id="UTC_Time"></span><span id="utc_time"></span><span id="UTC_TIME"></span>

**Hora UTC** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

O usuário para notificar quando um trabalho for concluído ou falhar.

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**Recoveryaction**")
</dt> </dl>

Uma cadeia de caracteres que descreve a ação de recuperação quando a propriedade **recoveryaction** é **outra** ("1").

</dd> <dt>

**Proprietário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OwningJobElement**](cim-owningjobelement.md).")
</dt> </dl>

O usuário que enviou o trabalho ou o nome do serviço ou do método que solicitou o trabalho.

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("percent"), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (101), **PUnit** ("porcentagem")
</dt> </dl>

A porcentagem do trabalho concluído.

> [!Note]  
> O valor "101" é indefinido e não será permitido na próxima revisão principal da especificação.

 

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A importância do trabalho. Quanto menor o número, maior a prioridade.

</dd> <dt>

**Recuperação de**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**OtherRecoveryAction**")
</dt> </dl>

Descreve a ação de recuperação a ser tomada quando um trabalho de execução falha.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

É desconhecido quanto à ação de recuperação a ser tomada.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd>

A ação de recuperação será especificada na propriedade **OtherRecoveryAction** .

</dd> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>Não **continuar** (2)


</dt> <dd>

Pare a execução do trabalho e atualize adequadamente seu status.

</dd> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar com o próximo trabalho** (3)


</dt> <dd>

Continue com o próximo trabalho na fila.

</dd> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Executar trabalho novamente** (4)


</dt> <dd>

O trabalho deve ser executado novamente.

</dd> <dt>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>

<span id="Run_Recovery_Job"></span><span id="run_recovery_job"></span><span id="RUN_RECOVERY_JOB"></span>**Executar trabalho de recuperação** (5)


</dt> <dd>

Execute o trabalho associado usando a relação **RecoveryJob** . Observe que o trabalho de recuperação já deve estar na fila na qual ele será executado.

</dd> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (-31), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (31), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")
</dt> </dl>

Um inteiro que é usado em conjunto com a propriedade **RunDayOfWeek** para indicar o dia em que o trabalho é processado; ou, se **RunDayOfWeek** for definido como zero, **RunDay** indicará o dia do mês em que o trabalho é processado. Se **RunDay** for um inteiro negativo, ele especificará um dia em relação ao fim do mês, ou se **RunDay** for um inteiro positivo, ele especificará um dia relativo ao início do mês.

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunStartInterval**")
</dt> </dl>

Um inteiro que é usado em conjunto com a propriedade **RunDay** para indicar o dia em que o trabalho é processado; ou, se **RunDayOfWeek** for definido como zero, **RunDay** indicará o dia do mês em que o trabalho é processado.

<dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>

**-Sábado** (-7)


</dt> <dd></dd> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>

**-Sexta** (-6)


</dt> <dd></dd> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>

**-Quinta-feira** (-5)


</dt> <dd></dd> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>

**-Quartas** (-4)


</dt> <dd></dd> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>

**-Terça-feira** (-3)


</dt> <dd></dd> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>

**-Segunda-feira** (-2)


</dt> <dd></dd> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>

**-Domingo** (-1)


</dt> <dd></dd> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>

**ExactDayOfMonth** (0)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (1)


</dt> <dd></dd> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Segunda** (2)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Terça-feira** (3)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Quarta-feira** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Quinta-feira** (5)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Sexta-feira** (6)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")
</dt> </dl>

O mês em que o trabalho é processado.

<dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>

**Janeiro** (0)


</dt> <dd></dd> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>

**Fevereiro** (1)


</dt> <dd></dd> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>

**Março** (2)


</dt> <dd></dd> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>

**Abril** (3)


</dt> <dd></dd> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>

**Maio** (4)


</dt> <dd></dd> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>

**Junho** (5)


</dt> <dd></dd> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>

**Julho** (6)


</dt> <dd></dd> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>

**Agosto** (7)


</dt> <dd></dd> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>

**Setembro** (8)


</dt> <dd></dd> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>

**Outubro** (9)


</dt> <dd></dd> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>

**Novembro** (10)


</dt> <dd></dd> <dt>

<span id="December"></span><span id="december"></span><span id="DECEMBER"></span>

**Dezembro** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")
</dt> </dl>

O intervalo de tempo após a meia-noite quando o trabalho é processado. Por exemplo, "00000000020000.000000:000" indica que o trabalho é executado em ou após duas horas locais, ou hora UTC (UTC é especificado com a propriedade **LocalOrUtcTime** ).

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ trabalho CIM**.**RunMonth**","**\_ trabalho CIM**.**RunDay**","**\_ trabalho CIM**.**RunDayOfWeek**","**\_ trabalho CIM**.**RunStartInterval**")
</dt> </dl>

> [!Note]  
> Essa propriedade é preterida. Em vez disso, recomendamos que você use as propriedades **RunMonth**, **RunDay**, **RunDayOfWeek** e **RunStartInterval** .

 

A hora em que o trabalho atual é agendado para iniciar. Esse tempo pode ser representado por uma data e hora ou um intervalo relativo à hora em que a propriedade é solicitada. Um valor de todos os zeros indica que o trabalho já está em execução.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que o trabalho foi iniciado. Esse tempo pode ser representado por uma data e hora ou por um intervalo relativo à hora em que a propriedade é solicitada.

</dd> <dt>

**Timeenvio**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que o trabalho foi enviado. Um valor de todos os zeros indica que o elemento pai não é capaz de relatar uma data e hora.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ trabalho CIM**.**LocalOrUtcTime**")
</dt> </dl>

O tempo após o qual o trabalho se torna inválido ou deve ser interrompido. A hora pode ser representada por uma data e hora ou por um intervalo relativo à hora em que essa propriedade é solicitada. Um valor de todos os noves indica que o trabalho pode ser executado indefinidamente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> </dl>

 

