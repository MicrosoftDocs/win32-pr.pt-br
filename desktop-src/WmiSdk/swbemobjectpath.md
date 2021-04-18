---
description: Use os métodos e as propriedades do objeto SWbemObjectPath para construir e validar um caminho de objeto. Esse objeto pode ser criado pela chamada do VBScript CreateObject.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objeto SWbemObjectPath (Wbemdisp. h)
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
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784536"
---
# <a name="swbemobjectpath-object"></a>Objeto SWbemObjectPath

Use os métodos e as propriedades do objeto **SWbemObjectPath** para construir e validar um caminho de objeto. Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .

## <a name="members"></a>Membros

O objeto **SWbemObjectPath** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemObjectPath** tem esses métodos.



| Método                                                   | Descrição                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [**SetAsClass**](swbemobjectpath-setasclass.md)         | Força o caminho para tratar de uma classe WMI.<br/>              |
| [**SetAsSingleton**](swbemobjectpath-setassingleton.md) | Força o caminho para endereçar uma instância WMI singleton.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemObjectPath** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso           | Descrição                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Authority**](swbemobjectpath-authority.md)<br/>             | Leitura/gravação<br/> | Cadeia de caracteres que define o componente de autoridade do caminho do objeto.<br/>                                                                                                           |
| [**Classe**](swbemobjectpath-class.md)<br/>                     | Leitura/gravação<br/> | Nome da classe que faz parte do caminho do objeto.<br/>                                                                                                                        |
| [**DisplayName**](swbemobjectpath-displayname.md)<br/>         | Leitura/gravação<br/> | Cadeia de caracteres que contém o caminho em um formulário que pode ser usado como um nome de exibição de moniker. Consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).<br/> |
| [**IsClass**](swbemobjectpath-isclass.md)<br/>                 | Somente leitura<br/>  | Valor booliano que indica se esse caminho representa uma classe. Isso é análogo à propriedade [ \_ \_ genus](wmi-system-properties.md) na API com.<br/>                    |
| [**IsSingleton**](swbemobjectpath-issingleton.md)<br/>         | Somente leitura<br/>  | Valor booliano que indica se esse caminho representa uma instância singleton.<br/>                                                                                                |
| [**simétricas**](swbemobjectpath-keys.md)<br/>                       | Somente leitura<br/>  | Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que contém as associações de valor de chave.<br/>                                                                          |
| [**Localidade**](swbemobjectpath-locale.md)<br/>                   | Leitura/gravação<br/> | Cadeia de caracteres que contém a localidade deste caminho de objeto.<br/>                                                                                                                     |
| [**Namespace**](swbemobjectpath-namespace.md)<br/>             | Leitura/gravação<br/> | Nome do namespace que faz parte do caminho do objeto. Isso é o mesmo que a propriedade [ \_ \_ namespace](wmi-system-properties.md) na API com.<br/>                        |
| [**ParentNamespace**](swbemobjectpath-parentnamespace.md)<br/> | Somente leitura<br/>  | Nome do pai do namespace que faz parte do caminho do objeto.<br/>                                                                                                      |
| [**Caminho**](swbemobjectpath-path.md)<br/>                       | Leitura/gravação<br/> | Contém o caminho absoluto. Isso é o mesmo que a propriedade do sistema [ \_ \_ Path](wmi-system-properties.md) na API com. Essa é a propriedade padrão deste objeto.<br/>    |
| [**Relpath**](swbemobjectpath-relpath.md)<br/>                 | Leitura/gravação<br/> | Contém o caminho relativo. Isso é o mesmo que a propriedade do sistema [ \_ \_ RelPath](wmi-system-properties.md) na API com.<br/>                                              |
| [**Segurança\_**](swbemobjectpath-security-.md)<br/>            | Somente leitura<br/>  | Usado para ler ou alterar as configurações de segurança.<br/>                                                                                                                             |
| [**Servidor**](swbemobjectpath-server.md)<br/>                   | Leitura/gravação<br/> | O nome do servidor. Isso é o mesmo que a propriedade do sistema de [ \_ \_ servidor](wmi-system-properties.md) na API com.<br/>                                                       |



 

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
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                       |
| IID<br/>                      | ISWbemObjectPath de IID \_<br/>                                                        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




