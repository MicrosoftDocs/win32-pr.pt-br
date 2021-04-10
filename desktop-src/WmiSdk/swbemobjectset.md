---
description: Um objeto SWbemObjectSet é uma coleção de objetos SWbemObject. Para obter mais informações, consulte Acessando uma coleção. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objeto SWbemObjectSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171782"
---
# <a name="swbemobjectset-object"></a>Objeto SWbemObjectSet

Um objeto **SWbemObjectSet** é uma coleção de objetos [**SWbemObject**](swbemobject.md) . Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md). Este objeto não pode ser criado pela chamada VBScript **CreateObject** .

Você pode obter um objeto **SWbemObjectSet** chamando qualquer um dos seguintes métodos ou seus equivalentes assíncronos:

-   [**SWbemObject. ASSOCIATORS\_**](swbemobject-associators-.md)
-   [**SWbemObject. instâncias\_**](swbemobject-instances-.md)
-   [**SWbemObject. referências\_**](swbemobject-references-.md)
-   [**Subclasses de SWbemObject\_**](swbemobject-subclasses-.md)
-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices. References**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)

> [!Note]  
> O objeto **SWbemObjectSet** não dá suporte aos métodos opcionais **Add** e **Remove** Collection.

 

> [!Note]  
> Como o retorno de chamada para o coletor não pode ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

## <a name="members"></a>Membros

O objeto **SWbemObjectSet** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemObjectSet** tem esses métodos.



| Método                              | Descrição                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [**Item**](swbemobjectset-item.md) | Recupera um objeto [**SWbemObject**](swbemobject.md) da coleção. Esse é o método padrão do objeto.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemObjectSet** tem essas propriedades.



| Propriedade                                                  | Tipo de acesso          | Descrição                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Contar**](swbemobjectset-count.md)<br/>          | Somente leitura<br/> | Número de itens na coleção.<br/>        |
| [**Segurança\_**](swbemobjectset-security-.md)<br/> | Somente leitura<br/> | Usado para ler ou alterar as configurações de segurança.<br/> |



 

## <a name="remarks"></a>Comentários

Um **SWbemObjectSet** é uma coleção de zero ou mais objetos [**SWbemObject**](swbemobject.md) . Cada **SWbemObject** em um **SWbemObjectSet** pode representar uma das duas coisas:

-   Uma instância de um recurso gerenciado por WMI.
-   Uma instância de uma definição de classe.

O uso mais comum dessa classe no WMI é como o valor de retorno para uma chamada [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) ou [**InstancesOf**](swbemservices-instancesof.md) , conforme descrito no exemplo de código a seguir:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



Na maior parte, a única coisa que você fará com um **SWbemObjectSet** é enumerar todos os objetos contidos na coleção em si. No entanto, o **SWbemObjectSet** inclui uma contagem de propriedades que pode ser útil no script de administração do sistema. Como o nome implica, Count informa o número de itens na coleção. Por exemplo, esse script recupera uma coleção de todos os serviços instalados em um computador e, em seguida, ecoa o número total de serviços encontrados:

Para obter mais informações sobre como usar essa classe, consulte [enumerando o WMI](enumerating-wmi.md).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir ilustra como as coleções **SWbemObjectSet** são manipuladas.


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



O exemplo de código Perl a seguir ilustra como as coleções de **SWbemObjectSet** são manipuladas.


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
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
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | ISWbemObjectSet de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




