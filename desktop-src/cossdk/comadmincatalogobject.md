---
description: Representa itens em coleções no catálogo COM+. Use-o para recuperar e modificar as propriedades expostas por um item em uma coleção.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: Classe COMAdminCatalogObject (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: bce57021774b3abc2f69a1120862912452629c3e70d9c8fd0ebcc5d39ce5203d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548583"
---
# <a name="comadmincatalogobject-class"></a>Classe COMAdminCatalogObject

Representa itens em coleções no catálogo COM+. Use-o para recuperar e modificar as propriedades expostas por um item em uma coleção.

## <a name="when-to-implement"></a>Quando implementar

Essa classe é implementada pelo COM+.



| Requisito | Valor |
|------------|------------------------------------------|
| Interfaces | [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a>Quando usar

Use objetos criados a partir da classe **COMAdminCatalogObject** para modificar as propriedades de itens contidos em coleções no catálogo com+. Esses itens correspondem aos itens mostrados dentro das pastas na árvore de console da ferramenta de administração de serviços de componentes. As pastas na ferramenta de administração de serviços de componentes correspondem às coleções no catálogo, que você pode representar usando objetos criados na classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Nem todas as coleções e os itens expostos por meio de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e **COMAdminCatalogObject** estão disponíveis na ferramenta de administração de serviços de componentes.

Para obter informações sobre coleções específicas e suas propriedades, consulte [coleções de administração do com+](com--administration-collections.md).

Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).

## <a name="remarks"></a>Comentários

Você não pode criar diretamente um objeto **COMAdminCatalogObject** . Para usar os métodos deste objeto, você deve criar um objeto [**COMAdminCatalog**](comadmincatalog.md) , obter uma referência a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e, em seguida, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obter uma referência a uma interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa uma coleção de nível superior ou usar [**ICatalogCollection:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) para acessar coleções que não são de nível superior.

Depois de ter uma referência à interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) da coleção na qual você está interessado, chame [**ICatalogCollection::P opular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) para popular a coleção com todos os seus itens. Itere em cada um dos itens na coleção chamando [**ICatalogCollection:: get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) para obter uma referência a cada interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) . Quando você encontrar o item de interesse, poderá modificar as propriedades do item e sair da iteração. Se você fizer alterações em qualquer item de uma coleção, deverá chamar [**ICatalogCollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para salvar as alterações no catálogo com+.

Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração de COM+ de nível superior; "ItemName" deve ser substituído pelo nome do item no qual você está interessado; "PropertyName" deve ser substituído pelo nome da propriedade que você está modificando no item; e varNewProp devem ser substituídos por uma variante que contém o novo valor para a propriedade.


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+. Um objeto COMAdminCatalogCollection pode ser criado chamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) em um objeto [**COMAdminCatalog**](comadmincatalog.md) ou [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

Chame o método [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para popular a coleção com todos os seus itens. Iterar em cada um dos itens na coleção. Quando você encontrar o item de interesse, poderá modificar as propriedades do item e sair da iteração. Se você fizer alterações em qualquer item de uma coleção, deverá chamar o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) do objeto **COMAdminCatalogCollection** para salvar as alterações no catálogo com+.

Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração de COM+ de nível superior; "ItemName" deve ser substituído pelo nome do item no qual você está interessado; "PropertyName" deve ser substituído pelo nome da propriedade que você está modificando no item; e NewPropValue devem ser substituídos pelo novo valor da propriedade.


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMAdminCatalog**](comadmincatalog.md)
</dt> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




