---
description: Um objeto SWbemPrivilegeSet é uma coleção de objetos SWbemPrivilege em um objeto SWbemSecurity que solicita privilégios específicos para um objeto Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Objeto SWbemPrivilegeSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296593"
---
# <a name="swbemprivilegeset-object"></a>Objeto SWbemPrivilegeSet

Um objeto **SWbemPrivilegeSet** é uma coleção de objetos [**SWbemPrivilege**](swbemprivilege.md) em um objeto [**SWbemSecurity**](swbemsecurity.md) que solicita privilégios específicos para um objeto Instrumentação de gerenciamento do Windows (WMI). Consulte a lista de privilégios em [**constantes de privilégio**](privilege-constants.md). Os itens são adicionados à coleção usando os métodos [**Add**](swbemprivilegeset-add.md) e [**AddAsString**](swbemprivilegeset-addasstring.md) . Os itens são recuperados da coleção usando o método [**Item**](swbemprivilegeset-item.md) e removidos usando o método [**Remove**](swbemprivilegeset-remove.md) . Este objeto não pode ser criado pela chamada do método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) do VBScript. Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).

Um objeto **SWbemPrivilegeSet** é um conjunto de solicitações de substituição de privilégio para um objeto específico. Quando uma chamada à API é feita usando esse objeto, as solicitações de substituição de privilégio são tentadas. O objeto **SWbemPrivilegeSet** não define os privilégios disponíveis para o usuário ou processo atual. Em outras palavras, a obtenção de privilégios para qualquer objeto WMI não identifica as configurações de privilégio feitas na conexão com o WMI ou os privilégios em vigor quando um objeto é entregue a um coletor.

## <a name="members"></a>Membros

O objeto **SWbemPrivilegeSet** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemPrivilegeSet** tem esses métodos.



| Método                                               | Descrição                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Agrega**](swbemprivilegeset-add.md)                 | Adiciona um objeto [**SWbemPrivilege**](swbemprivilege.md) à coleção **SWbemPrivilegeSet** usando uma constante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .<br/> |
| [**AddAsString**](swbemprivilegeset-addasstring.md) | Adiciona um objeto [**SWbemPrivilege**](swbemprivilege.md) à coleção **SWbemPrivilegeSet** usando uma cadeia de caracteres de privilégio.<br/>                                    |
| [**DeleteAll**](swbemprivilegeset-deleteall.md)     | Exclui todos os privilégios da coleção.<br/>                                                                                                              |
| [**Item**](swbemprivilegeset-item.md)               | Recupera um objeto [**SWbemPrivilege**](swbemprivilege.md) da coleção. Esse é o método padrão deste objeto.<br/>                                 |
| [**Remover**](swbemprivilegeset-remove.md)           | Remove um objeto [**SWbemPrivilege**](swbemprivilege.md) da coleção.<br/>                                                                              |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemPrivilegeSet** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Contar**](swbemprivilegeset-count.md)<br/> | Somente leitura<br/> | Número de itens na coleção.<br/> |



 

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir obtém um objeto SWbemPrivileges e adiciona todos os privilégios disponíveis à coleção por valor de privilégio, conforme definido em [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



O exemplo de código VBScript a seguir demonstra como adicionar privilégios usando o objeto **SWbemPrivilegeSet** .


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



O exemplo de código do Perl a seguir demonstra como adicionar privilégios usando o objeto **SWbemPrivilegeSet** .


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGESET CLSID<br/>                                                     |
| IID<br/>                      | ISWbemPrivilegeSet de IID \_<br/>                                                      |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Executando operações privilegiadas](executing-privileged-operations.md)
</dt> <dt>

[Executando operações privilegiadas usando o VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> <dt>

[**Constantes de privilégio**](privilege-constants.md)
</dt> </dl>

 

