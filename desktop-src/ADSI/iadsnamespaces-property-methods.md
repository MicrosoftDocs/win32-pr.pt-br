---
title: Métodos de propriedade IADsNamespaces (IADs. h)
description: Os métodos de propriedade da interface IADsNamespaces obtêm e definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: fe959741-429e-480a-8111-3ebadaf55f77
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsNamespaces
topic_type:
- apiref
api_name:
- IADsNamespaces Property Methods
- IADsNamespaces.DefaultContainer
- IADsNamespaces.get_DefaultContainer
- IADsNamespaces.put_DefaultContainer
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b30467e931d7e8790f9a17542d5da2070525fe0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644948"
---
# <a name="iadsnamespaces-property-methods"></a><span data-ttu-id="acb45-105">Métodos de propriedade IADsNamespaces</span><span class="sxs-lookup"><span data-stu-id="acb45-105">IADsNamespaces Property Methods</span></span>

<span data-ttu-id="acb45-106">Os métodos de propriedade da interface [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) obtêm e definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="acb45-106">The [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) interface property methods get and set the properties described in the following table.</span></span> <span data-ttu-id="acb45-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="acb45-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="acb45-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="acb45-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="acb45-109">**DefaultContainer**</span><span class="sxs-lookup"><span data-stu-id="acb45-109">**DefaultContainer**</span></span>
<span data-ttu-id="acb45-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="acb45-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="acb45-111">A propriedade **defaultcontainer** identifica um objeto de contêiner de base ao qual você pode associar e usar como ponto de partida ao navegar.</span><span class="sxs-lookup"><span data-stu-id="acb45-111">The **DefaultContainer** property identifies a base container object to which you can bind and use as a starting point when browsing.</span></span> <span data-ttu-id="acb45-112">Esses dados são armazenados e recuperados do valor do registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="acb45-112">This data is stored and retrieved from the following registry value.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         ADs
            DefaultContainer
```

<span data-ttu-id="acb45-113">A ADSI define a propriedade **defaultcontainer** para fornecer uma maneira rápida de obter um ponteiro para um objeto de contêiner ADSI definido anteriormente.</span><span class="sxs-lookup"><span data-stu-id="acb45-113">ADSI defines the **DefaultContainer** property to provide a quick way of getting a pointer to a previously defined ADSI container object.</span></span>

<dt>

<span data-ttu-id="acb45-114">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="acb45-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="acb45-115">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="acb45-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultContainer(
  [out] BSTR* pbstrDefault
);
HRESULT put_DefaultContainer(
  [in] BSTR bstrDefault
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="acb45-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="acb45-116">Remarks</span></span>

<span data-ttu-id="acb45-117">Os provedores devem fornecer essa propriedade de acordo com o usuário.</span><span class="sxs-lookup"><span data-stu-id="acb45-117">Providers must supply this property on a per-user basis.</span></span> <span data-ttu-id="acb45-118">O contêiner padrão é definido imediatamente após a invocação de **IADsNamespaces::p UT \_ defaultcontainer**.</span><span class="sxs-lookup"><span data-stu-id="acb45-118">The default container is set immediately after the invocation of **IADsNamespaces::put\_DefaultContainer**.</span></span> <span data-ttu-id="acb45-119">Não é necessário chamar [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .</span><span class="sxs-lookup"><span data-stu-id="acb45-119">Calling [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) is not required.</span></span> <span data-ttu-id="acb45-120">Na verdade, o objeto namespaces fornecido pelo sistema retorna **E \_ NOTIMPL** para o método **IADs. setinfo** chamado neste objeto.</span><span class="sxs-lookup"><span data-stu-id="acb45-120">In fact, the system-supplied namespaces object returns **E\_NOTIMPL** for the **IADs.SetInfo** method called on this object.</span></span> <span data-ttu-id="acb45-121">Quando um contêiner é o objeto namespaces, uma operação de enumeração sempre resulta em uma lista de objetos de namespace específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="acb45-121">When a container is the namespaces object, an enumeration operation always results in a list of provider-specific namespace objects.</span></span> <span data-ttu-id="acb45-122">Quando [**IADsContainer. GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) é usado para obter um objeto de namespace, o parâmetro *bstrClass* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="acb45-122">When [**IADsContainer.GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) is used to obtain a namespace object, the *bstrClass* parameter is ignored.</span></span> <span data-ttu-id="acb45-123">Isso ocorre porque o contêiner, ou seja, o objeto namespaces, contém apenas um tipo de objeto, ou seja, objetos de namespace específicos do provedor.</span><span class="sxs-lookup"><span data-stu-id="acb45-123">This is because the container, that is, the namespaces object, contains only one type of object, namely, provider-specific namespace objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="acb45-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acb45-124">Requirements</span></span>



| <span data-ttu-id="acb45-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="acb45-125">Requirement</span></span> | <span data-ttu-id="acb45-126">Valor</span><span class="sxs-lookup"><span data-stu-id="acb45-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acb45-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb45-127">Minimum supported client</span></span><br/> | <span data-ttu-id="acb45-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acb45-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acb45-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="acb45-129">Minimum supported server</span></span><br/> | <span data-ttu-id="acb45-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acb45-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acb45-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="acb45-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="acb45-132"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="acb45-132"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="acb45-133">DLL</span><span class="sxs-lookup"><span data-stu-id="acb45-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acb45-134"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acb45-134"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="acb45-135">IID</span><span class="sxs-lookup"><span data-stu-id="acb45-135">IID</span></span><br/>                      | <span data-ttu-id="acb45-136">IID \_ IADsNamespaces é definido como 28B96BA0-B330-11CF-A9AD-00AA006BC149</span><span class="sxs-lookup"><span data-stu-id="acb45-136">IID\_IADsNamespaces is defined as 28B96BA0-B330-11CF-A9AD-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="acb45-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="acb45-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acb45-138">**IADsContainer. GetObject**</span><span class="sxs-lookup"><span data-stu-id="acb45-138">**IADsContainer.GetObject**</span></span>](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject)
</dt> <dt>

[<span data-ttu-id="acb45-139">**IADsNamespaces**</span><span class="sxs-lookup"><span data-stu-id="acb45-139">**IADsNamespaces**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)
</dt> <dt>

[<span data-ttu-id="acb45-140">Métodos de propriedade de interface</span><span class="sxs-lookup"><span data-stu-id="acb45-140">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





