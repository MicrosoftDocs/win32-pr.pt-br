---
title: Classe Win32_TSPermissionsSetting
description: Inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.
ms.assetid: ebc6e96a-668e-44aa-b589-c3e476fb3029
ms.tgt_platform: multiple
keywords:
- Classe de Win32_TSPermissionsSetting Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_TSPermissionsSetting classe, descrita
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting
- Win32_TSPermissionsSetting.Caption
- Win32_TSPermissionsSetting.Description
- Win32_TSPermissionsSetting.InstallDate
- Win32_TSPermissionsSetting.Name
- Win32_TSPermissionsSetting.Status
- Win32_TSPermissionsSetting.TerminalName
- Win32_TSPermissionsSetting.DenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.PolicySourceDenyAdminPermissionForCustomization
- Win32_TSPermissionsSetting.StringSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877b8373667bf01010ceb63c0ec35e46db48f702
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764731"
---
# <a name="win32_tspermissionssetting-class"></a>\_Classe Win32 TSPermissionsSetting

A classe WMI **\_ TSPermissionsSetting do Win32** inclui um método para adicionar novas contas ao terminal e um método para restaurar as permissões padrão para um terminal.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética. Para obter informações de referência sobre métodos, consulte a tabela de métodos mais adiante neste tópico.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TSPERMISSIONSSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSPermissionsSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   DenyAdminPermissionForCustomization;
  uint32   PolicySourceDenyAdminPermissionForCustomization;
  string   StringSecurityDescriptor;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ TSPermissionsSetting** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ TSPermissionsSetting** tem esses métodos.



| Método                                                                | Descrição                                                                                                                    |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Addconta**](win32-tspermissionssetting-addaccount.md)           | Adiciona uma conta ao terminal com o conjunto de permissões especificado no valor do parâmetro *PermissionPreSet* .<br/> |
| [**RestoreDefaults**](win32-tspermissionssetting-restoredefaults.md) | Restaura os valores padrão do conjunto de permissões para o terminal.<br/>                                                        |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ TSPermissionsSetting** tem essas propriedades.

<dl> <dt>

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

**DenyAdminPermissionForCustomization**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o administrador local tem permissão para personalizar.

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

**PolicySourceDenyAdminPermissionForCustomization**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **MinEncryptionLevel** é configurada pelo servidor, pela política de grupo ou por padrão.

<dt>

0
</dt> <dd>

Servidor

</dd> <dt>

1
</dt> <dd>

Política de grupo

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

**StringSecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Descritor de segurança associado ao terminal em formato de matriz de bytes binários.

</dd> <dt>

**Terminalname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do terminal.

Esta propriedade é herdada do [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Para se conectar ao \\ \\ \\ namespace TerminalServices de cimv2 raiz, o nível de autenticação deve incluir a privacidade do pacote. Para chamadas C/C++, esse é um nível de autenticação **da \_ \_ privacidade do \_ PCT no \_ nível \_ do autenticação RPC C**. Para chamadas de script e de Visual Basic, esse é um nível de autenticação de **WbemAuthenticationLevelPktPrivacy** ou "PktPrivacy", com um valor de 6. O exemplo a seguir Visual Basic Scripting Edition (VBScript) mostra como se conectar a um computador remoto com privacidade de pacote.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**\_TerminalSetting Win32**](win32-terminalsetting.md)
</dt> </dl>

 

