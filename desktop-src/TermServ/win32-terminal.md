---
title: Win32_Terminal classe
description: Representa um terminal.
ms.assetid: d56cc605-6c5a-46ae-96fd-d0a4f5b6074a
ms.tgt_platform: multiple
keywords:
- Win32_Terminal classe Serviços de Área de Trabalho Remota
- Win32_Terminal classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_Terminal
- Win32_Terminal.Caption
- Win32_Terminal.Description
- Win32_Terminal.InstallDate
- Win32_Terminal.Name
- Win32_Terminal.Status
- Win32_Terminal.fEnableTerminal
- Win32_Terminal.LoggedOnUsers
- Win32_Terminal.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43f3998e1b8f9e7d252a8a4c949d7d083c763a8759d7c9df6aa60c21618e217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867956"
---
# <a name="win32_terminal-class"></a>Classe de Terminal Win32 \_

A **classe WMI \_ do Terminal Win32** representa um terminal.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, overwrite, provider("Win32_WIN32_TERMINAL_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_Terminal : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint32   fEnableTerminal;
  uint32   LoggedOnUsers;
  string   TerminalName;
};
```

## <a name="members"></a>Membros

A **classe \_ Terminal Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Terminal Win32** tem esses métodos.



| Método                                  | Descrição                                                                                                                                                                             |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Criar**](create-win32-terminal.md) | Cria um terminal com configurações padrão que podem ser personalizadas usando as propriedades e os métodos das classes [**Win32 \_ TerminalSetting.**](win32-terminalsetting.md)<br/> |
| [**Excluir**](delete-win32-terminal.md) | Exclui o terminal especificado.<br/>                                                                                                                                              |
| [**Habilitar**](win32-terminal-enable.md) | Desabilita ou habilita o terminal.<br/>                                                                                                                                            |
| [**Renomear**](win32-terminal-rename.md) | Renomeia o terminal.<br/>                                                                                                                                                        |



 

### <a name="properties"></a>Propriedades

A **classe \_ Terminal Win32** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Descrição curta (cadeia de caracteres de uma linha) do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**fEnableTerminal**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o terminal especificado está desabilitado ou habilitado.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE** (0)


</dt> <dd>

O terminal está desabilitado.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**TRUE** (1)


</dt> <dd>

O terminal está habilitado.

</dd> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

A data em que o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LoggedOnUsers**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de sessões de logon para o terminal.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O nome exclusivo que identifica a instância do terminal.

</dd> </dl>

## <a name="remarks"></a>Comentários

**Win32 \_ O** terminal é associado a [**Win32 \_ TerminalSetting**](win32-terminalsetting.md) como a propriedade **Element** da associação [**Win32 \_ TerminalTerminalSetting.**](win32-terminalterminalsetting.md)

As classes a seguir são subclasses da classe **\_ Terminal Win32:** [**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md), [**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md), [**Win32 \_ TSSessionSetting**](win32-tssessionsetting.md), [**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md), [**Win32 \_ TSRemoteControlSetting**](win32-tsremotecontrolsetting.md), [**Win32 \_ TSClientSetting**](win32-tsclientsetting.md), [**Win32 \_ TSNetworkAdapterSetting**](win32-tsnetworkadaptersetting.md), [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md), [**Win32 \_ TSPermissionsSetting**](win32-tspermissionssetting.md)e [**Win32 \_ TSAccount**](win32-tsaccount.md).

Observe que as winstations associadas à sessão de console não podem acessar os métodos e as propriedades dessa classe. Se for feita uma tentativa de fazer isso especificando "Console" como o valor da propriedade **TerminalName,** os métodos desse objeto retornarão **WBEM \_ E NOT \_ \_ SUPPORTED**. Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.

Para se conectar ao \\ \\ namespace raiz CIMV2 \\ TerminalServices, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Para Visual Basic e script de chamadas, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


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
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[**\_TerminalServiceSetting Win32**](win32-terminalservicesetting.md)
</dt> <dt>

[**\_TerminalTerminalSetting Win32**](win32-terminalterminalsetting.md)
</dt> </dl>

 

