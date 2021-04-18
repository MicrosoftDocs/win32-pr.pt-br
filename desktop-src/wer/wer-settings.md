---
title: Configurações WER
description: Configurações para personalizar a experiência de relatório de problemas. Todas essas configurações podem ser definidas usando Política de Grupo. Alguns também podem ser alterados na central de ações para Windows 7 e Windows 8. Para o Windows 10, use a função de pesquisa em configurações para localizar exibir configurações avançadas do sistema.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Relatório de Erros do Windows de relatório de erros do Windows, configurações
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/13/2021
ms.locfileid: "105751388"
---
# <a name="wer-settings"></a>Configurações WER

Relatório de Erros do Windows (WER) fornece muitas configurações para personalizar a experiência de relatório de problemas. Todas essas configurações podem ser definidas usando Política de Grupo. Alguns também podem ser alterados na **central de ações** para Windows 7 e Windows 8. Para o Windows 10, use a função de pesquisa em configurações para localizar **exibir configurações avançadas do sistema**. As configurações do WER estão localizadas em uma das seguintes subchaves do registro:

-   **HKEY \_ Software de \_ usuário atual** \\  \\ **Microsoft** \\ **Windows** \\ **relatório de erros do Windows**
-   **HKEY \_ Software do \_ computador local** \\  \\ **Microsoft** \\ **Windows** \\ **relatório de erros do Windows**

## <a name="windows-error-reporting-subkey"></a>Subchave Relatório de Erros do Windows

<dl> <dt>

<span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>

0-desabilitar limitação de bypass de dados. Se o bypass estiver desabilitado ou não estiver configurado como uma configuração de política, o WER restringirá os dados por padrão. O WER não carrega mais de um arquivo CAB para um relatório que contém dados sobre os mesmos tipos de evento.

</dd> <dd>

1-Habilitar limitação de bypass de dados. O WER não acelera os dados. O WER carrega arquivos CAB adicionais que podem conter dados sobre os mesmos tipos de evento que um relatório carregado anteriormente.

</dd> </dl>

Se deseja habilitar o bypass da limitação de dados do cliente do WER

</dd> <dt>

<span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>1-somente parâmetros (padrão no Windows 7)</dd> <dd>2-todos os dados (padrão no Windows Vista)</dd> </dl>

Se os parâmetros devem ser arquivados somente ou todos os dados

</dd> <dt>

<span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Autorização \\ de consentimento**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>1-sempre perguntar (padrão)</dd> <dd>2-somente parâmetros</dd> <dd>3-parâmetros e dados seguros</dd> <dd>4-todos os dados</dd> </dl>

Opção de consentimento padrão

</dd> <dt>

<span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**DefaultOverrideBehavior de consentimento \\**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-o consentimento vertical substituirá o consentimento padrão (padrão)</dd> <dd>1-o consentimento padrão substituirá o consentimento específico do aplicativo</dd> </dl>

Se o consentimento padrão substitui o consentimento vertical

</dd> <dt>

<span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Vertical do consentimento \\ \[\]**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>1-sempre perguntar (padrão)</dd> <dd>2-somente parâmetros</dd> <dd>3-parâmetros e dados seguros</dd> <dd>4-todos os dados</dd> </dl>

Opção de consentimento para o plug-in do WER

</dd> <dt>

<span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**
</dt> <dd>

**REG \_ sz**

O caminho do diretório

Diretório de destino no servidor

</dd> <dt>

<span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**
</dt> <dd>

**REG \_ DWORD**

O número da porta

Número da porta a ser usada com o servidor corporativo

</dd> <dt>

<span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**
</dt> <dd>

**REG \_ sz**

O nome do servidor

Nome do servidor corporativo

</dd> <dt>

<span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-não (padrão)</dd> <dd>1 – Sim</dd> </dl>

Se a autenticação integrada do Windows deve ser usada

</dd> <dt>

<span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-não (padrão)</dd> <dd>1 – Sim</dd> </dl>

Se o SSL deve ser usado

</dd> <dt>

<span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ EXEName \] (substitua " \[ EXEName \] " por um nome real de um arquivo. exe, por exemplo, "notepad.exe")**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:

<dl> <dd>0-processos com um nome de imagem executável de **\[ EXEName \]** não exigem que o usuário escolha **depurar** ou **continuar** (padrão)</dd> <dd>1-processos com um nome de imagem executável de **\[ EXEName \]** exigem que o usuário escolha **depurar** ou **continuar**</dd> </dl> </dd> <dt>

<span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " é o nome do valor literal)**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:

<dl> <dd>0-todos os processos, exceto aqueles especificados explicitamente na configuração **DebugApplications \\ \[ \] EXEName** não exigem que o usuário escolha **depurar** ou **continuar** (padrão)</dd> <dd>1-todos os processos, exceto aqueles especificados explicitamente na configuração **DebugApplications \\ \[ \] EXEName** exigem que o usuário escolha **depurar** ou **continuar**</dd> </dl> </dd> <dt>

<span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0 - Habilitado</dd> <dd>1 - Desabilitado</dd> </dl>

Habilitar ou desabilitar o arquivo morto

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-habilitado (padrão)</dd> <dd>1 - Desabilitado</dd> </dl>

Habilitar ou desabilitar o WER

</dd> <dt>

<span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0 - Habilitado</dd> <dd>1 - Desabilitado</dd> </dl>

Habilitar ou desabilitar o enfileiramento de relatórios

</dd> <dt>

<span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-interface do usuário (padrão)</dd> <dd>1-sem interface do usuário</dd> </dl>

Habilitar ou desabilitar a interface do usuário do WER

</dd> <dt>

<span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-enviar (padrão)</dd> <dd>1-não enviar</dd> </dl>

Se deseja impedir o envio de dados de segundo nível

</dd> <dt>

<span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ Nome do aplicativo ExcludedApplications\]**
</dt> <dd>

**REG \_ sz**

Usar [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)

Lista de aplicativos excluídos

</dd> <dt>

<span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-não (padrão)</dd> <dd>1 – Sim</dd> </dl>

Se deseja enviar todos os relatórios para a fila do usuário

</dd> <dt>

<span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\** Nome do **aplicativo DumpFolder ou LocalDumps \\ \[ \] \\ DumpFolder**
</dt> <dd>

**REG \_ expande \_ sz**

O caminho do diretório. O valor padrão é% LOCALAPPDATA% \\ CrashDumps. Se o padrão não for usado, o aplicativo deverá garantir que a pasta tenha uma ACL suficiente.

**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** . Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com Service Pack 1 (SP1).

O caminho onde os arquivos de despejo devem ser armazenados.

Observe que as configurações por processo substituirão as configurações globais existentes para obter mais informações, consulte [coletando despejos de User-Mode](collecting-user-mode-dumps.md).

Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.

</dd> <dt>

<span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\** Nome do **aplicativo DumpCount ou LocalDumps \\ \[ \] \\ DumpCount**
</dt> <dd>

**REG \_ DWORD**

O número máximo. O padrão é 10. Quando o valor máximo for excedido, o arquivo de despejo mais antigo na pasta será substituído pelo novo arquivo de despejo.

**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** . Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com SP1.

O número máximo de arquivos de despejo na pasta.

Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.

</dd> <dt>

<span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ Dumptype** ou **LocalDumps do nome do aplicativo de \\ \[ \] \\ decarregamentotype**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0-despejo personalizado</dd> <dd>1-minidespejo (padrão)</dd> <dd>2-despejo completo</dd> </dl>

**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** . Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com SP1.

O tipo de despejo.

Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.

</dd> <dt>

<span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\** Nome do **aplicativo CustomDumpFlags ou LocalDumps \\ \[ \] \\ CustomDumpFlags**
</dt> <dd>

**REG \_ DWORD**

Um ou mais valores da enumeração [**de \_ tipo de minidespejo**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) . O padrão é {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.

**Windows Vista:** Não há suporte para os valores de registro na chave **LocalDumps** . Observe que esse comportamento mudou com o Windows Server 2008 e o Windows Vista com SP1.

As opções de despejo personalizado a serem usadas. Esse valor é usado somente quando **dumptype** é definido como 0.

Essa configuração não tem suporte no hive **HKEY \_ Current \_ User** Registry.

</dd> <dt>

<span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**
</dt> <dd>

**REG \_ DWORD**

Valores possíveis:<dl> <dd>0 – habilitado (padrão)</dd> <dd>1 – desabilitado</dd> </dl>

Habilitar ou desabilitar o registro em log

</dd> <dt>

<span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**
</dt> <dd>

**REG \_ DWORD**

Intervalo de valores possíveis: 1 a 5.000. O padrão é 1000.

Tamanho máximo do arquivo morto, em arquivos

</dd> <dt>

<span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**
</dt> <dd>

**REG \_ DWORD**

Intervalo de valores possíveis: 1 a 500. O padrão é 50.

Tamanho máximo da fila

</dd> <dt>

<span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**
</dt> <dd>

**REG \_ DWORD**

Número de dias

Intervalo entre lembretes ao usuário para verificar se há soluções, em dias

</dd> <dt>

<span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ nome do pwszOutOfProcessCallbackDll incluindo caminho\]**
</dt> <dd>

**REG \_ DWORD**

O conteúdo do valor é ignorado.

O nome do valor é usado para buscar o valor de pwszOutOfProcessCallbackDll.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para esse valor de registro.

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a>Configurações de relatórios de kernel do WER Live

As configurações de relatórios do kernel ao vivo do WER, que são descritas a seguir, estão localizadas na seguinte subchave do registro:

-   **HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **CrashControl**

## <a name="fulllivekernelreports-subkey"></a>Subchave FullLiveKernelReports

<dl> <dt>

<span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

O limite (em horas) de com que frequência qualquer único componente pode criar um despejo ao vivo completo. Esse valor deve ser maior ou igual a **SystemThrottleThreshold**. A definição de ambas como zero (0) desabilitará toda a limitação baseada em tempo. O padrão é 168 (7 dias).

</dd> <dt>

<span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**
</dt> <dd>

**REG \_ DWORD**

O número máximo de despejos ao vivo completos que podem estar no disco em um determinado momento. O padrão é 1. Definir esse valor como zero (0) desativará o recurso de despejo dinâmico.

</dd> <dt>

<span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**
</dt> <dd>

**REG \_ QWORD**

Um [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que indica o último tempo de relatório ao vivo completo, para o sistema ou um reportType específico. Isso é usado para calcular se um limite de política foi atendido.

</dd> <dt>

<span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**
</dt> <dd>

**REG \_ DWORD**

O limite (em horas) de quantas vezes qualquer componente no sistema pode criar um despejo ao vivo completo. O padrão é 120 (5 dias).

</dd> </dl>

## <a name="livekernelreports-subkey"></a>Subchave LiveKernelReports

<dl> <dt>

<span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**
</dt> <dd>

**REG \_ sz**


O local de armazenamento Redirecionado de relatórios de kernel ao vivo. O local padrão é%systemroot%\LiveKernelReports. Esse valor deve ser um caminho válido. O caminho deve estar no formato NT Path. Por exemplo, \? ? \c: \LiveDumpsFolder.  Para obter mais informações sobre formatos de caminho, consulte  [formatos de caminho de arquivo em sistemas Windows](/dotnet/standard/io/file-path-formats).

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do WER](wer-reference.md)
</dt> </dl>

 

 
