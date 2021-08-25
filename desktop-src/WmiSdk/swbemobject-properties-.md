---
description: A \_ Propriedade Properties do objeto SWbemObject retorna um objeto SWbemPropertySet que é uma coleção das propriedades da classe ou instância atual. Esta propriedade é somente para leitura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Propriedade SWbemObject.Properties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 413e13b725fce117b9358a254a860c631fc5fbe3158bf7f6d277ebca22647168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857306"
---
# <a name="swbemobjectproperties_-property"></a>Propriedade SWbemObject. Properties \_

A **propriedade \_ Properties** do objeto [**SWbemObject**](swbemobject.md) retorna um objeto [**SWbemPropertySet**](swbempropertyset.md) que é uma coleção das propriedades da classe ou instância atual. Esta propriedade é somente para leitura.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a>Valor da propriedade

## <a name="examples"></a>Exemplos

O exemplo de código do PowerShell para [gerar scripts de classe WMI do PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) na galeria do TechNet usa a \_ Propriedade Properties para gerar um script para cada uma das classes WMI que listarão o nome da classe WMI e as propriedades.

O código a seguir, extraído da [lista todas as propriedades de um exemplo de](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) código VBScript da classe WMI na galeria do TechNet, lista as propriedades de uma classe WMI especificada.


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



 

 




