---
description: A \_ propriedade de derivação do objeto SWbemObject contém uma matriz de cadeias de caracteres que descreve a hierarquia de derivação de classe para a instância que está sendo referenciada.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Derivation_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797648"
---
# <a name="swbemobjectderivation_-property"></a>Propriedade SWbemObject. Derivation \_

A propriedade de **derivação \_** do objeto [**SWbemObject**](swbemobject.md) contém uma matriz de cadeias de caracteres que descreve a hierarquia de derivação de classe para a instância que está sendo referenciada. O primeiro elemento na matriz define a classe pai e o último elemento define a classe dinastia. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir descreve como recuperar a hierarquia de classe para o disco lógico do Win32 \_ .


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



Ele seguinte exemplo de Perl descreve como recuperar a hierarquia de classe para o disco lógico do Win32 \_ .


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



 

 




