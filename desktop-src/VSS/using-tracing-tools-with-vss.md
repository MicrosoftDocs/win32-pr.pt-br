---
description: Para coletar informações de rastreamento para a infraestrutura do VSS, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta Tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Usando ferramentas de rastreamento com VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34b79fa91bad210b20d14c2655368f4a5494efe4b462a7a0b93ea672b049d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937738"
---
# <a name="using-tracing-tools-with-vss"></a>Usando ferramentas de rastreamento com VSS

Para coletar informações de rastreamento para a infraestrutura do VSS, você pode usar a ferramenta VssTrace, a ferramenta Logman ou a ferramenta Tracelog. O VssTrace está disponível no SDK (Software Development Kit) do Microsoft Windows e pode ser usado para rastrear aplicativos VSS no Windows 7 e versões posteriores do sistema operacional Windows. O Logman é um controlador de rastreamento para eventos de rastreamento e contadores de desempenho; ele também pode ser usado para rastrear aplicativos VSS no Windows 7 e versões posteriores do sistema operacional Windows sistema operacional. O rastreamento está incluído no WDK (Kit Windows Driver).

Para usar ferramentas de rastreamento com o [ASR (Automated Recuperação do Sistema),](using-vss-automated-system-recovery-for-disaster-recovery.md)consulte Using Tracing Tools with ASR Applications ( Usando ferramentas de rastreamento [com aplicativos ASR).](using-tracing-tools-with-vss-asr-applications.md)

> [!Note]  
> VssTrace, Logman e Tracelog exigem privilégio de administrador.

 

Para obter informações sobre cada ferramenta, consulte as seguintes seções:

-   [Usando o VssTrace](#using-vsstrace)
    -   [Opções de Command-Line VssTrace](#vsstrace-command-line-options)
-   [Usando o Logman](#using-logman)
-   [Usando o Tracelog](#using-tracelog)

## <a name="using-vsstrace"></a>Usando o VssTrace

Para executar a ferramenta VssTrace na linha de comando, use a seguinte sintaxe:

opções de linha de comando **vsstrace** 

Para exibir a ajuda concisa de linha de comando para a ferramenta VssTrace, use a seguinte sintaxe:

**vsstrace -help**

Para exibir a ajuda de linha de comando detalhada para a ferramenta VssTrace, use a seguinte sintaxe:

**vsstrace -help all**

### <a name="vsstrace-command-line-options"></a>Opções de Command-Line VssTrace

A ferramenta VssTrace usa as seguintes opções de linha de comando:

<dl> <dt>

<span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**Sinalizadores -f** 
</dt> <dd>

Habilita os módulos cujos sinalizadores são especificados pelo bitmask *Flags.* Cada sinalizador corresponde a um módulo VSS. Se *Sinalizadores* for zero, nenhum módulo será habilitado. Observe que a maioria dos módulos está habilitada por padrão. Essa opção pode ser combinada com a **+** _opção Módulo._ Por exemplo, **vsstrace -f 0 +WRITER +COORD** desabilita o rastreamento de todos os módulos habilitados por padrão e habilita o rastreamento de autores VSS e o serviço VSS. Como alternativa, **vsstrace +f 0xffff -COORD** permite o rastreamento de todos os módulos, exceto o serviço VSS.

> [!Note]  
> Se você usar a **opção -f** junto com a opção **+** _Module,_ **o -f** deverá aparecer antes da **+** _opção Módulo._

 

A tabela a seguir lista o nome e o sinalizador do módulo para cada módulo disponível.

| Módulo | Sinalizador       | Habilitado por padrão | Itens rastreados                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| EXCEPT | 0x00000001 | Sim                | Tratamento de exceção do C++.                                                                                                                       |
| Coord  | 0x00000002 | Sim                | O serviço VSS, que também é chamado de coordenador do VSS.                                                                                    |
| SWPRV  | 0x00000004 | Sim                | O serviço Provedor de Cópias de Sombra do Sistema VSS.                                                                                                  |
| BUCOMP | 0x00000008 | Sim                | O solicitante do VSS e o processamento de metadados de backup.                                                                                             |
| WRITER | 0x00000010 | Sim                | Operações do vsS writer e implementações de writer hospedados do VSS, como o Windows do Registro.                                             |
| VSSAPI | 0x00000020 | Sim                | Funções diversas da API do VSS exportadas por VSSAPI.DLL.                                                                                |
| HWDIAG | 0x00000040 | Sim                | Infraestrutura e operações do provedor de hardware VSS.                                                                                          |
| ADMIN  | 0x00000080 | Sim                | Utilitários de linha de comando do VSS, como VSSADMIN.EXE e DISKSHADOW.EXE.                                                                           |
| VSSUI  | 0x00000100 | Sim                | A interface Cópias de Sombra para Pastas Compartilhadas interface do usuário de configuração do usuário. A interface do usuário está disponível somente em sistemas operacionais Windows Server.         |
| TEST   | 0x00000200 | Sim                | Não aplicável. (Este módulo de rastreamento é reservado.)                                                                                            |
| Ioctl  | 0x00000400 | Sim                | Detalhes das operações FSCTL e IOCTL iniciadas pelo serviço VSS chamando a [**função DeviceIoControl.**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) |
| Gen    | 0x00000800 | Sim                | Funções gerais do utilitário VSS, como alocadores, classes de cadeia de caracteres e operações de registro e volume.                                        |
| WRXML  | 0x00001000 | Não                 | Processamento XML para metadados de autor. Este módulo tem um nível muito alto de ruído.                                                               |
| VSSXML | 0x00002000 | Não                 | Classes base de processamento XML. Este módulo tem um nível muito alto de ruído.                                                                      |



 

</dd> <dt>

<span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Módulo_
</dt> <dd>

Habilita o módulo especificado pelo *Módulo*. Mais de um módulo pode ser habilitado por vez. Para listar os módulos disponíveis, digite **módulos vsstrace –help** no prompt de linha de comando.

</dd> <dt>

<span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Módulo_
</dt> <dd>

Desabilite o módulo especificado pelo *Módulo*. Para listar os módulos disponíveis, digite **módulos vsstrace –help** no prompt de linha de comando.

</dd> <dt>

<span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*
</dt> <dd>

Habilita o processo especificado por *ProcessId.* Para habilitar todos os processos, use \* " " para o valor de *ProcessId*. Mais de uma **opção pid** pode ser especificada por vez. A ordem das opções determina quais processos estão habilitados ou desabilitados. Por exemplo, para habilitar apenas o processo cujo identificador de processo 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.

</dd> <dt>

<span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*
</dt> <dd>

Desabilite o processo especificado por *ProcessId.* Para desabilitar todos os processos, use \* " " para o valor de *ProcessId*. Mais de uma **opção pid** pode ser especificada por vez. A ordem das opções determina quais processos estão habilitados ou desabilitados. Por exemplo, para desabilitar todos os processos, exceto o processo cujo identificador de processo é 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.

</dd> <dt>

<span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**ThreadId +tid** 
</dt> <dd>

Habilita o thread especificado por *ThreadId.* Para habilitar todos os threads, use \* " " para o valor de *ThreadId*. Mais de uma **opção tid** pode ser especificada por vez. A ordem das opções determina quais threads estão habilitados ou desabilitados. Por exemplo, para habilitar apenas o thread cujo identificador de processo 0x31a, use **vsstrace -tid \* +tid 0x31a**.

</dd> <dt>

<span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*
</dt> <dd>

Desabilite o thread especificado por *ThreadId.* Para desabilitar todos os threads, use \* " " para o valor de *ThreadId*. Mais de uma **opção tid** pode ser especificada por vez. A ordem das opções determina quais threads estão habilitados ou desabilitados. Por exemplo, para desabilitar todos os threads, exceto o thread cujo identificador de processo é 0x31a, use **vsstrace -tid \* +tid 0x31a**.

</dd> <dt>

<span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*
</dt> <dd>

Use o nível de rastreamento especificado pelo *Nível*. Quanto maior o nível, mais detalhada será a saída do rastreamento. Cada nível inclui todos os níveis inferiores. O nível padrão é 170. Os níveis a seguir estão disponíveis.



| Nível | Informações incluídas na saída de rastreamento |
|-------|------------------------------------------|
| 000   | Nenhum                                     |
| 020   | Erros fatais                             |
| 030   | Exceções sem tratamento                     |
| 040   | Erros                                   |
| 050   | Asserções                               |
| 060   | Avisos                                 |
| 080   | Tratamento de exceções                       |
| 100   | Atividade do Log de Eventos                       |
| 120   | Informações gerais                      |
| 140   | fluxo de código                                |
| 160   | Entrada e saída da função                  |
| 170   | Valores de retorno da função                   |
| 180   | Parâmetros de função (terse)              |
| 190   | Parâmetros de função (detalhados)            |
| 200   | Nível de informações detalhado 1              |
| 210   | Nível de informações detalhado 2              |
| 220   | Nível de informações detalhado 3              |
| 230   | Nível de código rápido 1                        |
| 240   | Nível de código rápido 2                        |
| 250   | Nível de código rápido 3                        |
| 255   | Tudo                                      |



 

</dd> <dt>

<span id="_indent"></span><span id="_INDENT"></span>**+recuo**
</dt> <dd>

Recua a saída de rastreamento formatada em cada função e limite de subfunção.

</dd> <dt>

<span id="-indent"></span><span id="-INDENT"></span>**-recuo**
</dt> <dd>

Não recua a saída de rastreamento formatada.

</dd> <dt>

<span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*
</dt> <dd>

Converta o arquivo de saída do Logman especificado *por EtlFile* em um formato de texto acessível.

</dd> <dt>

<span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*
</dt> <dd>

Salve as informações de rastreamento no arquivo de saída especificado por *OutputFile*. Para melhor desempenho, o arquivo de saída deve estar localizado em um volume que não faz parte da cópia de sombra.

</dd> <dt>

<span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*
</dt> <dd>

Exibe a ajuda de linha de comando, conforme especificado por *HelpOption*. Os valores *válidos de HelpOption* são **módulos**, **níveis** e **todos**. Especificar **módulos faz** com que os módulos sejam listados. Especificar níveis **faz** com que os níveis disponíveis sejam listados. Especificar tudo **faz** com que a ajuda detalhada seja exibida. Se nenhuma opção for usada, a ajuda concisa será exibida.

</dd> </dl>

## <a name="using-logman"></a>Usando o Logman

O procedimento a seguir descreve como usar o Logman com seu aplicativo VSS.

**Para usar o Logman com seu aplicativo VSS**

1.  Use o seguinte comando para iniciar o rastreamento:

    **logman start vss -o** *x: \\ ***vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170**

    > [!Note]  
    > Substitua "x: " pelo caminho para o diretório em \\ que você gostaria que o arquivo de log de rastreamento fosse armazenado.

     

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

 

 
