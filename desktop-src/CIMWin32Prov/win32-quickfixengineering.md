---
description: O Win32 \_ QuickFixEngineering&\# 8194; A classe WMI representa uma pequena atualização em todo o sistema, normalmente conhecida como atualização de QFE (Quick-Fix Engineering), aplicada ao sistema operacional atual.
ms.assetid: 84aed428-7620-4f7a-941f-f9d683020d8a
ms.tgt_platform: multiple
title: Classe Win32_QuickFixEngineering
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_QuickFixEngineering
- Win32_QuickFixEngineering.Caption
- Win32_QuickFixEngineering.Description
- Win32_QuickFixEngineering.InstallDate
- Win32_QuickFixEngineering.Name
- Win32_QuickFixEngineering.Status
- Win32_QuickFixEngineering.CSName
- Win32_QuickFixEngineering.FixComments
- Win32_QuickFixEngineering.HotFixID
- Win32_QuickFixEngineering.InstalledBy
- Win32_QuickFixEngineering.InstalledOn
- Win32_QuickFixEngineering.ServicePackInEffect
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15110b5801555947eed434b8148aec3cc753f6eec359f32b96cd67a5b2649f31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675008"
---
# <a name="win32_quickfixengineering-class"></a>\_Classe Win32 QuickFixEngineering

A  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ QuickFixEngineering do Win32** representa uma pequena atualização de todo o sistema, normalmente conhecida como atualização de QFE (rápida correção de engenharia), aplicada ao sistema operacional atual. Essa classe retorna apenas as atualizações fornecidas pela CBS (serviço baseado em componente). Essas atualizações não estão listadas no registro. as atualizações fornecidas pelo Microsoft Windows Installer (MSI) ou pelo site de atualização do Windows ( [https://update.microsoft.com](https://update.microsoft.com/) ) não são retornadas pelo **Win32 \_ QuickFixEngineering**.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A1}"), AMENDMENT]
class Win32_QuickFixEngineering : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CSName;
  string   FixComments;
  string   HotFixID;
  string   InstalledBy;
  string   InstalledOn;
  string   ServicePackInEffect;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ QuickFixEngineering** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ QuickFixEngineering** tem essas propriedades.

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

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**propagado**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem do CIM**](cim-computersystem.md).**Name**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" WMI ")
</dt> </dl>

Nome local do sistema de computador. O valor dessa propriedade é proveniente da classe [**de \_ sistema CIM**](cim-computersystem.md) .

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

**FixComments**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| SOFTWARE Win32Registry \\ \\ Microsoft \\ \\ Windows NT \\ \\ \\ \\ Hotfix CurrentVersion")
</dt> </dl>

Comentários adicionais relacionados à atualização.

</dd> <dt>

**HotFixID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Identificador exclusivo associado a uma atualização específica.

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

**InstalledBy**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| SOFTWARE Win32Registry \\ \\ Microsoft \\ \\ Windows NT \\ \\ \\ \\ Hotfix CurrentVersion")
</dt> </dl>

Pessoa que instalou a atualização. Se esse valor for desconhecido, a propriedade estará vazia.

</dd> <dt>

**Dever**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| SOFTWARE Win32Registry \\ \\ Microsoft \\ \\ Windows NT \\ \\ \\ \\ Hotfix CurrentVersion")
</dt> </dl>

Data em que a atualização foi instalada. Se esse valor for desconhecido, a propriedade estará vazia.

> [!Note]  
> Essa propriedade pode usar formatos diferentes, dependendo de quando o QuickFix foi instalado. A maioria dos sistemas usa um formato de data padrão, como "23-10-2013". No entanto, alguns sistemas podem retornar um valor hexadecimal de 64 bits no formato [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) do Win32.

 

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ServicePackInEffect**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Hotfix")
</dt> </dl>

Service Pack em vigor quando a atualização foi aplicada. Se nenhum service pack tiver sido aplicado, a propriedade terá o valor SP0. Se não for possível determinar qual service pack estava em vigor, essa propriedade será **nula**.

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

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("Sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de vírgula** ("comm perdida")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ QuickFixEngineering do Win32** é derivada de [**CIM \_ LogicalElement.**](cim-logicalelement.md)

Como as atualizações são armazenadas em dois locais, uma enumeração dessa classe pode resultar em duplicatas.

Uma correção quente é um patch temporário do sistema operacional produzido pelo grupo Correção Rápida Engenharia da Microsoft. Assim como os service packs, as correções ativas representam alterações feitas em uma versão do Windows após o lançamento do sistema operacional.

Ao contrário dos service packs, as correções ativas não se destinam à instalação sem problemas em todos os computadores. Em vez disso, eles são desenvolvidos para resolver problemas muito específicos, geralmente para configurações específicas do computador.

Além disso, as correções ativas representam instalações independentes que não dependem de outras correções ativas liberadas. Por exemplo, uma correção quente hipotética 4 não incluiria as correções de bug e a funcionalidade incluídas nas correções a quente 1, 2 e 3. Na maioria dos casos, também não seria necessário instalar as correções a quente 1, 2 e 3 antes de instalar a correção 4. Isso torna a enumeração de correções ativas individuais uma tarefa administrativa importante: para saber a configuração exata de um computador, você precisa saber não apenas quais service packs foram instalados, mas também quais hot fixes individuais foram instalados.

A **classe \_ QuickFixEngineering do Win32** permite enumerar todas as correções ativas que foram instaladas em um computador

## <a name="examples"></a>Exemplos

O exemplo do PowerShell [Obter Programas](https://Gallery.TechNet.Microsoft.Com/Get-Installed-Programs-fae091ed) Instalados retorna uma lista completa de programas instalados.

O exemplo de VBScript a seguir enumera as correções a quente instaladas em um computador


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colQuickFixes = objWMIService.ExecQuery("SELECT * FROM Win32_QuickFixEngineering")
For Each objQuickFix in colQuickFixes
 Wscript.Echo "Computer: " & objQuickFix.CSName
 Wscript.Echo "Description: " & objQuickFix.Description
 Wscript.Echo "Hot Fix ID: " & objQuickFix.HotFixID
 Wscript.Echo "Installation Date: " & objQuickFix.InstallDate
 Wscript.Echo "Installed By: " & objQuickFix.InstalledBy
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[Tarefas WMI: sistemas operacionais](../wmisdk/wmi-tasks--operating-systems.md)
</dt> </dl>

 

 
