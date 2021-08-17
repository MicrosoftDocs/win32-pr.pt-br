---
title: Schtasks.exe
description: Permite que um administrador crie, exclua, consulte, altere, execute e termine tarefas agendadas em um computador local ou remoto.
ms.assetid: 3cf973de-14c4-4ca9-86a7-7f97181bd9e0
keywords:
- Schtasks.exe Agendador de Tarefas
topic_type:
- apiref
api_name:
- Schtasks.exe
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 0da33bf63d999ddad42f58dfa15a1c36571a664855ac20e48ef43bfd7aecd55b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139379"
---
# <a name="schtasksexe"></a>Schtasks.exe

Permite que um administrador crie, exclua, consulte, altere, execute e termine tarefas agendadas em um computador local ou remoto. Executar Schtasks.exe sem argumentos exibe o status e o próximo tempo de execução para cada tarefa registrada. 

Para obter mais informações sobre Agendador de Tarefas, consulte esta introdução: [Agendador de Tarefas para desenvolvedores](task-scheduler-start-page.md).

## <a name="creating-a-task"></a>Criando uma tarefa

A sintaxe a seguir é usada para criar uma tarefa no computador local ou remoto.

``` syntax
schtasks /Create 
[/S system [/U username [/P [password]]]]
[/RU username [/RP [password]] /SC schedule [/MO modifier] [/D day]
[/M months] [/I idletime] /TN taskname /TR taskrun [/ST starttime]
[/RI interval] [ {/ET endtime | /DU duration} [/K] 
[/XML xmlfile] [/V1]] [/SD startdate] [/ED enddate] [/IT] [/Z] [/F]
```

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Um valor que especifica o computador remoto ao que se conectar. Se omitido, o parâmetro do sistema assume como padrão o computador local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Um valor que especifica o contexto do usuário sob o qual Schtasks.exe deve ser executado.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**Senha /P** **\[ \]**
</dt> <dd>

Um valor que especifica a senha para um determinado contexto de usuário. Se omitido, Schtasks.exe solicita a entrada do usuário.

</dd> <dt>

<span id="_RU_username"></span><span id="_ru_username"></span><span id="_RU_USERNAME"></span>**/RU** **username**
</dt> <dd>

Um valor que especifica o contexto do usuário no qual a tarefa é executado. Para a conta do sistema, os valores válidos são "", "NT AUTHORITY \\ SYSTEM" ou "SYSTEM". Para Agendador de Tarefas 2.0, "NT AUTHORITY \\ LOCALSERVICE" e "NT AUTHORITY \\ NETWORKSERVICE" também são valores válidos.

</dd> <dt>

<span id="_RP__password_"></span><span id="_rp__password_"></span><span id="_RP__PASSWORD_"></span>**Senha /RP** **\[ \]**
</dt> <dd>

Um valor que especifica a senha para o usuário especificado com o parâmetro /RU. Para solicitar a senha, o valor deve ser " \* " ou nenhum valor. Essa senha é ignorada para a conta do sistema. Esse parâmetro deve ser combinado com /RU ou com a opção /XML.

</dd> <dt>

<span id="_SC_schedule"></span><span id="_sc_schedule"></span><span id="_SC_SCHEDULE"></span>**/SC** **schedule**
</dt> <dd>

Um valor que especifica a frequência de agendamento. Os valores válidos são: MINUTE, HOURLY, DAILY, WEEKLY, MONTHLY, ONCE, ONLOGON, ONIDLE e ONEVENT.

</dd> <dt>

<span id="_MO_modifier"></span><span id="_mo_modifier"></span><span id="_MO_MODIFIER"></span>**Modificador /MO** 
</dt> <dd>

Um valor que refina o tipo de agendamento para permitir um controle mais refinado sobre a recorrência da agenda. Os valores válidos são:

-   MINUTO: 1 a 1439 minutos.
-   HOURLY: 1 a 23 horas.
-   DIARIAMENTE: 1 a 365 dias.
-   SEMANAL: semanas de 1 a 52.
-   ONCE: nenhum modificador.
-   ONSTART: nenhum modificador.
-   ONLOGON: nenhum modificador.
-   ONIDLE: nenhum modificador.
-   MENSAL: 1 a 12 ou FIRST, SECOND, THIRD, FOURTH, LAST e LASTDAY.
-   ONEVENT: cadeia de caracteres de consulta de evento XPath.

</dd> <dt>

<span id="_D_days"></span><span id="_d_days"></span><span id="_D_DAYS"></span>**/D** **dias**
</dt> <dd>

Um valor que especifica o dia da semana para executar a tarefa. Os valores válidos são: MON, TUE, WED, THU, FRI, SAT, SUN e para agendas MENSAIS de 1 a 31 (dias do mês). O caractere curinga ( \* ) especifica todos os dias.

</dd> <dt>

<span id="_M_months"></span><span id="_m_months"></span><span id="_M_MONTHS"></span>**/M** **months**
</dt> <dd>

Um valor que especifica os meses do ano. O padrão é o primeiro dia do mês. Os valores válidos são: JAN, FEB, MAR, APR, MAY, JUN, JUL, AUG, SEP, OCT, NOV e DEC. O caractere curinga ( \* ) especifica todos os meses.

</dd> <dt>

<span id="_I_idletime"></span><span id="_i_idletime"></span><span id="_I_IDLETIME"></span>**/I** **idletime**
</dt> <dd>

Um valor que especifica a quantidade de tempo ocioso a aguardar antes de executar uma tarefa ONIDLE agendada. O intervalo válido é de 1 a 999 minutos.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Um valor que especifica um nome que identifica exclusivamente a tarefa agendada.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Um valor que especifica o caminho e o nome do arquivo da tarefa a ser executado no horário agendado. Por exemplo: C: \\ Windows \\ System32 \\calc.exe.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/ST** **starttime**
</dt> <dd>

Um valor que especifica a hora de início para executar a tarefa. O formato de hora é HH:mm (hora de 24 horas). Por exemplo, 14:30 especifica 14h30. O padrão é que a hora atual é /ST não está especificada. Essa opção é necessária com o argumento /SC ONCE.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**Intervalo de /RI** 
</dt> <dd>

Um valor que especifica o intervalo de repetição em minutos. Isso não se aplica aos seguintes tipos de agendamento: MINUTE, HOURLY, ONSTART, ONLOGON, ONIDLE e ONEVENT. O intervalo válido é de 1 a 599940 minutos. Se os parâmetros /ET ou /DU são especificados, o padrão é 10 minutos.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/ET** **endtime**
</dt> <dd>

Um valor que especifica a hora de término para executar a tarefa. O formato de hora é HH:mm (hora de 24 horas). Por exemplo, 14:50 especifica 14h50. Isso não se aplica aos seguintes tipos de agendamento: ONSTART, ONLOGON, ONIDLE e ONEVENT.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/DU** **duration**
</dt> <dd>

Um valor que especifica a duração da tarefa. O formato de hora é HH:mm (hora de 24 horas). Por exemplo, 14:50 especifica 14h50. Isso não se aplica a /ET e aos seguintes tipos de agendamento: ONSTART, ONLOGON, ONIDLE e ONEVENT. Para tarefas /V1 (Agendador de Tarefas tarefas 1.0), se /RI for especificado, o padrão de duração será de uma hora.

**Windows XP:** Essa opção não está disponível.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/k** 
</dt> <dd>

Um valor que encerra a tarefa na hora de término ou no tempo de duração. Isso não se aplica aos seguintes tipos de agendamento: ONSTART, ONLOGON, ONIDLE e ONEVENT. /ET ou /DU devem ser especificados.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **startdate**
</dt> <dd>

Um valor que especifica a primeira data na qual executar a tarefa. O formato é mm/dd/aaaa. Esse valor assume como padrão a data atual. Isso não se aplica aos seguintes tipos de agendamento: ONCE, ONSTART, ONLOGON, ONIDLE e ONEVENT.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/ED** **enddate**
</dt> <dd>

Um valor que especifica a última data em que a tarefa será executado. O formato é mm/dd/aaaa. Isso não se aplica aos seguintes tipos de agendamento: ONCE, ONSTART, ONLOGON, ONIDLE e ONEVENT.

</dd> <dt>

<span id="_EC_ChannelName"></span><span id="_ec_channelname"></span><span id="_EC_CHANNELNAME"></span>**/EC** **ChannelName**
</dt> <dd>

Um valor que especifica o canal de eventos para gatilhos ONEVENT.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Um valor que permite que a tarefa seja executado interativamente somente se o usuário /RU estiver conectado no momento em que a tarefa for executado. A tarefa será executado somente se o usuário estiver conectado.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_NP_"></span><span id="_np_"></span>**/NP** 
</dt> <dd>

Um valor que indica que nenhuma senha é armazenada. A tarefa não é executado interativamente como o usuário determinado. Somente recursos locais estão disponíveis.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/z** 
</dt> <dd>

Um valor que marca a tarefa a ser excluída após sua última executar.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_XML_xmlfile"></span><span id="_xml_xmlfile"></span><span id="_XML_XMLFILE"></span>**/XML** **xmlfile**
</dt> <dd>

Um valor que cria uma tarefa de um arquivo XML. Esse parâmetro pode ser combinado com opções /RU e /RP ou com a opção /RP sozinho quando o XML da tarefa já contiver a entidade de segurança.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_V1_"></span><span id="_v1_"></span>**/V1** 
</dt> <dd>

Um valor que cria uma tarefa visível para Windows 2000, Windows Server 2003 e Windows XP.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/f** 
</dt> <dd>

Um valor que cria a tarefa com força e suprime avisos se a tarefa especificada já existir.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span>**/RL** **level**
</dt> <dd>

Um valor que define o nível de executar para a tarefa. Os valores válidos são LIMITED e HIGHEST. O padrão é LIMITED.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/DELAY** **delaytime**
</dt> <dd>

Um valor que especifica o tempo de espera para atrasar a tarefa depois que o gatilho é disparado. O formato de hora é mmmm:ss. Essa opção só é válida para tipos de agendamento ONSTART, ONLOGON e ONEVENT.

**Windows XP e Windows Server 2003:** Essa opção não está disponível.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Um valor que exibe a mensagem de ajuda para Schtasks.exe.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao criar uma tarefa em um computador remoto em execução no Windows XP, no Windows Server 2003 ou no sistema operacional Windows 2000, use a opção /V1.

Não é possível criar uma tarefa remota não interativa Agendador de Tarefas 1.0 (crie uma tarefa sem usar a opção /IT e usando a opção /V1) se o computador remoto tiver a exceção de firewall Compartilhamento de Arquivos e Impressoras habilitada e a exceção de firewall gerenciamento de tarefas agendadas remotas desabilitada.

## <a name="deleting-a-task"></a>Excluindo uma tarefa

A sintaxe a seguir é usada para excluir uma ou mais tarefas agendadas.

``` syntax
schtasks /Delete 
[/S system [/U username [/P [password]]]]
[/TN taskname] [/F]
```

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Um valor que especifica o computador remoto ao que se conectar. Se omitido, o parâmetro do sistema assume como padrão o computador local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Um valor que especifica o contexto do usuário sob o qual Schtasks.exe deve ser executado.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**Senha /P** **\[ \]**
</dt> <dd>

Um valor que especifica a senha para o contexto de usuário especificado. Se omitido, Schtasks.exe solicita a entrada do usuário.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Um valor que especifica o nome da tarefa agendada a ser excluído. O caractere curinga ( \* ) pode ser usado para excluir todas as tarefas.

</dd> <dt>

<span id="_F_"></span><span id="_f_"></span>**/f** 
</dt> <dd>

Um valor que exclui com força a tarefa e suprime avisos se a tarefa especificada estiver em execução.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Um valor que exibe a Ajuda para Schtasks.exe.

</dd> </dl>

## <a name="running-a-task"></a>Executando uma tarefa

A sintaxe a seguir é usada para executar imediatamente uma tarefa agendada.

``` syntax
schtasks /Run 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Um valor que especifica o computador remoto ao que se conectar. Se omitido, o parâmetro do sistema assume como padrão o computador local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Um valor que especifica o contexto do usuário sob o qual Schtasks.exe deve ser executado.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**Senha /P** **\[ \]**
</dt> <dd>

Um valor que especifica a senha para o contexto de usuário especificado. Se omitido, Schtasks.exe solicita a entrada do usuário.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Um valor que especifica o nome da tarefa agendada a ser executado.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Um valor que exibe a Ajuda para Schtasks.exe.

</dd> </dl>

## <a name="ending-a-running-task"></a>Encerrando uma tarefa em execução

A sintaxe a seguir é usada para interromper uma tarefa agendada em execução.

> [!Note]  
> Para impedir que uma tarefa remota seja executada, verifique se o computador remoto tem as exceções de firewall Compartilhamento de Arquivos e Impressoras e Gerenciamento de Tarefas Agendadas Remotas habilitadas.

 

``` syntax
schtasks /End 
[/S system [/U username [/P [password]]]]
/TN taskname
```

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Um valor que especifica o computador remoto ao que se conectar. Se omitido, o parâmetro do sistema assume como padrão o computador local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Um valor que especifica o contexto do usuário sob o qual Schtasks.exe deve ser executado.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**Senha /P** **\[ \]**
</dt> <dd>

Um valor que especifica a senha para o contexto de usuário especificado. Se omitido, Schtasks.exe solicita a entrada do usuário.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **taskname**
</dt> <dd>

Um valor que especifica o nome da tarefa agendada a ser parada.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Um valor que exibe a Ajuda para Schtasks.exe.

</dd> </dl>

## <a name="querying-for-task-information"></a>Consultando informações de tarefa

A sintaxe a seguir é usada para exibir as tarefas agendadas do computador local ou remoto.

``` syntax
schtasks /Query 
[/S system [/U username [/P [password]]]]
[/FO format | /XML] [/NH] [/V] [/TN taskname] [/?]
```

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**Sistema /S** 
</dt> <dd>

Um valor que especifica o computador remoto ao que se conectar. Se omitido, o parâmetro do sistema assume como padrão o computador local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **username**
</dt> <dd>

Um valor que especifica o contexto do usuário sob o qual Schtasks.exe deve ser executado.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**Senha /P** **\[ \]**
</dt> <dd>

Um valor que especifica a senha para o contexto de usuário especificado. Se omitido, Schtasks.exe solicita a entrada do usuário.

</dd> <dt>

<span id="_FO_format"></span><span id="_fo_format"></span><span id="_FO_FORMAT"></span>**Formato /FO** 
</dt> <dd>

Um valor que especifica o formato de saída. Os valores válidos são TABLE, LIST e CSV.

</dd> <dt>

<span id="_NH_"></span><span id="_nh_"></span>**/NH** 
</dt> <dd>

Um valor que especifica que o header de coluna não deve ser exibido na saída. Isso é válido somente para formatos de tabela e CSV.

</dd> <dt>

<span id="_V_"></span><span id="_v_"></span>**/V** 
</dt> <dd>

Um valor que exibe a saída de tarefa detalhada.

> [!Note]  
> Se uma tarefa foi agendada para ser executada apenas uma vez, as informações de agendamento exibidas são "os dados de agendamento não estão disponíveis neste formato".

 

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**
</dt> <dd>

Um valor que especifica o nome da tarefa para a qual recuperar as informações. Se nenhum nome de tarefa for especificado, as informações para todas as tarefas serão exibidas.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_XML_"></span><span id="_xml_"></span>**/XML** 
</dt> <dd>

Um valor que é usado para exibir as definições de tarefa em formato XML.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Um valor que é usado para exibir a ajuda para Schtasks.exe.

</dd> </dl>

## <a name="changing-a-task"></a>Alterando uma tarefa

A sintaxe a seguir é usada para alterar a forma como o programa é executado, ou alterar a conta de usuário e a senha usadas por uma tarefa agendada.

``` syntax
schtasks /Change 
[/S system [/U username [/P [password]]]] /TN taskname
{ [/RU runasuser] [/RP runaspassword] [/TR taskrun] [/ST starttime] 
[/RI interval] [ {/ET endtime | /DU duration} [/K] ]
[/SD startdate] [/ED enddate] [/ENABLE | /DISABLE] [/IT] [/Z] }
```

### <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_S_system"></span><span id="_s_system"></span><span id="_S_SYSTEM"></span>**/S** **sistema**
</dt> <dd>

Um valor que especifica o computador remoto ao qual se conectar. Se omitido, o parâmetro do sistema usa como padrão o computador local.

</dd> <dt>

<span id="_U_username"></span><span id="_u_username"></span><span id="_U_USERNAME"></span>**/U** **nome de usuário**
</dt> <dd>

Um valor que especifica o contexto de usuário no qual Schtasks.exe deve ser executado.

</dd> <dt>

<span id="_P__password_"></span><span id="_p__password_"></span><span id="_P__PASSWORD_"></span>**/P** **\[ senha \]**
</dt> <dd>

Um valor que especifica a senha para o contexto de usuário fornecido. Se for omitido, Schtasks.exe solicitará a entrada do usuário.

</dd> <dt>

<span id="_TN_taskname"></span><span id="_tn_taskname"></span><span id="_TN_TASKNAME"></span>**/TN** **Nome_Tarefa**
</dt> <dd>

Um valor que especifica qual tarefa agendada deve ser alterada.

</dd> <dt>

<span id="_RU_runasuser"></span><span id="_ru_runasuser"></span><span id="_RU_RUNASUSER"></span>**/Ru** **runasuser**
</dt> <dd>

Um valor que altera o nome de usuário (contexto do usuário) no qual a tarefa agendada será executada. Para a conta do sistema, os valores válidos são "", "NT AUTHORITY \\ System" ou "System". Para Agendador de Tarefas tarefas 2,0, "NT AUTHORITY \\ LocalService" e "NT Authority \\ NetworkService" também são valores válidos.

</dd> <dt>

<span id="_RP_runaspassword"></span><span id="_rp_runaspassword"></span><span id="_RP_RUNASPASSWORD"></span>**/RP** **runaspassword**
</dt> <dd>

Um valor que especifica uma nova senha para o contexto de usuário existente ou a senha para uma nova conta de usuário. Essa senha é ignorada para a conta do sistema.

</dd> <dt>

<span id="_TR_taskrun"></span><span id="_tr_taskrun"></span><span id="_TR_TASKRUN"></span>**/TR** **taskrun**
</dt> <dd>

Um valor que especifica um novo programa em que a tarefa será executada.

</dd> <dt>

<span id="_ST_starttime"></span><span id="_st_starttime"></span><span id="_ST_STARTTIME"></span>**/St** **StartTime**
</dt> <dd>

Um valor que especifica a hora de início para executar a tarefa. O formato de hora é HH: mm (hora de 24 horas). Por exemplo, 14:30 especifica 2: às 16h30.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_RI_interval"></span><span id="_ri_interval"></span><span id="_RI_INTERVAL"></span>**/Ri** **intervalo**
</dt> <dd>

Um valor que especifica o intervalo de repetição, em minutos. O intervalo válido é de 1-599940 minutos.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_ET_endtime"></span><span id="_et_endtime"></span><span id="_ET_ENDTIME"></span>**/Et** **EndTime**
</dt> <dd>

Um valor que especifica a hora de término da tarefa. O formato de hora é HH: mm (hora de 24 horas). Por exemplo, 14:50 especifica 2:50PM.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_DU_duration"></span><span id="_du_duration"></span><span id="_DU_DURATION"></span>**/Du** **duração**
</dt> <dd>

Um valor que especifica a duração da execução da tarefa. O formato de hora é HH: mm (hora de 24 horas). Por exemplo, 14:50 especifica 2:50PM. Isso não é aplicável com o parâmetro/ET.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_K_"></span><span id="_k_"></span>**/K** 
</dt> <dd>

Um valor que termina a tarefa na hora de término ou no tempo de duração.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_SD_startdate"></span><span id="_sd_startdate"></span><span id="_SD_STARTDATE"></span>**/SD** **StartDate**
</dt> <dd>

Um valor que especifica a primeira data na qual executar a tarefa. O formato é mm/dd/aaaa.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_ED_enddate"></span><span id="_ed_enddate"></span><span id="_ED_ENDDATE"></span>**/Ed** **EndDate**
</dt> <dd>

Um valor que especifica a última data em que a tarefa será executada. O formato é mm/dd/aaaa.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_IT_"></span><span id="_it_"></span>**/IT** 
</dt> <dd>

Um valor que permite que a tarefa seja executada interativamente somente se o usuário/RU estiver conectado no momento no momento em que a tarefa for executada. A tarefa será executada somente se o usuário estiver conectado.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_RL_level"></span><span id="_rl_level"></span><span id="_RL_LEVEL"></span> **Nível** de/RL
</dt> <dd>

Um valor que define o nível de execução para a tarefa. Os valores válidos são limitado e mais alto.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_ENABLE_"></span><span id="_enable_"></span>**/ENABLE** 
</dt> <dd>

Um valor que habilita a tarefa agendada. Uma tarefa habilitada pode ser executada e uma tarefa desabilitada não pode ser executada.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_DISABLE_"></span><span id="_disable_"></span>**/DISABLE** 
</dt> <dd>

Um valor que desabilita a execução da tarefa agendada.

> [!Note]  
> Se uma tarefa remota Agendador de Tarefas 1,0 for desabilitada por Schtasks.exe e o computador remoto tiver a exceção de firewall de compartilhamento de arquivos e impressoras habilitada e a exceção de firewall de gerenciamento de tarefas agendadas remotas estiver desabilitada, a tarefa não será desabilitada quando lida de uma API Agendador de Tarefas 2,0.

 

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_Z_"></span><span id="_z_"></span>**/Z** 
</dt> <dd>

Um valor que marca a tarefa a ser excluída após sua execução final.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="_DELAY_delaytime"></span><span id="_delay_delaytime"></span><span id="_DELAY_DELAYTIME"></span>**/Delay** **DelayTime**
</dt> <dd>

Um valor que especifica o tempo de espera para atrasar a execução da tarefa depois que o gatilho é acionado. O formato de hora é mmmm: SS. Essa opção só é válida para tarefas com os tipos de agendamento OnStart, ONLOGON e OnEvent.

**Windows XP e Windows Server 2003:** Esta opção não está disponível.

</dd> <dt>

<span id="___"></span>**/?** 
</dt> <dd>

Um valor que exibe a mensagem de ajuda para Schtasks.exe.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



 

 





