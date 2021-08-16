---
description: A classe \_ WMI singleton WMISetting do Win32 contém os parâmetros operacionais para o serviço WMI. Essa classe só pode ter uma instância, que sempre existe para cada Windows sistema e não pode ser excluída. Instâncias adicionais não podem ser criadas.
ms.assetid: d33cd4f3-969b-46ce-baff-466f1a464906
ms.tgt_platform: multiple
title: Win32_WMISetting classe
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
ms.openlocfilehash: 39c976a6a8b4c25fbc42561b7d0a8db52b9029f679ad72993f931efa596d2d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079570"
---
# <a name="win32_wmisetting-class"></a>Classe \_ WMISetting Win32

A **classe \_ WMI singleton WMISetting** [do](../wmisdk/retrieving-a-class.md) Win32 contém os parâmetros operacionais para o serviço WMI. Essa classe só pode ter uma instância, que sempre existe para cada Windows sistema e não pode ser excluída. Instâncias adicionais não podem ser criadas.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

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

A **classe \_ WMISetting Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ WMISetting Win32** tem essas propriedades.

<dl> <dt>

**ASPScriptDefaultNamespace**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ scripting Default \| Namespace")
</dt> </dl>

Namespace de script padrão. Essa propriedade contém o namespace usado por chamadas da API de Script para WMI se nenhum for especificado pelo chamador.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ \_Namespace** \\ **padrão de** script \\  \\ **WBEM** \\ **da \|** Microsoft MACHINE Software LOCAL    

Exemplo: raiz \\ cimv2

Para ver um script de exemplo que usa essa propriedade, consulte a seção Comentários.

</dd> <dt>

**ASPScriptEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ scripting Enable for \| ASP")
</dt> </dl>

Se **For True,** o script WMI poderá ser usado Active Server Pages (ASP). Essa propriedade é válida em sistemas que executam versões sem suporte do Windows somente. Para sistemas de Windows com suporte, o script WMI sempre é permitido no ASP.

</dd> <dt>

**AutorecoverMofs**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| AUTOrecover MOFs")
</dt> </dl>

Lista de nomes de arquivo MOF totalmente qualificados usados para inicializar ou recuperar o repositório WMI. A lista determina a ordem na qual os arquivos MOF são compilados.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ MOFs \_ de** recuperação automática do \\  \\ **MICROSOFT** \\ **WBEM** \\ **CIMOM \| do** MACHINE Software LOCAL    

</dd> <dt>

**AutoStartWin9X**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| AutostartWin9X")
</dt> </dl>

Sem suporte.

<dt>

<span id="Don_t_start"></span><span id="don_t_start"></span><span id="DON_T_START"></span>

**Não iniciar** (0)


</dt> <dd></dd> <dt>

<span id="Autostart"></span><span id="autostart"></span><span id="AUTOSTART"></span>

**Início Automático** (1)


</dt> <dd></dd> <dt>

<span id="Start_on_reboot"></span><span id="start_on_reboot"></span><span id="START_ON_REBOOT"></span>

**Iniciar na reinicialização** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**BackupInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Backup Interval \| Threshold"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("minutos")
</dt> </dl>

Sem suporte. Em vez disso, faça backup do repositório WMI manualmente.

</dd> <dt>

**BackupLastTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Time Functions \| GetTimeZoneInformation")
</dt> </dl>

Data e hora em que o último backup foi executado.

</dd> <dt>

**BuildVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \| Build")
</dt> </dl>

Informações de versão para o serviço WMI instalado no momento.

Período de tempo que se desdoce entre backups do banco de dados WMI.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Build \_** \\  \\  \\ **\| WBEM** do Microsoft MACHINE Software LOCAL

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Descrição textual curta do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**DatabaseDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Repository \| Directory")
</dt> </dl>

Caminho do diretório que contém o repositório WMI.

</dd> <dt>

**DatabaseMaxSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max DB \| Size"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
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

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**EnableAnonWin9xConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableAnonConnections")
</dt> </dl>

Sem suporte.

</dd> <dt>

**EnableEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableEvents")
</dt> </dl>

Se **True**, o subsistema de evento WMI deverá ser habilitado.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| EnableEvents**

</dd> <dt>

**EnableStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| EnableStartupHeapPreallocation")
</dt> </dl>

Se **True**, o WMI criará um heap pré-alocado com o tamanho do valor **LastStartupHeapPreallocation** quando o WMI for inicializado.

</dd> <dt>

**HighThresholdOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM High Threshold On Client \| Objects"), [**Units**](../wmisdk/standard-qualifiers.md) ("objects per second")
</dt> </dl>

Taxa máxima na qual os objetos criados pelo provedor podem ser entregues aos clientes. Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI mantém objetos em filas antes de entregar aos consumidores. Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponde ao provedor. Se a memória mantida por objetos não recolhidos atingir **LowThresholdOnObjects**, o WMI reduzirá a adição de novos objetos à fila. Se eventos não encontrados continuarem se acumulando e a espera máxima para entregar eventos em **MaxWaitOnClientObjects** for atingida enquanto a memória usada estiver no valor em **HighThresholdOnClientObjects**, o WMI não aceitará mais objetos de provedores e retornará **WBEM \_ E OUT OF \_ \_ \_ MEMORY** para os clientes.

</dd> <dt>

**HighThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM High Threshold On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Taxa máxima na qual os eventos devem ser entregues aos clientes. Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI enfilia eventos antes de entregar aos consumidores. Para obter mais eficiência, os consumidores devem coletar os eventos em um ritmo que corresponde ao provedor. Se a memória mantida por eventos não recolhidos atingir **LowThresholdOnObjects**, o WMI reduzirá a adição de novos eventos à fila. Se eventos não recolhidos continuarem se acumulando e a espera máxima para entregar eventos em **MaxWaitOnEvents** for atingida enquanto a memória usada estiver no valor em **HighThresholdOnEvents,** o WMI não aceitará mais eventos de provedores e retornará **WBEM \_ E OUT OF \_ \_ \_ MEMORY** para os clientes.

> [!Note]  
> A interrupção só é feita para consumidores de Eventos Permanentes, portanto, os consumidores temporários não devem esperar a interrupção quando os eventos são feitos backup na fila de eventos interna do WMI.

 

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Limite \_ alto** cimom do \\  \\ **MICROSOFT** \\ **WBEM** MACHINE Software LOCAL \\ **em objetos cliente \| (B)**    

</dd> <dt>

**InstallationDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM Installation \| Directory")
</dt> </dl>

Caminho do diretório em que o software WMI foi instalado. O local padrão é \\ System32 \\ Wbem.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Diretório \_ de instalação do** \\  \\  \\ **WBEM \|** da Microsoft MACHINE Software LOCAL

</dd> <dt>

**LastStartupHeapPreallocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| LastStartupHeapPreallocation"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho do heap pré-alocado criado pelo WMI durante a inicialização.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **WBEM \| CIMOM \| LastStartupHeapPreallocation**

</dd> <dt>

**LoggingDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Logging \| Directory")
</dt> </dl>

Caminho do diretório que contém o local dos arquivos de log do sistema WMI.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Diretório \_ de log CIMOM** do \\  \\ **MICROSOFT** \\ **WBEM \| SOFTWARE \| LOCAL** MACHINE

</dd> <dt>

**LoggingLevel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM \| Logging")
</dt> </dl>

Habilitando o log de eventos e o nível de detalhes do log usado.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Log \_ CIMOM** do \\  \\ **Microsoft** \\ **WBEM \| SOFTWARE \|** LOCAL MACHINE

<dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

**Off** (0)


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

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Low Threshold On Client \| Objects"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("objetos por segundo")
</dt> </dl>

Taxa na qual o WMI começa a diminuir a criação de novos objetos criados para clientes. Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI mantém objetos em filas antes de entregar aos consumidores. Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponde ao provedor. Se a taxa de solicitações de objetos atingir **LowThresholdOnClientObjects**, o WMI reduzirá gradualmente a criação de novos objetos para corresponder à taxa de uso do cliente. Essa lentidão começa quando a taxa na qual os objetos estão sendo criados excede o valor dessa propriedade. Consulte **HighThresholdOnClientObjects**.

Essa propriedade reflete o valor do Registro.

**CHAVE \_ Limite \_ alto** cimom do \\  \\ **MICROSOFT** \\ **WBEM** MACHINE Software LOCAL \\ **em objetos cliente \| (B)**    

</dd> <dt>

**LowThresholdOnEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Low Threshold On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("eventos por segundo")
</dt> </dl>

Taxa na qual o WMI começa a reduzir a entrega de novos eventos. Para acomodar diferenciais de velocidade entre provedores e clientes, o WMI enfilia eventos antes de entregar aos consumidores. Para obter mais eficiência, os consumidores devem coletar os objetos em um ritmo que corresponde ao provedor. Se a fila ficar fora de controle, o WMI diminuirá– a entrega de eventos gradualmente para se alinhar à taxa do cliente. Essa lentidão começa quando a taxa na qual os eventos são gerados excede o valor dessa propriedade. Consulte **HighThresholdOnEvents**.

> [!Note]  
> A interrupção só é feita para consumidores de eventos permanentes, portanto, os consumidores temporários não devem esperar a interrupção quando os eventos são feitos backup na fila de eventos interna do WMI.

 

Essa propriedade reflete o valor do Registro.

**HKEY \_ Limite \_ alto** \\  \\ **do MICROSOFT** \\ **WBEM** CIMOM do SOFTWARE LOCAL \\ **MACHINE em objetos \| cliente {B}**    

</dd> <dt>

**MaxLogFileSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM CIMOM Log Size \\ \\ \| Max"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho máximo dos arquivos de log produzidos pelo serviço WMI.

Essa propriedade reflete o valor na chave do Registro.

**HKEY \_ Tamanho \_ máximo do** arquivo de log CIMOM do \\  \\ **Microsoft** \\ **WBEM \| \| Software** LOCAL MACHINE

</dd> <dt>

**MaxWaitOnClientObjects**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft \\ \\ \\ \\ WBEM \\ \\ CIMOM Max Wait On \| Events"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")
</dt> </dl>

Quantidade de tempo que um objeto recém-criado aguarda para ser usado pelo cliente antes de ser descartado e um valor de erro é retornado. Essa propriedade interage com as propriedades **LowThresholdOnClientObjects** e **HighThresholdOnClientObjects** para reduzir — reduzir — a entrega de objetos aos consumidores quando o consumidor estiver recebendo os objetos muito lentamente.

</dd> <dt>

**MaxWaitOnEvents**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
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

o exemplo de código [Modify WMI Configurações](https://Gallery.TechNet.Microsoft.Com/aa80d174-3592-4fed-9c50-11f34e541445) VBScript na galeria do TechNet usa a classe **Win32 \_ WMISetting** para configurar o intervalo de backup do wmi e o nível de log.

A [lista do exemplo de código VBScript do namespace padrão](https://Gallery.TechNet.Microsoft.Com/3fc69acd-ead0-4dd1-9ea1-e15a7331cfa0) na galeria do TechNet usa a classe **Win32 \_ WMISetting** para recuperar e exibir a configuração atual do WMI "namespace padrão para script".

O exemplo de código de [Modificar o namespace padrão do WMI](https://Gallery.TechNet.Microsoft.Com/6dbb20e6-036d-43a2-ad6d-58325ada6a19) do VBScript na galeria do TechNet usa a propriedade **ASPScriptDefaultNamespace** para definir a configuração "namespace padrão para script" do WMI como "raiz \\ cimv2".

a [lista todos os](https://Gallery.TechNet.Microsoft.Com/29c04301-e9b2-46d1-8714-2dbb51014c92) exemplos de código wmi Configurações VBSCript usa várias propriedades no **Win32 \_ WMISetting** para retornar uma lista de configurações de WMI configuradas em um computador.

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

 

 
