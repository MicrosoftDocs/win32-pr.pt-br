---
title: Classe Win32_TSSessionSetting
description: Define as definições de configuração para a classe de terminal do Win32, \_ tais como limites de tempo e ações de desconexão e reconexão.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSSessionSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSSessionSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5139b53917f3d54b95fd153ac39fab176f047ba4bb9ec6df5d1c7c9b6e2d2f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769146"
---
# <a name="win32_tssessionsetting-class"></a>\_Classe Win32 TSSessionSetting

A classe WMI **\_ TSSessionSetting do Win32** define definições de configuração para a classe de [**\_ terminal do Win32**](win32-terminal.md) , tais como limites de tempo e ações de desconexão e reconexão.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSSessionSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSSessionSetting** tem esses métodos.



| Método                                                              | Descrição                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**BrokenConnection**](win32-tssessionsetting-brokenconnection.md) | Define as propriedades de conexão desfeitas incluídas nesta classe.<br/> |
| [**Limite de**](win32-tssessionsetting-timelimit.md)               | Define as propriedades de limite de tempo incluídas nesta classe.<br/>        |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSSessionSetting** tem essas propriedades.

<dl> <dt>

**ActiveSessionLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade máxima de tempo, em milissegundos, alocada a uma sessão ativa. Um valor de 0 especifica uma quantidade infinita de tempo.

</dd> <dt>

**BrokenConnectionAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ação que o servidor executa na sessão quando uma conexão é interrompida devido a perda de rede ou limites de tempo excedidos.

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Desconectar** (0)


</dt> <dd>

O usuário está desconectado da sessão.

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (1)


</dt> <dd>

A sessão é excluída permanentemente do servidor.

</dd> </dl>

</dd> <dt>

**BrokenConnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

A política que o servidor usa para determinar quando interromper uma conexão devido à perda de rede ou a limites de tempo excedidos.

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Servidor-substituir** (1)


</dt> <dd>

As configurações da política de desconexão do usuário são substituídas pelo servidor.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por usuário** (0)


</dt> <dd>

As configurações da política de desconexão do usuário estão em vigor.

</dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição (cadeia de caracteres de uma linha) do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo, em milissegundos, após o qual uma sessão desconectada é encerrada. Um valor de 0 especifica uma quantidade infinita de tempo.

</dd> <dt>

**EnableTimeoutWarning**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Habilita o aviso de tempo limite.

**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Esta propriedade não está disponível.

</dd> <dt>

**IdleSessionLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo, em milissegundos, após o qual uma sessão ociosa é encerrada. Um valor de 0 especifica uma quantidade infinita de tempo.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 ")
</dt> </dl>

A data em que o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PolicySourceActiveSessionLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **ActiveSessionLimit** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de grupo

</dd> <dt>

2
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceBrokenConnectionAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **BrokenConnectionAction** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de grupo

</dd> <dt>

2
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceDisconnectedSessionLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade DisconnectedSessionLimit** está configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de grupo

</dd> <dt>

2
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceIdleSessionLimit**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade IdleSessionLimit** está configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de grupo

</dd> <dt>

2
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**PolicySourceReconnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade ReconnectPolicy** está configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de grupo

</dd> <dt>

2
</dt> <dd>

Padrão

</dd> </dl>

</dd> <dt>

**ReconnectionPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Especifica se um usuário deve usar o cliente anterior para se reconectar a uma sessão desconectada.

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Qualquer cliente** (0)


</dt> <dd>

Qualquer cliente será usado para se reconectar.

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Cliente anterior** (1)


</dt> <dd>

O cliente anterior usado em uma conexão será usado para se reconectar.

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Status atual do objeto. Vários status operacionais e não operacionais podem ser definidos. Os status operacionais incluem: "OK", "Degradado" e "Pred Fail" (um elemento, como uma unidade de disco rígido habilitada para SMART, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status nãooperacionais incluem: "Error", "Starting", "Stopping" e "Service". O último, "Serviço", pode ser aplicado durante o espelhamento de um disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Erro")


</dt> <dd></dd> <dt>



 ("Degradado")


</dt> <dd></dd> <dt>



 ("Desconhecido")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Iniciando")


</dt> <dd></dd> <dt>



 ("Parando")


</dt> <dd></dd> <dt>



 ("Serviço")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do terminal.

Essa propriedade é herdada de [**\_ TerminalSetting do Win32.**](win32-terminalsetting.md)

</dd> <dt>

**TimeLimitPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

A política que o servidor usa para determinar os limites de tempo para sessões de usuário.

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Por Usuário** (0)


</dt> <dd>

As configurações de política de limites de tempo do usuário estão em vigor.

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Substituição do servidor** (1)


</dt> <dd>

As configurações de política de limites de tempo do usuário são substituídos pelo servidor.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

Esteja ciente de que as winstations associadas à sessão de console não podem acessar os métodos e as propriedades dessa classe. Se for feita uma tentativa de fazer isso especificando "Console" como o valor da propriedade TerminalName, os métodos desse objeto retornarão **WBEM \_ E \_ NOT \_ SUPPORTED**. Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto com a finalidade de adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.

Para se conectar ao namespace "Raiz \\ CIMV2 \\ TerminalServices", o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse seria um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Para Visual Basic e chamadas de script, esse seria um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**Configuração cim \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

