---
description: A \_ classe WMI singleton do Win32 WMISetting contém os parâmetros operacionais para o serviço WMI. Essa classe pode ter apenas uma instância, que sempre existe para cada sistema Windows e não pode ser excluída. Não é possível criar instâncias adicionais.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Classe Win32_WMISetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMISetting
- Win32_WMISetting.Caption
- Win32_WMISetting.Description
- Win32_WMISetting.SettingID
- Win32_WMISetting.ASPScriptDefaultNamespace
- Win32_WMISetting.ASPScriptEnabled
- Win32_WMISetting.AutorecoverMofs
- Win32_WMISetting.AutoStartWin9X
- Win32_WMISetting.BackupInterval
- Win32_WMISetting.BackupLastTime
- Win32_WMISetting.BuildVersion
- Win32_WMISetting.DatabaseDirectory
- Win32_WMISetting.DatabaseMaxSize
- Win32_WMISetting.EnableAnonWin9xConnections
- Win32_WMISetting.EnableEvents
- Win32_WMISetting.EnableStartupHeapPreallocation
- Win32_WMISetting.HighThresholdOnClientObjects
- Win32_WMISetting.HighThresholdOnEvents
- Win32_WMISetting.InstallationDirectory
- Win32_WMISetting.LastStartupHeapPreallocation
- Win32_WMISetting.LoggingDirectory
- Win32_WMISetting.LoggingLevel
- Win32_WMISetting.LowThresholdOnClientObjects
- Win32_WMISetting.LowThresholdOnEvents
- Win32_WMISetting.MaxLogFileSize
- Win32_WMISetting.MaxWaitOnClientObjects
- Win32_WMISetting.MaxWaitOnEvents
- Win32_WMISetting.MofSelfInstallDirectory
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 8f94524d18074e3a35c7bcad09e9b9fba80e8470
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826171"
---
# <a name="win32_wmisetting-class"></a>\_Classe Win32 WMISetting

A [classe WMI](../wmisdk/retrieving-a-class.md) singleton do **Win32 \_ WMISetting** contém os parâmetros operacionais para o serviço WMI. Essa classe pode ter apenas uma instância, que sempre existe para cada sistema Windows e não pode ser excluída. Não é possível criar instâncias adicionais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Singleton, Dynamic, Provider("WBEMCORE"), UUID("{A83EF166-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMISetting : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  string   ASPScriptDefaultNamespace = "\\\\root\\cimv2";
  boolean  ASPScriptEnabled;
  string   AutorecoverMofs[];
  uint32   AutoStartWin9X;
  uint32   BackupInterval;
  datetime BackupLastTime;
  string   BuildVersion;
  string   DatabaseDirectory;
  uint32   DatabaseMaxSize;
  boolean  EnableAnonWin9xConnections;
  boolean  EnableEvents;
  boolean  EnableStartupHeapPreallocation;
  uint32   HighThresholdOnClientObjects;
  uint32   HighThresholdOnEvents;
  string   InstallationDirectory;
  uint32   LastStartupHeapPreallocation;
  string   LoggingDirectory;
  uint32   LoggingLevel;
  uint32   LowThresholdOnClientObjects;
  uint32   LowThresholdOnEvents;
  uint32   MaxLogFileSize;
  uint32   MaxWaitOnClientObjects;
  uint32   MaxWaitOnEvents;
  string   MofSelfInstallDirectory;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ WMISetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ WMISetting** tem essas propriedades.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| padrão namespace")
</dt> </dl>

Namespace de script padrão. Essa propriedade contém o namespace usado por chamadas da API de script para WMI se nenhum for especificado pelo chamador.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_** \\  \\ Namespace padrão do software do computador local **Microsoft** \\ **WBEM** \\ **scripting \|**    

Exemplo: raiz \\ cimv2

Para obter um exemplo de script que usa essa propriedade, consulte a seção comentários.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ scripting \| enable for ASP")
</dt> </dl>

Se **for true**, o script WMI poderá ser usado em páginas de Active Server (ASP). Essa propriedade é válida em sistemas que executam apenas versões sem suporte do Windows. Para sistemas Windows com suporte, o script WMI sempre é permitido no ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Recover MOFs")
</dt> </dl>

Lista de nomes de arquivos MOF totalmente qualificados usados para inicializar ou recuperar o repositório WMI. A lista determina a ordem na qual os arquivos MOF são compilados.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| AutoRecuperação MOFs**    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

Não há suporte.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**Não iniciar** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Início automática** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Iniciar na reinicialização** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**BackupInterval que**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| \\ \\ limite do intervalo de backup do Microsoft \\ \\ WBEM \\ \\ CIMOM software Win32Registry \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Não há suporte. Em vez disso, faça backup do repositório WMI manualmente.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| time Functions \| GetTimeZoneInformation")
</dt> </dl>

Data e hora em que o último backup foi executado.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| Build")
</dt> </dl>

Informações de versão para o serviço WMI atualmente instalado.

Período de tempo decorrido entre os backups do banco de dados WMI.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ Build do \_ computador local** \\ **software** \\ **Microsoft** \\ **WBEM \|**

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório de \\ \\ repositório do Microsoft \\ \\ WBEM \\ \\ CIMOM software Win32Registry \| ")
</dt> </dl>

Caminho do diretório que contém o repositório WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max DB size"), [**Units**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Tamanho máximo do repositório WMI.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

Não há suporte.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

Se **for true**, o subsistema de eventos do WMI deverá ser habilitado.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

Se **for true**, o WMI criará um heap pré-alocado com o tamanho do valor **LASTSTARTUPHEAPPREALLOCATION** quando o WMI for inicializado.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| alto Threshold nos objetos cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")
</dt> </dl>

Taxa máxima em que os objetos criados pelo provedor podem ser entregues aos clientes. Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI mantém objetos em filas antes de entregá-los aos consumidores. Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponda ao provedor. Se a memória mantida por objetos não coletados atingir **LowThresholdOnObjects**, o WMI reduzirá a adição de novos objetos à fila. Se os eventos não coletados continuarem a ser acumulados e a espera máxima de entrega de eventos em **MaxWaitOnClientObjects** for atingida enquanto a memória usada estiver no valor em **HIGHTHRESHOLDONCLIENTOBJECTS**, o WMI não aceitará mais objetos de provedores e retornará o **WBEM \_ e a \_ \_ \_ memória insuficiente** para os clientes.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ de software Microsoft \\ \\ WBEM \\ \\ CIMOM \| limite alto nos eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Taxa máxima na qual os eventos devem ser entregues aos clientes. Para acomodar diferenciais de velocidade entre provedores e clientes, os eventos de filas do WMI antes de entregá-los aos consumidores. Para obter mais eficiência, os consumidores devem coletar os eventos em um ritmo que corresponda ao provedor. Se a memória mantida por eventos não coletados atingir **LowThresholdOnObjects**, o WMI reduzirá a adição de novos eventos na fila. Se os eventos não coletados continuarem a ser acumulados e a espera máxima de entrega de eventos em **MaxWaitOnEvents** for atingida enquanto a memória usada estiver no valor em **HighThresholdOnEvents**, o WMI não aceitará mais eventos de provedores e retornará o **WBEM \_ e a \_ \_ \_ memória insuficiente** para os clientes.

> [!Note]  
> A limitação só é feita para consumidores de eventos permanentes, portanto, os consumidores temporários não devem esperar a limitação quando os eventos são submetidos a backup na fila de eventos internos do WMI.

 

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| limite alto nos objetos cliente (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório de \\ \\ instalação do Microsoft WBEM software Win32Registry \\ \\ \| ")
</dt> </dl>

Caminho do diretório em que o software WMI foi instalado. O local padrão é \\ System32 \\ WBEM.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_** Diretório de \\  \\ **instalação do software Microsoft** \\ **WBEM \|** do computador local

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho do heap pré-alocado criado pelo WMI durante a inicialização.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| diretório de \\ \\ log do Microsoft \\ \\ WBEM \\ \\ CIMOM software Win32Registry \| ")
</dt> </dl>

Caminho do diretório que contém o local dos arquivos de log do sistema WMI.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_** Diretório de log do \\  \\ **Microsoft** \\ **WBEM \| CIMOM \| do** software de computador local

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| log")
</dt> </dl>

Habilitação do log de eventos e o nível de detalhamento do log usado.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_** Registro em \\  \\ **log do Microsoft** \\ **WBEM \| CIMOM \|** no software da máquina local

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Desativado** (0)


</dt> <dd></dd> <dt>

<span id="Error_logging"></span><span id="error_logging"></span><span id="ERROR_LOGGING"></span>

**Log de erros** (1)


</dt> <dd></dd> <dt>

<span id="Verbose_Error_logging"></span><span id="verbose_error_logging"></span><span id="VERBOSE_ERROR_LOGGING"></span>

**Log de erros detalhado** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**LowThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ de software Microsoft \\ \\ WBEM \\ \\ CIMOM \| limite baixo em objetos de cliente"), [**unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")
</dt> </dl>

Taxa na qual o WMI começa a reduzir a criação de novos objetos criados para clientes. Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI mantém objetos em filas antes de entregá-los aos consumidores. Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponda ao provedor. Se a taxa de solicitações de objetos atingir **LowThresholdOnClientObjects**, o WMI reduzirá gradualmente a criação de novos objetos para corresponder à taxa de uso do cliente. Essa lentidão começa quando a taxa na qual os objetos estão sendo criados excede o valor dessa propriedade. Consulte **HighThresholdOnClientObjects**.

Essa propriedade reflete o valor do registro.

**Chave \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| limite alto nos objetos cliente (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| \\ \\ de software Microsoft \\ \\ WBEM \\ \\ CIMOM \| limite baixo nos eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Taxa na qual o WMI começa a reduzir a entrega de novos eventos. Para acomodar diferenciais de velocidade entre provedores e clientes, os eventos de filas do WMI antes de entregá-los aos consumidores. Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponda ao provedor. Se a fila ficar fora de controle, as restrições de WMI — ficarão mais lentas — a entrega de eventos gradualmente para alinhar com a taxa do cliente. Essa lentidão começa quando a taxa na qual os eventos são gerados excede o valor dessa propriedade. Consulte **HighThresholdOnEvents**.

> [!Note]  
> A limitação só é feita para consumidores de eventos permanentes, portanto, os consumidores temporários não devem esperar a limitação quando os eventos são submetidos a backup na fila de eventos internos do WMI.

 

Essa propriedade reflete o valor do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| limite alto nos objetos cliente {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| tamanho máximo do arquivo de log"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho máximo dos arquivos de log produzidos pelo serviço WMI.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_** \\  \\  \\ **\| \| Tamanho máximo do arquivo de log do Microsoft WBEM CIMOM** software do computador local

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max em eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")
</dt> </dl>

Quantidade de tempo que um objeto recém-criado espera para ser usado pelo cliente antes de ser descartado e um valor de erro é retornado. Essa propriedade interage com as propriedades **LowThresholdOnClientObjects** e **HighThresholdOnClientObjects** para limitação — lentidão – a entrega de objetos aos consumidores quando o consumidor está recebendo os objetos muito lentamente.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry de \| software \\ \\ Microsoft \\ \\ WBEM \\ \\ CIMOM \| Max em eventos"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")
</dt> </dl>

Quantidade de tempo para o qual um evento enviado a um cliente é colocado na fila antes de ser Descartado. Essa propriedade interacts0 com **LowThresholdOnEvents** e **HighThresholdOnEvents** para a limitação — retardamento — a entrega de objetos aos consumidores quando o consumidor está recebendo os objetos muito lentamente.

Essa propriedade reflete o valor do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \| máx. de eventos (MS)**    

</dd> <dt>

**MofSelfInstallDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ WBEM \| MOF Self-Install Directory")
</dt> </dl>

Caminho do diretório para aplicativos que instalam arquivos MOF no repositório do WMI. O WMI compila automaticamente todos os arquivos MOF colocados nesse diretório e, dependendo de seu sucesso, move o MOF para um subdiretório rotulado bom ou ruim. Se o \# comando [pragma autoautorecover](../wmisdk/pragma-autorecover.md) for incluído, o nome de arquivo totalmente qualificado será adicionado à lista **AUTORECOVERMOFS** usada quando o WMI estiver inicializando ou recuperando o repositório. A lista determina a ordem na qual MOFs são compilados.

Essa propriedade reflete o valor na chave do registro.

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM \| CIMOM \| MOF Self = diretório de instalação**

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ WMISetting** é derivada da [**\_ configuração de CIM**](cim-setting.md). Somente uma instância dessa classe pode existir em um computador.

Saber como o WMI é configurado em um computador pode ser muito útil quando você está Depurando scripts ou Solucionando problemas com o próprio serviço WMI. Por exemplo, muitos scripts WMI são escritos sob a suposição de que raiz \\ cimv2 é o namespace padrão no computador de destino. Como resultado, os criadores de script que precisam acessar uma classe em "raiz \\ CIMv2" geralmente não incluem o namespace no moniker GetObject, conforme mostrado no exemplo de código a seguir:

`Set colServices = GetObject("winmgmts:").ExecQuery ("SELECT * FROM Win32_Service")`

Se raiz \\ cimv2 não for o namespace padrão no computador de destino, esse script falhará. Para evitar que isso aconteça, a raiz do namespace \\ cimv2 deve ser incluída no moniker, conforme mostrado no exemplo de código a seguir:

`Set colServices = GetObject("winmgmts:root\cimv2").ExecQuery("SELECT * FROM Win32_Service")`

Se o namespace padrão no computador de destino for diferente do namespace assumido por um script, o script falhará. Além disso, o usuário receberá a mensagem de erro um pouco enganosa "classe inválida". Na verdade, a falha não é porque a classe é inválida, mas porque a classe não pode ser encontrada no namespace padrão. Esse é um problema difícil de solucionar problemas, pois é provável que você investigue possíveis problemas com a classe em vez de problemas com o namespace que foi (ou, neste caso, não foi) especificado.

Você pode usar a **classe \_ WMISetting do Win32** para determinar como o WMI foi configurado em um computador. Os detalhes de configuração, como o namespace padrão ou o número de Build do WMI, podem ser úteis para solucionar problemas de script. Essas configurações também fornecem informações administrativas importantes, como, ou até mesmo, se os erros do WMI são registrados em um computador e quais provedores de WMI serão automaticamente recarregados se você precisar recriar o repositório WMI.

## <a name="examples"></a>Exemplos

O exemplo de código do VBScript [Modificar configurações do WMI](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) na galeria do TechNet usa a classe **Win32 \_ WMISetting** para configurar o intervalo de backup e o nível de log do WMI.

A [lista do exemplo de código VBScript do namespace padrão](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) na galeria do TechNet usa a classe **Win32 \_ WMISetting** para recuperar e exibir a configuração atual do WMI "namespace padrão para script".

O exemplo de código de [Modificar o namespace padrão do WMI](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) do VBScript na galeria do TechNet usa a propriedade **ASPScriptDefaultNamespace** para definir a configuração "namespace padrão para script" do WMI como "raiz \\ cimv2".

A [lista todas as configurações do WMI](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) exemplo de código VBSCript usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações do WMI configuradas em um computador.

O exemplo de código JavaScript [listar informações de configuração do WMI](https://Gallery.TechNet.Microsoft.Com/0427cfde-4cd9-4a3d-9140-3bb622a1df5d) usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações do WMI configuradas em um computador.

A [lista de informações de configuração do WMI](https://Gallery.TechNet.Microsoft.Com/370e7fbe-ea3c-4290-8a56-1e38519f518d) exemplo de código Python usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações de WMI configuradas em um computador.

O exemplo de código do objeto de [informações de configuração do WMI de lista](https://Gallery.TechNet.Microsoft.Com/9309e4c5-2ca6-4662-9451-f1342d5171d2) REXX usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações de WMI configuradas em um computador.

O exemplo de código VBScript a seguir mostra como obter a versão do WMI em execução no computador local. O "Win32 \_ WMISetting = @" indica a única instância da classe. Para obter mais informações, consulte versões do WMI.


```VB
set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!/Root/CIMv2")

set objWMISetting = objWMIService.Get("Win32_WMISetting=@")

WScript.Echo  objWMISetting.BuildVersion
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemcore.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dt>

[Classes de gerenciamento de serviço WMI](./wmi-service-management-classes.md)
</dt> </dl>

 

 
