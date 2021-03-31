---
description: Representa um único item em um objeto SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Objeto SWbemRefreshableItem (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663793"
---
# <a name="swbemrefreshableitem-object"></a>Objeto SWbemRefreshableItem

O objeto **SWbemRefreshableItem** representa um único item em um objeto [**SWbemRefresher**](swbemrefresher.md) . Um objeto **SWbemRefreshableItem** é obtido por meio dos métodos [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) de [**SWbemRefresher**](swbemrefresher.md). Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .

## <a name="members"></a>Membros

O objeto **SWbemRefreshableItem** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemRefreshableItem** tem esses métodos.



| Método                                        | Descrição                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Remover**](swbemrefreshableitem-remove.md) | Remove o objeto **SWbemRefreshableItem** do objeto [**SWbemRefresher**](swbemrefresher.md) pai.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemRefreshableItem** tem essas propriedades.



| Propriedade                                                       | Tipo de acesso           | Descrição                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [**Index**](swbemrefreshableitem-index.md)<br/>         | Leitura/gravação<br/> | Índice do item em seu objeto [**SWbemRefresher**](swbemrefresher.md) pai.<br/>                                          |
| [**IsSet**](swbemrefreshableitem-isset.md)<br/>         | Leitura/gravação<br/> | Indica se o objeto **SWbemRefreshableItem** representa um único objeto ou um conjunto de objetos.<br/>                        |
| [**Objeto**](swbemrefreshableitem-object.md)<br/>       | Leitura/gravação<br/> | Representa um único objeto [**SWbemObject**](swbemobject.md) que é atualizado.<br/>                                          |
| [**ObjectSet**](swbemrefreshableitem-objectset.md)<br/> | Leitura/gravação<br/> | Representa o conjunto de objetos a ser atualizado.<br/>                                                                                |
| [**Atualizador**](swbemrefreshableitem-refresher.md)<br/> | Somente leitura<br/>  | Representa o objeto [**SWbemRefresher**](swbemrefresher.md) pai que contém o objeto **SWbemRefreshableItem** .<br/> |



 

## <a name="remarks"></a>Comentários

O método VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) não pode ser usado para criar objetos **SWbemRefreshableItem** diretamente.

## <a name="examples"></a>Exemplos

O script a seguir ilustra a criação de um objeto [**SWbemRefresher**](swbemrefresher.md) e a adição de objeto único e enumerador **SWbemRefreshableItem** a ele.


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHABLEITEM CLSID<br/>                                                  |
| IID<br/>                      | ISWbemRefreshableItem de IID \_<br/>                                                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




