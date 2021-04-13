---
description: Para coletar informações de rastreamento para a infraestrutura do VSS, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Usando ferramentas de rastreamento com VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164497"
---
# <a name="using-tracing-tools-with-vss"></a>Usando ferramentas de rastreamento com VSS

Para coletar informações de rastreamento para a infraestrutura do VSS, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta tracelog. O VssTrace está disponível no SDK (Software Development Kit) do Microsoft Windows e pode ser usado para rastrear aplicativos VSS no Windows 7 e versões posteriores do sistema operacional Windows. Logman é um controlador de rastreamento para eventos de rastreamento e contadores de desempenho; Ele também pode ser usado para rastrear aplicativos VSS no Windows 7 e versões posteriores do sistema operacional Windows. O tracelog está incluído no Windows Driver Kit (WDK).

Para usar as ferramentas de rastreamento com o [ASR (recuperação automatizada do sistema)](using-vss-automated-system-recovery-for-disaster-recovery.md), consulte [usando ferramentas de rastreamento com aplicativos ASR](using-tracing-tools-with-vss-asr-applications.md).

> [!Note]  
> VssTrace, logman e tracelog All exigem privilégio de administrador.

 

Para obter informações sobre cada ferramenta, consulte as seguintes seções:

-   [Usando VssTrace](#using-vsstrace)
    -   [Opções de Command-Line de VssTrace](#vsstrace-command-line-options)
-   [Usando logman](#using-logman)
-   [Usando tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Usando VssTrace

Para executar a ferramenta VssTrace na linha de comando, use a seguinte sintaxe:

 *Opções de linha de comando* vsstrace

Para exibir a ajuda de linha de comando concisa para a ferramenta VssTrace, use a seguinte sintaxe:

**vsstrace-ajuda**

Para exibir a ajuda de linha de comando detalhada para a ferramenta VssTrace, use a seguinte sintaxe:

**vsstrace-ajuda de tudo**

### <a name="vsstrace-command-line-options"></a>Opções de Command-Line de VssTrace

A ferramenta VssTrace usa as seguintes opções de linha de comando:

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *sinalizadores*
</dt> <dd>

Habilite os módulos cujos sinalizadores são especificados pelo bitmask dos *sinalizadores* . Cada sinalizador corresponde a um módulo VSS. Se *flags* for zero, nenhum módulo será habilitado. Observe que a maioria dos módulos está habilitada por padrão. Essa opção pode ser combinada com a **+** opção de _módulo_ . Por exemplo, **vsstrace-f 0 + Writer + coord** desabilita o rastreamento de todos os módulos que estão habilitados por padrão e habilita o rastreamento de gravadores VSS e o serviço VSS. Como alternativa, **vsstrace + f 0xFFFF-coord** habilita o rastreamento de todos os módulos, exceto o serviço VSS.

> [!Note]  
> Se você usar a opção **-f** junto com a **+** opção de _módulo_ , o **-f** deverá aparecer antes da opção de **+** _módulo_ .

 

A tabela a seguir lista o nome do módulo e o sinalizador para cada módulo disponível.

| Módulo | Sinalizador       | Habilitado por padrão | Itens rastreados                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Sim                | Manipulação de exceção de C++.                                                                                                                       |
| COORD  | 0x00000002 | Sim                | O serviço VSS, que também é chamado de coordenador VSS.                                                                                    |
| SWPRV  | 0x00000004 | Sim                | O serviço do provedor de cópia de sombra do sistema do VSS.                                                                                                  |
| BUCOMP | 0x00000008 | Sim                | O solicitante do VSS e o processamento de metadados de backup.                                                                                             |
| WRITER | 0x00000010 | Sim                | Operações do gravador VSS e implementações do gravador hospedado do VSS, como o gravador de registro do Windows.                                             |
| VSSAPI | 0x00000020 | Sim                | Funções diversas da API do VSS exportadas pelo VSSAPI.DLL.                                                                                |
| HWDIAG | 0x00000040 | Sim                | Infraestrutura e operações do provedor de hardware do VSS.                                                                                          |
| ADMIN  | 0x00000080 | Sim                | Utilitários de linha de comando do VSS, como VSSADMIN.EXE e DISKSHADOW.EXE.                                                                           |
| VSSUI  | 0x00000100 | Sim                | A interface do usuário de configuração do Cópias de Sombra para Pastas Compartilhadas (UI). A interface do usuário está disponível apenas em sistemas operacionais Windows Server.         |
| TEST   | 0x00000200 | Sim                | Não aplicável. (Este módulo de rastreamento está reservado.)                                                                                            |
| IOCTL  | 0x00000400 | Sim                | Detalhes das operações FSCTL e IOCTL que o serviço VSS iniciou chamando a função [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) . |
| GERAL    | 0x00000800 | Sim                | Funções gerais do utilitário VSS, como alocadores, classes de cadeia de caracteres e operações de registro e volume.                                        |
| WRXML  | 0x00001000 | Não                 | Processamento de XML para metadados do gravador. Este módulo tem um nível muito alto de ruído.                                                               |
| VSSXML | 0x00002000 | Não                 | Classes base de processamento XML. Este módulo tem um nível muito alto de ruído.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Modulo_
</dt> <dd>

Habilite o módulo especificado pelo *módulo*. Mais de um módulo pode ser habilitado por vez. Para listar os módulos disponíveis, digite **vsstrace – módulos de ajuda** no prompt de linha de comando.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Modulo_
</dt> <dd>

Desabilite o módulo especificado pelo *módulo*. Para listar os módulos disponíveis, digite **vsstrace – módulos de ajuda** no prompt de linha de comando.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ pid** *ProcessId*
</dt> <dd>

Habilite o processo especificado por *ProcessId*. Para habilitar todos os processos, use " \* " para o valor de *ProcessId*. Mais de uma opção de **pid** pode ser especificada de cada vez. A ordem das opções determina quais processos estão habilitados ou desabilitados. Por exemplo, para habilitar apenas o processo cujo identificador de processo é 0xe8c, use **vsstrace-PID \* + pid 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*
</dt> <dd>

Desabilite o processo especificado por *ProcessId*. Para desabilitar todos os processos, use " \* " para o valor de *ProcessId*. Mais de uma opção de **pid** pode ser especificada de cada vez. A ordem das opções determina quais processos estão habilitados ou desabilitados. Por exemplo, para desabilitar todos os processos, exceto o processo cujo identificador de processo é 0xe8c, use **vsstrace-PID \* + pid 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ tid** *ThreadID*
</dt> <dd>

Habilite o thread especificado por *ThreadID*. Para habilitar todos os threads, use " \* " para o valor de *ThreadID*. Mais de uma opção de **tid** pode ser especificada de cada vez. A ordem das opções determina quais threads estão habilitados ou desabilitados. Por exemplo, para habilitar apenas o thread cujo identificador de processo é 0x31a, use **vsstrace-tid \* + tid 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadID*
</dt> <dd>

Desabilite o thread especificado por *ThreadID*. Para desabilitar todos os threads, use " \* " para o valor de *ThreadID*. Mais de uma opção de **tid** pode ser especificada de cada vez. A ordem das opções determina quais threads estão habilitados ou desabilitados. Por exemplo, para desabilitar todos os threads, exceto o thread cujo identificador de processo é 0x31a, use **vsstrace-tid \* + tid 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *nível*
</dt> <dd>

Use o nível de rastreamento especificado por *nível*. Quanto mais alto o nível, mais detalhada será a saída de rastreamento. Cada nível inclui todos os níveis inferiores. O nível padrão é 170. Os níveis a seguir estão disponíveis.



| Nível | Informações incluídas na saída do rastreamento |
|-------|------------------------------------------|
| 000   | Nenhum                                     |
| 020   | Erros fatais                             |
| 030   | Exceções sem tratamento                     |
| 040   | Errors                                   |
| 050   | Asserções                               |
| 060   | Warnings                                 |
| 080   | Tratamento de exceções                       |
| 100   | Atividade de log de eventos                       |
| 120   | Informações gerais                      |
| 140   | fluxo de código                                |
| 160   | Função Enter e Exit                  |
| 170   | Valores de retorno de função                   |
| 180   | Parâmetros de função (conciso)              |
| 190   | Parâmetros de função (detalhado)            |
| 200   | Nível de informações detalhadas 1              |
| 210   | Nível de informações detalhadas 2              |
| 220   | Nível de Informação Detalhado 3              |
| 230   | Nível de código rápido 1                        |
| 240   | Nível de código rápido 2                        |
| 250   | Nível de código rápido 3                        |
| 255   | Todos                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+ recuar**
</dt> <dd>

Recue a saída de rastreamento formatada em cada função e limite de subfunção.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-recuar**
</dt> <dd>

Não recue a saída de rastreamento formatada.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *EtlFile*
</dt> <dd>

Converta o arquivo de saída logman especificado por *EtlFile* em um formato de texto legível.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *arquivo_de_saída*
</dt> <dd>

Salve as informações de rastreamento no arquivo de saída especificado pelo *OutputFile*. Para obter o melhor desempenho, o arquivo de saída deve estar localizado em um volume que não faz parte da cópia de sombra.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-ajuda** *HelpOption*
</dt> <dd>

Exiba a ajuda da linha de comando conforme especificado por *HelpOption*. Os valores de *HelpOption* válidos são **módulos**, **níveis** e **todos**. A especificação de **módulos** faz com que os módulos sejam listados. A especificação de **níveis** faz com que os níveis disponíveis sejam listados. Especificar **All** faz com que a ajuda detalhada seja exibida. Se nenhuma opção for usada, a ajuda concisa será exibida.

</dd> </dl>

## <a name="using-logman"></a>Usando logman

O procedimento a seguir descreve como usar o logman com seu aplicativo VSS.

**Para usar logman com seu aplicativo VSS**

1.  Use o seguinte comando para iniciar o rastreamento:

    **logman start VSS-o** *x: \\ * * * VSS. etl-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xFFF 170**

    > [!Note]  
    > Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado.

     

2.  Use o seguinte comando para interromper o rastreamento:

    **logman parar VSS-ETS**

O arquivo de log de rastreamento é *x: \\* VSS. etl.

Para obter mais informações sobre a ferramenta Logman, consulte [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).

## <a name="using-tracelog"></a>Usando tracelog

O procedimento a seguir descreve como usar o tracelog.

**Para usar o tracelog**

1.  Crie um arquivo de texto chamado VSS. CTL que contenha apenas o seguinte texto:

    **VSS 9138500e-3648-4edb-aa4c-859e9f7b7c38**

2.  Use o seguinte comando para iniciar o rastreamento:

    **tracelog-iniciar VSS-f** *x: \\ * * * VSS. etl-GUID VSS. CTL-Flag 0xAA de nível 0xFF**

    > [!Note]  
    > Substitua "x: \\ " pelo caminho para o diretório em que você deseja que o arquivo de log de rastreamento seja armazenado.

     

3.  Use o seguinte comando para interromper o rastreamento:

    **tracelog-parar VSS**

O arquivo de log de rastreamento é *x: \\* VSS. etl.

Para obter mais informações sobre a ferramenta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).

 

 
