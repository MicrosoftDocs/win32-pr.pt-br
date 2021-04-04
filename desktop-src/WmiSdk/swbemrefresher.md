---
description: O objeto SWbemRefresher é um objeto de contêiner que pode atualizar os dados para todos os objetos adicionados a ele. O conjunto de objetos adicionados, cada item representado por uma instância de SWbemRefreshableItem pode ser tratado como uma coleção e enumerado.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Objeto SWbemRefresher (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930169"
---
# <a name="swbemrefresher-object"></a>Objeto SWbemRefresher

O objeto **SWbemRefresher** é um objeto de contêiner que pode atualizar os dados para todos os objetos que são adicionados a ele. Instâncias únicas e enumeradores de instância podem ser adicionados ou removidos do contêiner. O conjunto de objetos adicionados, cada item representado por uma instância de [**SWbemRefreshableItem**](swbemrefreshableitem.md) , pode ser tratado como uma coleção e enumerado. As instâncias do WMI de qualquer classe podem ser adicionadas ao objeto **SWbemRefresher** . Mesmo que o provedor dos dados da instância não seja um provedor de alto desempenho, o objeto do atualizador ainda poderá atualizar os dados na chamada de [**atualização**](swbemrefresher-refresh.md) . Se os dados forem fornecidos por meio de um provedor de alto desempenho e a propriedade [**falha**](swbemrefresher-autoreconnect.md) for **true**, o objeto **SWbemRefresher** tentará restabelecer uma conexão interrompida com o provedor de dados. Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .

A operação de atualização pode ser executada chamando o método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou o método [**\_ SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .

## <a name="members"></a>Membros

O objeto **SWbemRefresher** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemRefresher** tem esses métodos.



| Método                                        | Descrição                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Agrega**](swbemrefresher-add.md)             | Adiciona um novo objeto atualizável à coleção no objeto do atualizador.<br/>                   |
| [**AddEnum**](swbemrefresher-addenum.md)     | Adiciona um novo enumerador ao objeto atualizador.<br/>                                             |
| [**DeleteAll**](swbemrefresher-deleteall.md) | Remove todos os itens da coleção no objeto do atualizador.<br/>                             |
| [**Item**](swbemrefresher-item.md)           | Retorna um item de atualizador especificado da coleção.<br/>                                    |
| [**Atualizar**](swbemrefresher-refresh.md)     | Atualiza todos os itens contidos no objeto do atualizador.<br/>                          |
| [**Remover**](swbemrefresher-remove.md)       | Remove o objeto de item do atualizador ou o conjunto de objetos com um índice especificado do atualizador.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemRefresher** tem essas propriedades.



| Propriedade                                                         | Tipo de acesso          | Descrição                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**Falha**](swbemrefresher-autoreconnect.md)<br/> | Somente leitura<br/> | Indica se o atualizador se reconectará automaticamente a um provedor remoto se a conexão for interrompida.<br/> |
| [**Contar**](swbemrefresher-count.md)<br/>                 | Somente leitura<br/> | Contém o número de itens no objeto atualizador.<br/>                                                      |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir ilustra a criação de um objeto **SWbemRefresher** , usando os métodos [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) para armazenar uma única instância e uma instância de enumeração, a atualização dos dados e o uso da propriedade item para obter os objetos [**SWbemRefreshableItem**](swbemrefreshableitem.md) .


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | ISWbemRefresher de IID \_<br/>                                                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemRefreshableItem**](swbemrefreshableitem.md)
</dt> <dt>

[**SWbemObjectEx**](swbemobjectex.md)
</dt> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




