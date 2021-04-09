---
description: Representa um trabalho criado com o comando AT.
ms.assetid: 2fa69e3f-9a6c-4aa9-8a6c-ea28eb4342ca
ms.tgt_platform: multiple
title: Classe Win32_ScheduledJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob
- Win32_ScheduledJob.Caption
- Win32_ScheduledJob.Description
- Win32_ScheduledJob.InstallDate
- Win32_ScheduledJob.Name
- Win32_ScheduledJob.Status
- Win32_ScheduledJob.ElapsedTime
- Win32_ScheduledJob.Notify
- Win32_ScheduledJob.Owner
- Win32_ScheduledJob.Priority
- Win32_ScheduledJob.TimeSubmitted
- Win32_ScheduledJob.UntilTime
- Win32_ScheduledJob.Command
- Win32_ScheduledJob.DaysOfMonth
- Win32_ScheduledJob.DaysOfWeek
- Win32_ScheduledJob.InteractWithDesktop
- Win32_ScheduledJob.JobId
- Win32_ScheduledJob.JobStatus
- Win32_ScheduledJob.RunRepeatedly
- Win32_ScheduledJob.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50162221e7ca18e07e3599deca2dba67b18ba708
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010121"
---
# <a name="win32_scheduledjob-class"></a>\_Classe Win32 ScheduledJob

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ ScheduledJob do Win32**   representa um trabalho criado com o comando **at** .

> [!Note]  
> A classe **Win32 \_ ScheduledJob** não representa um trabalho criado com o assistente de tarefa agendada no painel de controle. Você não pode alterar uma tarefa criada pelo WMI na interface do usuário de tarefas agendadas. Para obter mais informações, consulte a seção Comentários.

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E0-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("Delete"), AMENDMENT]
class Win32_ScheduledJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Command;
  uint32   DaysOfMonth;
  uint32   DaysOfWeek;
  boolean  InteractWithDesktop;
  uint32   JobId;
  string   JobStatus;
  boolean  RunRepeatedly;
  datetime StartTime;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ScheduledJob** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ ScheduledJob** tem esses métodos.



| Método                                                      | Descrição                                                                                                           |
|:------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Criada**](create-method-in-class-win32-scheduledjob.md) | Método de classe que envia um trabalho para o sistema operacional para execução em uma data e hora futura especificadas.<br/> |
| [**Apagar**](delete-method-in-class-win32-scheduledjob.md) | Método de classe que exclui um trabalho agendado.<br/>                                                                 |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ScheduledJob** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Comando**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**no comando \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| ")
</dt> </dl>

Nome do comando, programa em lotes ou arquivo binário (e argumentos de linha de comando) que o serviço de agendamento usa para invocar o trabalho.

Exemplo: "**Defrag** **/q/f**"

</dd> <dt>

**DaysOfMonth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**no \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfMonth**")
</dt> </dl>

Dias do mês em que o trabalho está agendado para ser executado. Se um trabalho estiver agendado para ser executado em vários dias do mês, esses valores poderão ser Unidos em um OR lógico. Por exemplo, se um trabalho for executado no 1º e no 16º de cada mês, o valor da propriedade **DaysOfMonth** será 1 ou 32768.

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1)


</dt> <dd>

primeiro

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2)


</dt> <dd>

2º

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4)


</dt> <dd>

3a.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8)


</dt> <dd>

4a.

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16)


</dt> <dd>

5

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32)


</dt> <dd>

6

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64)


</dt> <dd>

07

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128)


</dt> <dd>

oitavo

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256)


</dt> <dd>

nono

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512)


</dt> <dd>

10º

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024)


</dt> <dd>

11º

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048)


</dt> <dd>

12º

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096)


</dt> <dd>

13º

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192)


</dt> <dd>

14

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384)


</dt> <dd>

15º

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768)


</dt> <dd>

16

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536)


</dt> <dd>

dia

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072)


</dt> <dd>

18

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144)


</dt> <dd>

décimo

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288)


</dt> <dd>

dia

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576)


</dt> <dd>

21º

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152)


</dt> <dd>

22º

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304)


</dt> <dd>

23º

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608)


</dt> <dd>

24

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216)


</dt> <dd>

25

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432)


</dt> <dd>

26

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864)


</dt> <dd>

27

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728)


</dt> <dd>

dia

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456)


</dt> <dd>

dia

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912)


</dt> <dd>

dia

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824)


</dt> <dd>

dia

</dd> </dl>

</dd> <dt>

**DaysOfWeek**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**em \_ info**](/windows/win32/api/lmat/ns-lmat-at_info) \| **DaysOfWeek**")
</dt> </dl>

Dias da semana em que um trabalho é agendado para execução. Se um trabalho estiver agendado para ser executado em vários dias da semana, os valores poderão ser Unidos em um OR lógico. Por exemplo, se um trabalho estiver agendado para ser executado em segundas, às quartas-e sextas-feiras, o valor da propriedade **DaysOfWeek** seria 1 ou 4 ou 16.

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**Segunda** (1)


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**Terça-feira** (2)


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**Quarta-feira** (4)


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**Quinta-feira** (8)


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**Sexta-feira** (16)


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**Sábado** (32)


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**Domingo** (64)


</dt> <dd></dd> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Período de tempo em que o trabalho foi executado.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InteractWithDesktop**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede do win32api \| [**no trabalho de sinalizadores de \_ informação**](/windows/win32/api/lmat/ns-lmat-at_info)não \|  \| **\_ interativa**")
</dt> </dl>

O trabalho especificado é interativo, o que significa que um usuário pode fornecer entrada a um trabalho agendado enquanto ele está em execução.

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede do win32api \| [**no \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobID**")
</dt> </dl>

Identificando o número do trabalho. Ele é usado por métodos como um identificador para um trabalho que está sendo agendado neste computador.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("JobStatus"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede win32api \| [**em sinalizador de \_ Enumeração**](/windows/win32/api/lmat/ns-lmat-at_enum) \|  \| **\_ \_ erro de exec de trabalho**")
</dt> </dl>

Status da execução na última vez em que o trabalho foi agendado para execução.

<dt>

<span id="Success"></span><span id="success"></span><span id="SUCCESS"></span>

**Êxito** ("êxito")


</dt> <dd></dd> <dt>

<span id="Failure"></span><span id="failure"></span><span id="FAILURE"></span>

**Falha** ("falha")


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O usuário é notificado após a conclusão ou falha do trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**Proprietário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Usuário que enviou o trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Importância da execução de um trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**RunRepeatedly**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de gerenciamento de rede do win32api \| [**em \_ informações de**](/windows/win32/api/lmat/ns-lmat-at_info) \| **sinalizadores** de \| **trabalho são \_ executadas \_ periodicamente**")
</dt> </dl>

O trabalho agendado é executado repetidamente nos dias em que o trabalho é agendado. Se for **false**, o trabalho será executado uma vez.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("StartTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| estruturas de gerenciamento \| [**de rede em \_ enum**](/windows/win32/api/lmat/ns-lmat-at_enum) \| **JobTime**")
</dt> </dl>

Hora UTC para executar o trabalho, na forma de "AAAAMMDDHHMMSS. MMMMMm (+-) OOO ", onde" aaaammdd "deve ser substituído por" \* \* \* \* \* \* \* \* ". A substituição é necessária porque o serviço de agendamento só permite que os trabalhos sejam configurados para serem executados uma vez ou executados em um dia do mês ou da semana. Um trabalho não pode ser executado em uma data específica.

A seção "(+-) OOO" do valor da propriedade **StartTime** é a tendência atual para a conversão de hora local. A tendência é a diferença entre a hora UTC e a hora local. Para calcular a tendência de seu fuso horário, multiplique o número de horas em que o fuso horário está adiantado ou atrasado no horário de Greenwich (GMT) por 60 (use um número positivo para o número de horas se o fuso horário estiver à frente do GMT e um número negativo se o fuso horário estiver atrás do GMT). Adicione um 60 adicional ao seu cálculo se o seu fuso horário estiver usando o horário de verão. Por exemplo, o fuso horário padrão do Pacífico é de oito horas atrás do GMT, portanto, a tendência é igual a-420 (-8 \* 60 + 60) quando o horário de verão está em uso e-480 (-8 \* 60) quando o horário de verão não está em uso. Você também pode determinar o valor da tendência consultando a propriedade Bias da classe TimeZone do [**Win32 \_**](win32-timezone.md) .

Por exemplo: " \* \* \* \* \* \* \* \* 123000.000000-420" especifica 14,30 (2:30 P.M.) PST com o horário de verão em vigor.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**Timeenvio**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que o trabalho foi enviado.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que o trabalho é inválido ou deve ser parado.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Cada trabalho agendado no serviço de agendamento é armazenado de forma persistente (o Agendador pode iniciar um trabalho após uma reinicialização) e é executado na hora e no dia da semana ou mês especificados. Se o computador não estiver ativo ou se o serviço agendado não estiver em execução na hora do trabalho especificado, o serviço de agendamento executará o trabalho especificado no dia seguinte no horário especificado.

Os trabalhos são agendados de acordo com o tempo universal coordenado (UTC) com deslocamento de tendência de Greenwich Mean Time (GMT), o que significa que um trabalho pode ser especificado usando qualquer fuso horário. A classe **Win32 \_ ScheduledJob** retorna a hora local com o deslocamento UTC ao enumerar um objeto e converte para a hora local ao criar novos trabalhos. Por exemplo, um trabalho especificado para ser executado em um computador em Boston às 10:30 P.M. A hora da segunda-feira PST será agendada para ser executada localmente às 1:30 da manhã EST de terça-feira.

> [!Note]  
> Um cliente deve levar em conta se o horário de verão está ou não em operação no computador local e, se for, subtrair uma tendência de 60 minutos do deslocamento UTC.

 

A classe **Win32 \_ ScheduledJob** é derivada do [**\_ trabalho CIM**](cim-job.md). Você deve ser um membro do grupo Administradores para criar um trabalho agendado usando essa classe.

A classe **Win32 \_ ScheduledJob** é internamente usando o protocolo at, que está associado ao reprovamento a partir do Windows 8 e do Windows Server 2012. Como uma primeira etapa, o protocolo AT é desabilitado por padrão. Se o protocolo estiver desabilitado, por exemplo, chamar o método [**Create**](create-method-in-class-win32-scheduledjob.md) em um objeto **Win32 \_ ScheduledJob** falhará com o erro 0x8. Você pode ativar o protocolo AT novamente adicionando a seguinte entrada de registro:

``` syntax
Key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Schedule\Configuration 
Name: EnableAt 
Type: REG_DWORD
Value: 1
```

Talvez seja necessário reiniciar o computador para tornar a configuração eficaz.

Como o **Win32 \_ ScheduledJob** é baseado na API Win32 do [**NetScheduleJobGetInfo**](/windows/win32/api/lmat/nf-lmat-netschedulejobgetinfo) , você não pode usar essa classe em conjunto com o Agendador de tarefas. Se você quiser usar Agendador de Tarefas, use a API Agendador de Tarefas. Para obter mais informações, consulte a [referência de Agendador de tarefas](../taskschd/task-scheduler-reference.md).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir agenda Notepad.exe para ser executado interativamente às 1:25 pela hora do computador local todas as quartas-feiras.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set objNewJob = objWMIService.Get("Win32_ScheduledJob")
errJobCreated = objNewJob.Create("Notepad.exe", "********012500.000000-420", True , 4, , True, JobId) 
If errJobCreated <> 0 Then
Wscript.Echo "Error on task creation"
Else
Wscript.Echo "Task created"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Trabalho do CIM \_**](cim-job.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[Tarefas do WMI: tarefas agendadas](../wmisdk/wmi-tasks--scheduled-tasks.md)
</dt> </dl>

 

 
