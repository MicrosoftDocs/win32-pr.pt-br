---
description: a \_ classe WMI abstrata do Win32 ProcessStartup representa a configuração de inicialização de um processo baseado em Windows.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Classe Win32_ProcessStartup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10b0732b89d5240b457152f4bd19f951f69b8ee693baec54daea3bd6bbba9439
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759346"
---
# <a name="win32_processstartup-class"></a>\_Classe Win32 ProcessStartup

a [classe WMI](../wmisdk/retrieving-a-class.md) abstrata do **Win32 \_ ProcessStartup** representa a configuração de inicialização de um processo baseado em Windows. A classe é definida como uma definição de tipo de método, o que significa que ela é usada apenas para passar informações para o método [**Create**](create-method-in-class-win32-process.md) da classe [**\_ process do Win32**](win32-process.md) .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ProcessStartup** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ProcessStartup** tem essas propriedades.

<dl> <dt>

**CreateFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de processo e thread win32api \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")
</dt> </dl>

Valores adicionais que controlam a classe de prioridade e a criação do processo. Os seguintes valores de criação podem ser especificados em qualquer combinação, exceto quando observado.

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Depurar \_ Processo** (1)


</dt> <dd>

Se esse sinalizador for definido, o processo de chamada será tratado como um depurador e o novo processo será depurado. O sistema notifica o depurador de todos os eventos de depuração que ocorrem no processo que está sendo depurado.

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Depurar \_ Somente \_ este \_ processo** (2)


</dt> <dd>

Se esse sinalizador não for definido e o processo de chamada estiver sendo depurado, o novo processo se tornará outro processo sendo depurado. Se o processo de chamada não for um processo de ser depurado, nenhuma ação relacionada à depuração ocorrerá.

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Criar \_ Suspenso** (4)


</dt> <dd>

O thread principal do novo processo é criado em um estado suspenso e não é executado até que o método [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) seja chamado.

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>Desanexado **\_ Processo** (8)


</dt> <dd>

Para processos de console, o novo processo não tem acesso ao console do processo pai. Esse sinalizador não poderá ser usado se o sinalizador **criar \_ novo \_ console** estiver definido.

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Criar \_ Novo \_ console** (16)


</dt> <dd>

Esse novo processo tem um novo console, em vez de herdar o console pai. Esse sinalizador não pode ser usado com o sinalizador de **\_ processo desanexado** .

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Criar \_ Novo \_ \_ grupo de processos** (512)


</dt> <dd>

Esse novo processo é o processo raiz de um novo grupo de processos. O grupo de processos inclui todos os processos que são descendentes desse processo raiz. O identificador de processo do novo grupo de processos é o mesmo que o identificador de processo retornado na propriedade **ProcessId** da classe [**\_ process do Win32**](win32-process.md) . Os grupos de processos são usados pelo método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) para habilitar o envio de um sinal CTRL + C ou um sinal CTRL + BREAK para um grupo de processos de console.

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Criar \_ \_Ambiente Unicode** (1024)


</dt> <dd>

As configurações de ambiente listadas na propriedade **EnvironmentVariables** usam caracteres Unicode. Se esse sinalizador não for definido, o bloco de ambiente usará caracteres ANSI.

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Criar \_ \_ \_ Modo de erro padrão** (67108864)


</dt> <dd>

Processos recém-criados recebem o modo de erro padrão do sistema do processo de chamada em vez de herdar o modo de erro do processo pai. Esse sinalizador é útil para aplicativos de shell multithread que são executados com erros de hardware desabilitados.

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Criar \_ BREAKAWAY \_ do \_ trabalho** (16777216)


</dt> <dd>

Usado para o processo criado não ser limitado pelo objeto de trabalho.

</dd> </dl>

</dd> <dt>

**EnvironmentVariables**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ user \\ \\ Environment")
</dt> </dl>

Lista de configurações para a configuração de um computador. Variáveis de ambiente especificam caminhos de pesquisa para arquivos, diretórios para arquivos temporários, opções específicas de aplicativo e outras informações semelhantes. O sistema mantém um bloco de configurações de ambiente para cada usuário e um para o computador. O bloco de ambiente do sistema representa variáveis de ambiente para todos os usuários de um computador específico. O bloco de ambiente de um usuário representa as variáveis de ambiente que o sistema mantém para um usuário específico e inclui o conjunto de variáveis de ambiente do sistema. Por padrão, cada processo recebe uma cópia do bloco de ambiente para seu processo pai. Normalmente, esse é o bloco de ambiente para o usuário que fez logon. Um processo pode especificar diferentes blocos de ambiente para seus processos filhos.

</dd> <dt>

**ErrorMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Error Functions \| SetError")
</dt> </dl>

Em alguns processadores não x86, referências de memória desalinhadas causam uma exceção de falha de alinhamento. O **sinalizador \_ sem \_ falhas \_ de alinhamento** permite que você controle se um sistema operacional corrige ou não automaticamente essas falhas de alinhamento ou as torna visíveis para um aplicativo. Em uma plataforma de milhões de instruções por segundo (MIPS), um aplicativo deve chamar explicitamente [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) com **a \_ falha sem alinhamento \_ \_ , exceto** o sinalizador, para que o sistema operacional corrija automaticamente as falhas de alinhamento.

Como um sistema operacional processa vários tipos de erros graves. Você pode especificar que o sistema operacional tenha erros de processo ou que um aplicativo possa receber e processar erros.

A configuração padrão é para o sistema operacional tornar as falhas de alinhamento visíveis para um aplicativo. Como a plataforma x86 não torna as falhas de alinhamento visíveis para um aplicativo, o **sinalizador \_ sem \_ falhas \_ de alinhamento** não faz com que o sistema operacional gere um erro de falha de alinhamento — mesmo que o sinalizador não esteja definido. O estado padrão de [**SetError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) é definir todos os sinalizadores como 0 (zero).

<dt>



 (1)


</dt> <dd>

Padrão

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Falha \_ \_Erros críticos** (2)


</dt> <dd>

Se esse sinalizador for definido, o sistema operacional não exibirá a caixa de mensagem de identificador de erro crítico quando esse erro ocorrer. Em vez disso, o sistema operacional envia o erro para o processo de chamada.

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**Não \_ Falha de alinhamento \_ \_ , exceto** (4)


</dt> <dd>

Se esse sinalizador for definido, o sistema operacional corrigirá automaticamente as falhas de alinhamento de memória e as tornará invisíveis para o aplicativo. Ele faz isso para os processos de chamada e descendentes. Esse sinalizador se aplica somente ao RISC (computação de conjunto de instruções) e não tem nenhum efeito sobre os processadores x86.

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**Não \_ \_Caixa de \_ erro \_ de falha de GP** (8)


</dt> <dd>

Se esse sinalizador for definido, o sistema operacional não exibirá a caixa de mensagem de falha de proteção geral (GP) quando ocorrer um erro GP. Esse sinalizador só deve ser definido pela depuração de aplicativos que lidam com erros de GP.

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**Não \_ \_Caixa de \_ erro \_ Abrir arquivo** (16)


</dt> <dd>

Se esse sinalizador for definido, o sistema operacional não exibirá uma caixa de mensagem quando falhar em localizar um arquivo. Em vez disso, o erro é retornado para o processo de chamada. Esse sinalizador é ignorado no momento.

</dd> </dl>

</dd> <dt>

**Fillattribute**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")
</dt> </dl>

As cores do texto e do plano de fundo se uma nova janela do console for criada em um aplicativo de console. Esses valores são ignorados em aplicativos de GUI (interface gráfica do usuário). Para especificar as cores de primeiro plano e de segundo plano, adicione os valores juntos. Por exemplo, para ter o tipo vermelho (4) em um plano de fundo azul (16), defina Fillattribute como 20.

<dt>

1
</dt> <dd>

Azul em primeiro plano \_

</dd> <dt>

2
</dt> <dd>

Primeiro plano \_ verde

</dd> <dt>

4
</dt> <dd>

Vermelho em primeiro plano \_

</dd> <dt>

8
</dt> <dd>

Intensidade de primeiro \_ plano

</dd> <dt>

16
</dt> <dd>

Tela de \_ fundo azul

</dd> <dt>

32
</dt> <dd>

Verde da \_ tela de fundo

</dd> <dt>

64
</dt> <dd>

Plano de \_ fundo vermelho

</dd> <dt>

128
</dt> <dd>

Intensidade da \_ segundo plano

</dd> </dl>

</dd> <dt>

**Priorityclass**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**JOBOBJECT BASIC LIMIT \_ \_ \_ INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")
</dt> </dl>

Classe priority do novo processo. Use essa propriedade para determinar as prioridades de agendamento dos threads no processo. Se a propriedade for deixada nula, a classe de prioridade será padrão como Normal, a menos que a classe de prioridade do processo de criação seja Idle ou Below \_ Normal. Nesses casos, o processo filho recebe a classe de prioridade padrão do processo de chamada.

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)


</dt> <dd>

Indica um processo normal sem necessidades especiais de agendamento.

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Ocioso** (64)


</dt> <dd>

Indica um processo com threads que são executados somente quando o sistema está ocioso e são preempção pelos threads de qualquer processo em execução em uma classe de prioridade mais alta. Um exemplo é uma economia de tela. A classe de prioridade ociosa é herdada por processos filho.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (128)


</dt> <dd>

Indica um processo que executa tarefas críticas de tempo que devem ser executadas imediatamente para serem executadas corretamente. Os threads de um processo de classe de alta prioridade preempção dos threads de processos de classe de prioridade normal ou de prioridade ociosa. Um exemplo é Windows Lista de Tarefas, que deve responder rapidamente quando chamado pelo usuário, independentemente da carga no sistema operacional. Use muito cuidado ao usar a classe de alta prioridade, pois um aplicativo com limite de CPU de classe de alta prioridade pode usar quase todos os ciclos disponíveis. Somente um thread de prioridade em tempo real preempções definidos para esse nível.

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tempo real** (256)


</dt> <dd>

Indica um processo que tem a prioridade mais alta possível. Os threads de um processo de classe de prioridade em tempo real preempção dos threads de todos os outros processos, incluindo threads de alta prioridade e processos do sistema operacional que executam tarefas importantes. Por exemplo, um processo em tempo real que é executado por mais de um intervalo muito breve pode fazer com que os caches de disco não sejam liberados ou fazer com que um mouse não seja responsivo.

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Abaixo \_ Normal** (16384)


</dt> <dd>

Indica um processo que tem uma prioridade maior que Idle, mas menor que Normal.

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Acima \_ Normal** (32768)


</dt> <dd>

Indica um processo que tem uma prioridade maior que Normal, mas menor que Alta.

</dd> </dl>

</dd> <dt>

**ShowWindow**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")
</dt> </dl>

Como a janela é exibida para o usuário. Pode ser qualquer um dos valores que podem ser especificados no parâmetro *nCmdShow* para a [função ShowWindow.](/windows/desktop/api/winuser/nf-winuser-showwindow)

</dd> <dt>

**Título**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")
</dt> </dl>

Texto exibido na barra de título quando uma nova janela do console é criada; usado para processos de console. Se **NULL**, o nome do arquivo executável será usado como o título da janela. Essa propriedade deve ser **NULL para** processos de GUI ou console que não criam uma nova janela de console.

</dd> <dt>

**WinstationDesktop**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")
</dt> </dl>

O nome da área de trabalho ou o nome da área de trabalho e da estação de janela para o processo. Uma faixa invertida na cadeia de caracteres indica que a cadeia de caracteres inclui nomes de estação de área de trabalho e de janela. Se **WinstationDesktop** for **NULL,** o novo processo herdará a área de trabalho e a estação de janela de seu processo pai. Se **WinstationDesktop** for uma cadeia de caracteres vazia, o processo não herdará a área de trabalho e a estação de janela de seu processo pai. O sistema determina se uma nova área de trabalho e uma estação de janela devem ser criadas. Uma estação de janela é um objeto seguro que contém uma área de transferência, um conjunto de átomos globais e um grupo de objetos da área de trabalho. A estação de janela interativa atribuída à sessão de logon do usuário interativo também contém o teclado, o mouse e o dispositivo de exibição. Uma área de trabalho é um objeto seguro contido em uma estação de janela. Uma área de trabalho tem uma superfície de exibição lógica e contém janelas, menus e ganchos. Uma estação de janela pode ter várias áreas de trabalho. Somente as áreas de trabalho da estação de janela interativa podem ser visíveis e receber a entrada do usuário.

</dd> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")
</dt> </dl>

O deslocamento X do canto superior esquerdo de uma janela se uma nova janela for criada, em pixels. Os deslocamentos são do canto superior esquerdo da tela. Para processos de GUI, a posição especificada será usada na primeira vez que o novo processo chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobrecarada se o parâmetro *X* de **CreateWindow** for **CW \_ USEDEFAULT.**

> \[! Observação X\]  
> E **Y** não podem ser especificados independentemente.

 

</dd> <dt>

**XCountChars**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")
</dt> </dl>

Largura do buffer de tela em colunas de caracteres. Essa propriedade é usada para processos que criam uma janela do console e é ignorada em processos de GUI.

> [!Note]  
> **XCountChars** e **YCountChars** não podem ser especificados independentemente.

 

</dd> <dt>

**XSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")
</dt> </dl>

Largura de pixel de uma janela se uma nova janela for criada. Para processos de GUI, isso só será usado na primeira vez que o novo processo chamar [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobrecarada se o parâmetro nWidth de **CreateWindow** for **CW \_ USEDEFAULT.**

> [!Note]  
> **XSize** e **YSize** não podem ser especificados independentemente.

 

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY")
</dt> </dl>

Deslocamento de pixel do canto superior esquerdo de uma janela se uma nova janela for criada. Os deslocamentos são do canto superior esquerdo da tela. Para processos de GUI, a posição especificada é usada na primeira vez que o novo processo chama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobrecarada se o parâmetro *y* de **CreateWindow** for **CW \_ USEDEFAULT.**

> \[! Observação X\]  
> E **Y** não podem ser especificados independentemente.

 

</dd> <dt>

**YCountChars**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")
</dt> </dl>

Altura do buffer de tela em linhas de caracteres. Essa propriedade é usada para processos que criam uma janela de console, mas são ignoradas em processos de GUI.

> [!Note]  
> **XCountChars** e **YCountChars** não podem ser especificados de forma independente.

 

</dd> <dt>

**YSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de processo e estruturas de thread \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")
</dt> </dl>

Altura de pixel de uma janela se uma nova janela for criada. Para processos de GUI, isso é usado apenas na primeira vez que o novo processo chama [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para criar uma janela sobreposta se o parâmetro *nWidth* de **CreateWindow** for **\_ USEDEFAULT de peso variável**.

> [!Note]  
> **XSize** e **YSize** não podem ser especificados de forma independente.

 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe é derivada do [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).

Visão geral

O método [**Create**](create-method-in-class-win32-process.md) do [**\_ processo do Win32**](win32-process.md) permite configurar opções de inicialização para qualquer processo novo em execução em um computador. Por exemplo, você pode configurar um processo para que ele seja iniciado em uma janela "oculta", o que impede que um usuário veja e, possivelmente, interrompa-o. Se o processo for executado em uma janela de comando, você poderá configurar o tamanho, o título e as cores de primeiro plano e de plano de fundo da janela.

As opções de inicialização são configuradas usando a classe **Win32 \_ ProcessStartup** . **Win32 \_ ProcessStartup** é uma classe de tipo de método; a classe de tipo de método existe apenas para passar informações para um método. Nesse caso, todas as propriedades de uma instância do **Win32 \_ ProcessStartup** são passadas para uma instância do [**\_ processo Win32**](win32-process.md).

**Usando o Win32 \_ ProcessStartup**

1.  Crie uma instância do **Win32 \_ ProcessStartup**.
2.  Configure as propriedades da nova instância.
3.  Inclua a instância como parte do método de criação do [**\_ processo Win32**](win32-process.md) .

Por exemplo, se você tiver criado uma instância do **Win32 \_ ProcessStartup** chamada objConfig, passaria o nome do objeto no método Create da seguinte maneira:

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a>Exemplos

Você pode usar a classe **Win32 \_ ProcessStartup** para configurar várias opções de inicialização para um processo. Essas opções incluem, mas não se limitam a, como criar um processo em uma janela oculta e criar um processo de prioridade mais alta. O VBScript a seguir cria um processo em uma janela oculta.


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



O VBScript a seguir cria um processo de prioridade mais alta.


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



o exemplo de código VBScript a seguir cria um processo de Bloco de notas no computador local. **Win32 \_ ProcessStartup** é usado para definir as configurações do processo.


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
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

[**\_MethodParameterClass Win32**](win32-methodparameterclass.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> <dt>

[**\_\_ProviderHostQuotaConfiguration**](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[Tarefas do WMI: processos](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
