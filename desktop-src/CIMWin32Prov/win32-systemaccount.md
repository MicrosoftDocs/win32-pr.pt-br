---
description: O Win32 \_ SystemAccount&\# 8194; A classe WMI representa uma conta do sistema.
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Classe Win32_SystemAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754384"
---
# <a name="win32_systemaccount-class"></a>\_Classe Win32 SystemAccount

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemAccount do Win32** representa uma conta do sistema. A conta do sistema é usada pelo sistema operacional e serviços. Há muitos serviços e processos no Windows que precisam da capacidade de fazer logon internamente, por exemplo, durante uma instalação do Windows. A conta do sistema foi projetada para essa finalidade.

A conta do sistema é uma conta interna que não aparece no Gerenciador de usuários, não pode ser adicionada a nenhum grupo e não pode ter direitos de usuário atribuídos a ela. No entanto, a conta do sistema aparece em um volume do sistema de arquivos NTFS no Gerenciador de arquivos, localizado na seção permissões do menu segurança. Por padrão, a conta System recebe controle total para todos os arquivos em um volume do sistema de arquivos NTFS, o que significa que a conta System tem os mesmos privilégios funcionais que a conta de administrador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SystemAccount** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SystemAccount** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Domínio**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Domain"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management Functions \| nomedodomínio")
</dt> </dl>

Nome do domínio do Windows ao qual a conta do sistema pertence.

Exemplo: "NA-SALEs"

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fixos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Se for **true**, a conta será definida no computador local. Para recuperar apenas as contas definidas no computador local, crie uma consulta que inclua a condição "LocalAccount =**true**".

Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Network Management estruturas \| name")
</dt> </dl>

Nome da conta do sistema Windows no domínio especificado pela propriedade de **domínio** dessa classe.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**fixos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| identificadores de segurança do win32api (SIDs)")
</dt> </dl>

SID (identificador de segurança) desta conta. Um SID é um valor de cadeia de caracteres de comprimento variável usado para identificar um confiável. Cada conta tem um SID exclusivo emitido por uma autoridade (como um domínio do Windows), armazenado em um banco de dados de segurança. Quando um usuário faz logon, o sistema recupera o SID do usuário do banco de dados e o coloca no token de acesso do usuário. O sistema usa o SID no token de acesso do usuário para identificar o usuário em todas as interações subsequentes com a segurança do Windows. Quando um SID é usado como o identificador exclusivo para um usuário ou grupo, ele não pode ser usado novamente para identificar outro usuário ou grupo.

Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| tipos de enumeração de controle de acesso do \| \_ nome SID \_ use")
</dt> </dl>

Valores enumerados que especificam o tipo de SID (identificador de segurança).

Essa propriedade é herdada [**da \_ conta Win32**](win32-account.md).

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**SidTypeUser** (1)


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**SidTypeGroup** (2)


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**SidTypeDomain** (3)


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**SidTypeAlias** (4)


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**SidTypeWellKnownGroup** (5)


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6)


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**SidTypeInvalid** (7)


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8)


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**SidTypeComputer** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ SystemAccount** é derivada da [**\_ conta Win32**](win32-account.md).

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

[**\_Conta Win32**](win32-account.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
