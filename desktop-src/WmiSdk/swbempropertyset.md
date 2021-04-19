---
description: Um objeto SWbemPropertySet é uma coleção de objetos SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Objeto SWbemPropertySet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793693"
---
# <a name="swbempropertyset-object"></a>Objeto SWbemPropertySet

Um objeto **SWbemPropertySet** é uma coleção de objetos [**SWbemProperty**](swbemproperty.md) . Você pode adicionar itens à coleção usando o método [**Add**](swbempropertyset-add.md) , recuperar itens da coleção usando o método [**Item**](swbempropertyset-item.md) e remover itens da coleção usando o método [**Remove**](swbempropertyset-remove.md) . Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md). Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .

Os objetos [**SWbemProperty**](swbemproperty.md) que compõem uma coleção **SWbemPropertySet** são usados para descrever as propriedades de uma única classe ou instância WMI.

## <a name="members"></a>Membros

O objeto **SWbemPropertySet** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SWbemPropertySet** tem esses métodos.



| Método                                    | Descrição                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Agrega**](swbempropertyset-add.md)       | Adiciona um objeto [**SWbemProperty**](swbemproperty.md) à coleção **SWbemPropertySet** .<br/>                        |
| [**Item**](swbempropertyset-item.md)     | Obtém um [**SWbemProperty**](swbemproperty.md) nomeado da coleção. Este é o método padrão para esse objeto.<br/> |
| [**Remover**](swbempropertyset-remove.md) | Exclui um objeto [**SWbemProperty**](swbemproperty.md) da coleção.<br/>                                        |



 

### <a name="properties"></a>Propriedades

O objeto **SWbemPropertySet** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [**Contar**](swbempropertyset-count.md)<br/> | Somente leitura<br/> | O número de itens na coleção **SWbemPropertySet** .<br/> |



 

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir demonstra como [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) pode retornar **wbemErrResetToDefault** se a propriedade for substituída.


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTYSET CLSID<br/>                                                      |
| IID<br/>                      | ISWbemPropertySet de IID \_<br/>                                                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de API de script](scripting-api-objects.md)
</dt> </dl>

 

 




