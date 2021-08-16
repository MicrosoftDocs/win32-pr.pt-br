---
description: Use os métodos e as propriedades do objeto SWbemObjectPath para construir e validar um caminho de objeto. Esse objeto pode ser criado pela chamada CreateObject do VBScript.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objeto SWbemObjectPath (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2d7273b39c5cdccea7e46a077c925247846cd9ca255fc1dba20a95aeb159b773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118313545"
---
# <a name="swbemobjectpath-object"></a>Objeto SWbemObjectPath

Use os métodos e as propriedades do **objeto SWbemObjectPath** para construir e validar um caminho de objeto. Esse objeto pode ser criado pela chamada **CreateObject** do VBScript.

## <a name="members"></a>Membros

O **objeto SWbemObjectPath** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto SWbemObjectPath** tem esses métodos.



| Método                                                   | Descrição                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | Força o caminho a abordar uma classe WMI.<br/>              |
| [**SetAsSing ltd**](swbemobjectpath-setassingleton.md) | Força o caminho a abordar uma instância WMI singleton.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto SWbemObjectPath** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso           | Descrição                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autoridade**](swbemobjectpath-authority.md)<br/>             | Leitura/gravação<br/> | Cadeia de caracteres que define o componente Autoridade do caminho do objeto.<br/>                                                                                                           |
| [**Classe**](swbemobjectpath-class.md)<br/>                     | Leitura/gravação<br/> | Nome da classe que faz parte do caminho do objeto.<br/>                                                                                                                        |
| [**Displayname**](swbemobjectpath-displayname.md)<br/>         | Leitura/gravação<br/> | Cadeia de caracteres que contém o caminho em um formulário que pode ser usado como um nome de exibição de moniker. Consulte [Criando um aplicativo WMI ou script](creating-a-wmi-application-or-script.md).<br/> |
| [**Isclass**](swbemobjectpath-isclass.md)<br/>                 | Somente leitura<br/>  | Valor booliana que indica se esse caminho representa uma classe. Isso é análogo à [ \_ \_ propriedade Deia](wmi-system-properties.md) na API COM.<br/>                    |
| [**IsSing ltda**](swbemobjectpath-issingleton.md)<br/>         | Somente leitura<br/>  | Valor booliana que indica se esse caminho representa uma instância singleton.<br/>                                                                                                |
| [**Chaves**](swbemobjectpath-keys.md)<br/>                       | Somente leitura<br/>  | Um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que contém as vinculações de valor de chave.<br/>                                                                          |
| [**Local**](swbemobjectpath-locale.md)<br/>                   | Leitura/gravação<br/> | Cadeia de caracteres que contém a localidade desse caminho de objeto.<br/>                                                                                                                     |
| [**Namespace**](swbemobjectpath-namespace.md)<br/>             | Leitura/gravação<br/> | Nome do namespace que faz parte do caminho do objeto. Isso é o mesmo que a [ \_ \_ propriedade Namespace](wmi-system-properties.md) na API COM.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Somente leitura<br/>  | Nome do pai do namespace que faz parte do caminho do objeto.<br/>                                                                                                      |
| [**Caminho**](swbemobjectpath-path.md)<br/>                       | Leitura/gravação<br/> | Contém o caminho absoluto. Isso é o mesmo que a [ \_ \_ propriedade do](wmi-system-properties.md) sistema Path na API COM. Essa é a propriedade padrão desse objeto.<br/>    |
| [**Relpath**](swbemobjectpath-relpath.md)<br/>                 | Leitura/gravação<br/> | Contém o caminho relativo. Isso é o mesmo que a [ \_ \_ propriedade do sistema Relpath](wmi-system-properties.md) na API COM.<br/>                                              |
| [**Segurança\_**](swbemobjectpath-security-.md)<br/>            | Somente leitura<br/>  | Usado para ler ou alterar as configurações de segurança.<br/>                                                                                                                             |
| [**Servidor**](swbemobjectpath-server.md)<br/>                   | Leitura/gravação<br/> | O nome do servidor. Isso é o mesmo que a [ \_ \_ propriedade do sistema](wmi-system-properties.md) Server na API COM.<br/>                                                       |



 

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir demonstra como criar caminhos de objeto.


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



O exemplo de código Perl a seguir demonstra como criar caminhos de objeto.


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
  }
  else
  {
   print STDERR Win32::OLE->LastError, "\n";
  }
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




