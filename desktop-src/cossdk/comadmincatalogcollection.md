---
description: Representa qualquer coleção no catálogo COM+. Use-o para enumerar, adicionar, remover e recuperar itens em uma coleção e para acessar coleções relacionadas.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: Classe COMAdminCatalogCollection (COMAdmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646440"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="91a91-104">Classe COMAdminCatalogCollection</span><span class="sxs-lookup"><span data-stu-id="91a91-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="91a91-105">Representa qualquer coleção no catálogo COM+.</span><span class="sxs-lookup"><span data-stu-id="91a91-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="91a91-106">Use-o para enumerar, adicionar, remover e recuperar itens em uma coleção e para acessar coleções relacionadas.</span><span class="sxs-lookup"><span data-stu-id="91a91-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="91a91-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="91a91-107">When to implement</span></span>

<span data-ttu-id="91a91-108">Essa classe é implementada pelo COM+.</span><span class="sxs-lookup"><span data-stu-id="91a91-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="91a91-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a91-109">Requirement</span></span> | <span data-ttu-id="91a91-110">Valor</span><span class="sxs-lookup"><span data-stu-id="91a91-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="91a91-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="91a91-111">Interfaces</span></span> | [<span data-ttu-id="91a91-112">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="91a91-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="91a91-113">Quando usar</span><span class="sxs-lookup"><span data-stu-id="91a91-113">When to use</span></span>

<span data-ttu-id="91a91-114">Use objetos criados a partir da classe **COMAdminCatalogCollection** quando desejar manipular programaticamente uma coleção no catálogo com+.</span><span class="sxs-lookup"><span data-stu-id="91a91-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="91a91-115">Essas coleções correspondem às pastas na ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="91a91-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="91a91-116">Os itens dentro das pastas correspondem a itens em coleções, que você pode representar usando objetos criados a partir da classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="91a91-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="91a91-117">Para obter informações sobre as coleções no catálogo e suas propriedades, consulte [coleções de administração do com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="91a91-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="91a91-118">Para obter uma introdução à administração programática do COM+, consulte [automatizando a administração do com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="91a91-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="91a91-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="91a91-119">Remarks</span></span>

<span data-ttu-id="91a91-120">Você não pode criar diretamente um objeto **COMAdminCatalogCollection** .</span><span class="sxs-lookup"><span data-stu-id="91a91-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="91a91-121">Para usar os métodos desse objeto, você deve criar um objeto [**COMAdminCatalog**](comadmincatalog.md) , obter uma referência a [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)e, em seguida, usar [**ICOMAdminCatalog:: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) para obter uma referência a uma interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) que representa uma coleção de nível superior.</span><span class="sxs-lookup"><span data-stu-id="91a91-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="91a91-122">Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração COM+ de nível superior.</span><span class="sxs-lookup"><span data-stu-id="91a91-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="91a91-123">Para usar essa classe do Microsoft Visual Basic, adicione uma referência à biblioteca de tipos de administrador do COM+.</span><span class="sxs-lookup"><span data-stu-id="91a91-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="91a91-124">Um objeto COMAdminCatalogCollection pode ser criado chamando [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) em um objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="91a91-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="91a91-125">Isso é mostrado no exemplo a seguir, em que "TopCollection" deve ser substituído pelo nome de uma das coleções de administração COM+ de nível superior.</span><span class="sxs-lookup"><span data-stu-id="91a91-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="91a91-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91a91-126">Requirements</span></span>



| <span data-ttu-id="91a91-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a91-127">Requirement</span></span> | <span data-ttu-id="91a91-128">Valor</span><span class="sxs-lookup"><span data-stu-id="91a91-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91a91-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91a91-129">Minimum supported client</span></span><br/> | <span data-ttu-id="91a91-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="91a91-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="91a91-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91a91-131">Minimum supported server</span></span><br/> | <span data-ttu-id="91a91-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="91a91-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="91a91-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="91a91-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a91-134"><dt>COMAdmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a91-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="91a91-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="91a91-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="91a91-136"><dt>COMAdmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="91a91-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91a91-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="91a91-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a91-138">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="91a91-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="91a91-139">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="91a91-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="91a91-140">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="91a91-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




