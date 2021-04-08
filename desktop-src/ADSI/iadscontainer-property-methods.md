---
title: Métodos de propriedade IADsContainer (IADs. h)
description: Os métodos de propriedade da interface IADsContainer obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações e uma discussão geral sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: 74d348bf-7b7f-4971-ba03-f77940600674
ms.tgt_platform: multiple
keywords:
- ADSI dos métodos de propriedade IADsContainer
topic_type:
- apiref
api_name:
- IADsContainer Property Methods
- IADsContainer.Count
- IADsContainer.get_Count
- IADsContainer.Filter
- IADsContainer.get_Filter
- IADsContainer.put_Filter
- IADsContainer.Hints
- IADsContainer.get_Hints
- IADsContainer.put_Hints
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5196addda0d9ff89f8a4976f3197bbeeae07044
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086046"
---
# <a name="iadscontainer-property-methods"></a><span data-ttu-id="07296-105">Métodos de propriedade IADsContainer</span><span class="sxs-lookup"><span data-stu-id="07296-105">IADsContainer Property Methods</span></span>

<span data-ttu-id="07296-106">Os métodos de propriedade da interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="07296-106">The property methods of the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="07296-107">Para obter mais informações e uma discussão geral sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="07296-107">For more information, and a general discussion about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="07296-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="07296-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="07296-109">**Count**</span><span class="sxs-lookup"><span data-stu-id="07296-109">**Count**</span></span>
<span data-ttu-id="07296-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="07296-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="07296-111">Recupera o número de itens no contêiner.</span><span class="sxs-lookup"><span data-stu-id="07296-111">Retrieves the number of items in the container.</span></span> <span data-ttu-id="07296-112">Quando **Filter** é definido, **Count** retorna apenas o número de itens filtrados.</span><span class="sxs-lookup"><span data-stu-id="07296-112">When **Filter** is set, **Count** returns only the number of filtered items.</span></span>

<dt>

<span data-ttu-id="07296-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="07296-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07296-114">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="07296-114">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Count(
  [out] LONG* plCount
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="07296-115">**Filter**</span><span class="sxs-lookup"><span data-stu-id="07296-115">**Filter**</span></span>
<span data-ttu-id="07296-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="07296-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="07296-117">Recupera ou define o filtro usado para selecionar classes de objeto em uma determinada enumeração.</span><span class="sxs-lookup"><span data-stu-id="07296-117">Retrieves or sets the filter used to select object classes in a given enumeration.</span></span> <span data-ttu-id="07296-118">Essa é uma matriz variante, cada elemento de que é o nome de uma classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="07296-118">This is a variant array, each element of which is the name of a schema class.</span></span> <span data-ttu-id="07296-119">Se o **filtro** não estiver definido ou definido como vazio, todos os objetos de todas as classes serão recuperados pelo enumerador.</span><span class="sxs-lookup"><span data-stu-id="07296-119">If **Filter** is not set or set to empty, all objects of all classes are retrieved by the enumerator.</span></span>

<dt>

<span data-ttu-id="07296-120">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07296-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="07296-121">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="07296-121">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Filter(
  [out] VARIANT* pvFilter
);
HRESULT put_Filter(
  [in] VARIANT vFilter
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="07296-122">**Dicas**</span><span class="sxs-lookup"><span data-stu-id="07296-122">**Hints**</span></span>
<span data-ttu-id="07296-123"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="07296-123"></dt> <dd> <dl></span></span>

<span data-ttu-id="07296-124">Uma matriz variante de cadeias de caracteres **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="07296-124">A variant array of **BSTR** strings.</span></span> <span data-ttu-id="07296-125">Cada elemento identifica o nome de uma propriedade encontrada na definição de esquema.</span><span class="sxs-lookup"><span data-stu-id="07296-125">Each element identifies the name of a property found in the schema definition.</span></span> <span data-ttu-id="07296-126">O parâmetro *vHints* permite que o cliente indique quais atributos carregar para cada objeto enumerado.</span><span class="sxs-lookup"><span data-stu-id="07296-126">The *vHints* parameter enables the client to indicate which attributes to load for each enumerated object.</span></span> <span data-ttu-id="07296-127">Esses dados podem ser usados para otimizar o acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="07296-127">Such data may be used to optimize network access.</span></span> <span data-ttu-id="07296-128">A implementação exata, no entanto, é específica do provedor e não é usada no momento pelo provedor do WinNT.</span><span class="sxs-lookup"><span data-stu-id="07296-128">The exact implementation, however, is provider-specific, and is currently not used by the WinNT provider.</span></span>

<dt>

<span data-ttu-id="07296-129">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="07296-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="07296-130">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="07296-130">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Hints(
  [out] VARIANT* pvHints
);
HRESULT put_Hints(
  [in] VARIANT vHints
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="07296-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="07296-131">Remarks</span></span>

<span data-ttu-id="07296-132">Os processos de enumeração na contagem [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) e **IADsContainer: \_ : Get** são executados em relação aos objetos contidos no cache.</span><span class="sxs-lookup"><span data-stu-id="07296-132">The enumeration processes under [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) and **IADsContainer::get\_Count** are performed against the contained objects in the cache.</span></span> <span data-ttu-id="07296-133">Quando um contêiner contém um grande número de objetos, o desempenho pode ser afetado.</span><span class="sxs-lookup"><span data-stu-id="07296-133">When a container contains a large number of objects, the performance may be affected.</span></span> <span data-ttu-id="07296-134">Para melhorar o desempenho, desative o cache, configure um tamanho de página apropriado e use a interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="07296-134">To enhance performance, turn off the cache, set up an appropriate page size, and use the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="07296-135">Por esse motivo, a propriedade **obter \_ contagem** não tem suporte no provedor LDAP da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="07296-135">For this reason, the **get\_Count** property is not supported in the Microsoft LDAP provider.</span></span>

## <a name="examples"></a><span data-ttu-id="07296-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="07296-136">Examples</span></span>

<span data-ttu-id="07296-137">O exemplo de código a seguir Visual Basic mostra como os métodos de propriedade de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="07296-137">The following Visual Basic code example shows how property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span>


```VB
Dim cont As IADsContainer
Dim usr As IADsUser

On Error GoTo Cleanup
 
Set cont = GetObject("LDAP://OU=Sales, DC=Fabrikam, DC=COM")
cont.Hints = Array("adminDescription") ' Load this attribute. Optional.
Debug.Print cont.Get("adminDescription")

' Filter users.
cont.Filter = Array("user")

For Each usr In cont
  Debug.Print usr.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cont = Nothing
    Set usr = Nothing
```



<span data-ttu-id="07296-138">O exemplo de código C++ a seguir mostra como os métodos de propriedade de [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="07296-138">The following C++ code example shows how the property methods of [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) can be used.</span></span> <span data-ttu-id="07296-139">Para brevidade, a verificação de erros é omitida.</span><span class="sxs-lookup"><span data-stu-id="07296-139">For brevity, error checking is omitted.</span></span>


```C++
IADsContainer *pCont;
IADs *pChild;
IADs *pADs;
 
HRESULT hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=COM",
                          IID_IADsContainer, 
                          (void**)&pCont);

if(FAILED(hr)){goto Cleanup;}

LPWSTR pszArray[] = { L"adminDescription" };
DWORD dwNumber = sizeof(pszArray)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr( pszArray, dwNumber, &var);
if(FAILED(hr)){goto Cleanup;}

hr = pCont->put_Hints( var );
if(FAILED(hr)){goto Cleanup;}

VariantClear(&var);
 
hr = pCont->QueryInterface(IID_IADs, (void**)pADs);
if(FAILED(hr)){goto Cleanup;}
 
hr = pADs->Get(CComBSTR("adminDescription"), var);
 
LPWSTR pszUsers = {L"user"};
dwNumber = sizeof(pszUsers)/sizeof(LPWSTR);
hr = ADsBuildVarArrayStr(pszUsers, dwNumber, &var);
hr = pCont->put_Filter( var );
VariantClear(&var);
 
// Enumerate user objects in the container.
IEnumVARIANT *pEnum = NULL;
hr = ADsBuildEnumerator(pCont, &pEnum);
pCont->Release();    // Not required when users are enumerated.
 
ULONG lFetch;
VariantClear(&var);
while (SUCCEEDED(ADsEnumerateNext(pEnum, 1, &var, &lFetch)) && 
                      lFetch==1) {
    hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pChild)
    if(SUCCEEDED(hr)) {
        BSTR bstrName;
        pChild->get_Name(&bstrName);
        printf("  %S\n", bstrName);
        SysFreeString(bstrName);
        pChild->Release();
    }
    VariantClear(&var);
}
Cleanup:
    if(pADs)
        pADs->Release();

    if(pCont)
        pCont->Release();

    if(pChild)
        pChild->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="07296-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07296-140">Requirements</span></span>



| <span data-ttu-id="07296-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="07296-141">Requirement</span></span> | <span data-ttu-id="07296-142">Valor</span><span class="sxs-lookup"><span data-stu-id="07296-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07296-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07296-143">Minimum supported client</span></span><br/> | <span data-ttu-id="07296-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07296-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07296-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07296-145">Minimum supported server</span></span><br/> | <span data-ttu-id="07296-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07296-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07296-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07296-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="07296-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="07296-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="07296-149">DLL</span><span class="sxs-lookup"><span data-stu-id="07296-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07296-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07296-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="07296-151">IID</span><span class="sxs-lookup"><span data-stu-id="07296-151">IID</span></span><br/>                      | <span data-ttu-id="07296-152">IID \_ IADsContainer é definido como 001677D0-FD16-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="07296-152">IID\_IADsContainer is defined as 001677D0-FD16-11CE-ABC4-02608C9E7553</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="07296-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="07296-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07296-154">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="07296-154">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> <dt>

[<span data-ttu-id="07296-155">**IDirectorySearch**</span><span class="sxs-lookup"><span data-stu-id="07296-155">**IDirectorySearch**</span></span>](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
</dt> </dl>

 

 





