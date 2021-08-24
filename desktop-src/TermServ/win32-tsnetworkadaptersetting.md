---
title: Win32_TSNetworkAdapterSetting classe
description: Define várias definições de configuração para a classe do Terminal Win32, incluindo propriedades relacionadas ao adaptador de rede e o \_ número máximo de conexões permitidas.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterSetting classe Serviços de Área de Trabalho Remota
- Win32_TSNetworkAdapterSetting classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bddc43fc651b8107d56b63876b251f7973c6a11ecbdbbd5ee22e6dfec4338f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348541"
---
# <a name="win32_tsnetworkadaptersetting-class"></a>Classe Win32 \_ TSNetworkAdapterSetting

A classe WMI **Win32 \_ TSNetworkAdapterSetting** define várias definições de configuração para a classe [**do \_ Terminal Win32,**](win32-terminal.md) incluindo propriedades relacionadas ao adaptador de rede e o número máximo de conexões permitidas.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TSNetworkAdapterSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ TSNetworkAdapterSetting** tem esses métodos.



| Método                                                                                     | Descrição                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**SelectAllNetworkAdapters**](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | Seleciona todos os adaptadores de rede.<br/>                                                                 |
| [**SelectNetworkAdapterIP**](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | Seleciona um adaptador de rede com base no endereço IP do adaptador.<br/>                                  |
| [**SetNetworkAdapterLanaID**](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | Especifica o número do Adaptador de Rede de Área Local NetBIOS (LANG) do adaptador de rede a ser definido.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TSNetworkAdapterSetting** tem essas propriedades.

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

**DeviceIDList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeia de caracteres de IDs de dispositivo disponíveis retornadas na ordem dos adaptadores de rede física retornados na matriz **de propriedades NetworkAdapterList.** O valor da ID do dispositivo é a **propriedade DeviceID** no [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

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

**MaximumConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

O número máximo de conexões permitidas. O valor **MAXINT** indica um número ilimitado de conexões.

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

**NetworkAdapterID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O GUID que representa a ID do adaptador de rede a ser definido. Um **GUID** que consiste em todos os zeros indica todos os adaptadores de rede.

</dd> <dt>

**NetworkAdapterLanaID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de Adaptador de Rede de Área Local (LANG) netBIOS do adaptador de rede usado para identificar o adaptador de rede atribuído ao terminal.

</dd> <dt>

**NetworkAdapterList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de cadeia de caracteres de adaptadores de rede física disponíveis e as IDs de dispositivo correspondentes. As IDs do dispositivo são a **propriedade DeviceID** no [**Win32 \_ NetworkAdapter.**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

</dd> <dt>

**NetworkAdapterName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição do adaptador de rede a ser definido. Esse valor está em [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration).

</dd> <dt>

**PolicySourceMaximumConnections**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade MaximumConnections** está configurada pelo servidor, pela política de grupo ou por padrão.

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

</dd> </dl>

## <a name="remarks"></a>Comentários

Esteja ciente de que as winstations associadas à sessão de console não podem acessar os métodos e as propriedades dessa classe. Se for feita uma tentativa de fazer isso especificando "Console" como o valor da propriedade TerminalName, os métodos desse objeto retornarão **WBEM \_ E \_ NOT \_ SUPPORTED**. Esse código de erro também será retornado se uma estação de janela tentar chamar métodos desse objeto para adicionar ou modificar as propriedades de segurança das contas LocalSystem, LocalService ou NetworkService.

Para se conectar ao namespace "Root \\ CIMV2 \\ TerminalServices", o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação de **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Para Visual Basic e scripts, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "pktPrivacy", com um valor de 6. O exemplo Visual Basic VBScript (Scripting Edition) a seguir mostra como se conectar a um computador remoto com privacidade de pacote.


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

[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

