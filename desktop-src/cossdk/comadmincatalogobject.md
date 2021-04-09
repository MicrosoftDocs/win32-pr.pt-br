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
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089177"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="724d7-104">Classe COMAdminCatalogObject</span><span class="sxs-lookup"><span data-stu-id="724d7-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="724d7-105">Representa itens em coleções no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="724d7-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="724d7-106">Use-o para recuperar e modificar as propriedades expostas por um item em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="724d7-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="724d7-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="724d7-107">When to implement</span></span>

<span data-ttu-id="724d7-108">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="724d7-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="724d7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="724d7-109">Requirement</span></span> | <span data-ttu-id="724d7-110">Valor</span><span class="sxs-lookup"><span data-stu-id="724d7-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="724d7-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="724d7-111">Interfaces</span></span> | [<span data-ttu-id="724d7-112">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="724d7-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="724d7-113">Quando usar</span><span class="sxs-lookup"><span data-stu-id="724d7-113">When to use</span></span>

<span data-ttu-id="724d7-114">Use objetos criados a partir da classe **COMAdminCatalogObject** para modificar as propriedades de itens contidos em coleções no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="724d7-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="724d7-115">Esses itens correspondem aos itens mostrados dentro das pastas na árvore de console da ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="724d7-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="724d7-116">As pastas na ferramenta de administração de serviços de componentes correspondem às coleções no catálogo, que você pode representar usando objetos criados na classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="724d7-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="724d7-117">Nem todas as coleções e os itens expostos por meio de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) e **COMAdminCatalogObject** estão disponíveis na ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="724d7-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="724d7-118">Para obter informações sobre coleções específicas e suas propriedades, consulte [coleções de administração do com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="724d7-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="724d7-119">Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="724d7-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="724d7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="724d7-120">Remarks</span></span>

<span data-ttu-id="724d7-121">Você não pode criar diretamente um objeto **COMAdminCatalogObject** .</span><span class="sxs-lookup"><span data-stu-id="724d7-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="724d7-122">Para usar os métodos deste objeto, você deve criar um objeto [**COMAdminCatalog**](comadmincatalog.md) , obter uma referência a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e, em seguida, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obter uma referência a uma interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa uma coleção de nível superior ou usar [**ICatalogCollection:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) para acessar coleções que não são de nível superior.</span><span class="sxs-lookup"><span data-stu-id="724d7-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="724d7-123">Depois de ter uma referência à interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) da coleção na qual você está interessado, chame [**ICatalogCollection::P opular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) para popular a coleção com todos os seus itens.</span><span class="sxs-lookup"><span data-stu-id="724d7-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="724d7-124">Itere em cada um dos itens na coleção chamando [**ICatalogCollection:: get \_ Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) para obter uma referência a cada interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="724d7-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="724d7-125">Quando você encontrar o item de interesse, poderá modificar as propriedades do item e sair da iteração.</span><span class="sxs-lookup"><span data-stu-id="724d7-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="724d7-126">Se você fizer alterações em qualquer item de uma coleção, deverá chamar [**ICatalogCollection:: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para salvar as alterações no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="724d7-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="724d7-127">Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração de COM+ de nível superior; "ItemName" deve ser substituído pelo nome do item no qual você está interessado; "PropertyName" deve ser substituído pelo nome da propriedade que você está modificando no item; e varNewProp devem ser substituídos por uma variante que contém o novo valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="724d7-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


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



<span data-ttu-id="724d7-128">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+.</span><span class="sxs-lookup"><span data-stu-id="724d7-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="724d7-129">Um objeto COMAdminCatalogCollection pode ser criado chamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) em um objeto [**COMAdminCatalog**](comadmincatalog.md) ou [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="724d7-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="724d7-130">Chame o método [**popular**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para popular a coleção com todos os seus itens.</span><span class="sxs-lookup"><span data-stu-id="724d7-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="724d7-131">Iterar em cada um dos itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="724d7-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="724d7-132">Quando você encontrar o item de interesse, poderá modificar as propriedades do item e sair da iteração.</span><span class="sxs-lookup"><span data-stu-id="724d7-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="724d7-133">Se você fizer alterações em qualquer item de uma coleção, deverá chamar o método [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) do objeto **COMAdminCatalogCollection** para salvar as alterações no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="724d7-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="724d7-134">Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração de COM+ de nível superior; "ItemName" deve ser substituído pelo nome do item no qual você está interessado; "PropertyName" deve ser substituído pelo nome da propriedade que você está modificando no item; e NewPropValue devem ser substituídos pelo novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="724d7-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="724d7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="724d7-135">Requirements</span></span>



| <span data-ttu-id="724d7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="724d7-136">Requirement</span></span> | <span data-ttu-id="724d7-137">Valor</span><span class="sxs-lookup"><span data-stu-id="724d7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="724d7-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="724d7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="724d7-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="724d7-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="724d7-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="724d7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="724d7-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="724d7-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="724d7-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="724d7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="724d7-143"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="724d7-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="724d7-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="724d7-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="724d7-145"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="724d7-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724d7-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="724d7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724d7-147">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="724d7-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="724d7-148">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="724d7-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="724d7-149">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="724d7-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




