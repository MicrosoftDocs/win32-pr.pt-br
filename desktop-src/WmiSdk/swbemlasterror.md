---
description: Os métodos e as propriedades do objeto SWbemLastError contêm e manipulam objetos de erro.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Objeto SWbemLastError (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763196"
---
# <a name="swbemlasterror-object"></a>Objeto SWbemLastError

Os métodos e as propriedades do objeto **SWbemLastError** contêm e manipulam objetos de erro. Os métodos e as propriedades desse objeto são exatamente iguais aos do objeto [**SWbemObject**](swbemobject.md) , mas são usados para conter informações de erro em vez de informações de classe WMI. Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .

Você pode criar um objeto de erro **SWbemLastError** para inspecionar as informações de erro estendidas que estão associadas a uma chamada de método anterior. Se as informações de erro não estiverem disponíveis, haverá falha na tentativa de criar um objeto de erro. Se a chamada for bem sucedido e um objeto de erro retornar, o status do objeto será redefinido. Outras tentativas de recuperar um objeto de erro falharão até que ocorra um novo erro. Se você fizer uma chamada assíncrona que falhe, um objeto **SWbemLastError** poderá ser retornado para você pelo evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) no parâmetro *objWbemErrorObject* .

## <a name="members"></a>Membros

O objeto **SWbemLastError** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemLastError** tem esses métodos.



| Método                                                   | Descrição                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **ASSOCIADORES\_**                                        | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **AssociatorsAsync\_**                                   | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| [**8i\_**](swbemlasterror-clone-.md)                 | Faz uma cópia do objeto atual.<br/>                                               |
| [**CompareTo\_**](swbemlasterror-compareto-.md)         | Testa dois objetos para igualdade.<br/>                                                   |
| **Excluir\_**                                             | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **DeleteAsync\_**                                        | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **ExecMethod\_**                                         | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **ExecMethodAsync\_**                                    | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| [**GetObjectText\_**](swbemlasterror-getobjecttext-.md) | Recupera a representação textual do objeto escrito com a sintaxe MOF.<br/>       |
| **Instâncias\_**                                          | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **InstancesAsync\_**                                     | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **Posicione\_**                                                | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **PutAsync\_**                                           | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **Referências\_**                                         | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **ReferencesAsync\_**                                    | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **SpawnDerivedClass\_**                                  | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **SpawnInstance\_**                                      | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **Subclasses\_**                                         | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |
| **SubclassesAsync\_**                                    | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemLastError** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso          | Descrição                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Derivação\_**<br/>                                   | Somente leitura<br/> | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/>                                                                  |
| **Métodos\_** <br/>                                     | Somente leitura<br/> | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/>                                                                  |
| [**Caminho\_**](swbemlasterror-path-.md)<br/>             | Somente leitura<br/> | Contém um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual.<br/>                    |
| [**Propriedades\_**](swbemlasterror-properties-.md)<br/> | Somente leitura<br/> | Representa a coleção de propriedades do objeto **SWbemLastError** . Essa propriedade é um objeto [**SWbemPropertySet**](swbempropertyset.md) .<br/> |
| **Qualificadores\_**<br/>                                   | Somente leitura<br/> | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/>                                                                  |
| **Segurança\_**<br/>                                     | Somente leitura<br/> | Não usado. O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.<br/>                                                                  |



 

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir demonstra como inspecionar informações de erro e objeto de erro.


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



O exemplo do Perl a seguir demonstra como inspecionar informações de erro e objeto de erro.


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
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
| CLSID<br/>                    | \_SWBEMLASTERROR CLSID<br/>                                                        |
| IID<br/>                      | ISWbemLastError de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




