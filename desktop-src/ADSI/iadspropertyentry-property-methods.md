---
title: Métodos de propriedade IADsPropertyEntry (IADs. h)
description: Forneça acesso às propriedades a seguir.
ms.assetid: 73b0f6d4-55db-46cf-a781-e10bc4fcf2db
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsPropertyEntry
topic_type:
- apiref
api_name:
- IADsPropertyEntry Property Methods
- IADsPropertyEntry.Name
- IADsPropertyEntry.get_Name
- IADsPropertyEntry.put_Name
- IADsPropertyEntry.ADsType
- IADsPropertyEntry.get_ADsType
- IADsPropertyEntry.put_ADsType
- IADsPropertyEntry.ControlCode
- IADsPropertyEntry.get_ControlCode
- IADsPropertyEntry.put_ControlCode
- IADsPropertyEntry.Values
- IADsPropertyEntry.get_Values
- IADsPropertyEntry.put_Values
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e82344b2b659395bb14c0500fde3214530e000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824768"
---
# <a name="iadspropertyentry-property-methods"></a><span data-ttu-id="e19cf-104">Métodos de propriedade IADsPropertyEntry</span><span class="sxs-lookup"><span data-stu-id="e19cf-104">IADsPropertyEntry Property Methods</span></span>

<span data-ttu-id="e19cf-105">Os métodos de propriedade da interface [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) fornecem acesso às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="e19cf-105">The property methods of the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) interface provide access to the following properties.</span></span> <span data-ttu-id="e19cf-106">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="e19cf-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e19cf-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e19cf-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="e19cf-108">**ADsType**</span><span class="sxs-lookup"><span data-stu-id="e19cf-108">**ADsType**</span></span>
<span data-ttu-id="e19cf-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e19cf-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="e19cf-110">O tipo de dados da propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="e19cf-110">The data type of the **Name** property.</span></span> <span data-ttu-id="e19cf-111">Os valores do tipo de dados são definidos na enumeração [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) .</span><span class="sxs-lookup"><span data-stu-id="e19cf-111">The values of the data type is defined in the [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) enumeration.</span></span>

<dt>

<span data-ttu-id="e19cf-112">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e19cf-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e19cf-113">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="e19cf-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsType(
  [out] LONG* plADsType
);
HRESULT put_ADsType(
  [in] LONG lADsType
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e19cf-114">**ControlCode**</span><span class="sxs-lookup"><span data-stu-id="e19cf-114">**ControlCode**</span></span>
<span data-ttu-id="e19cf-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e19cf-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="e19cf-116">Uma constante que especifica a operação a ser executada na propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="e19cf-116">A constant that specifies the operation to be performed on the named property.</span></span> <span data-ttu-id="e19cf-117">O valor é definido na enumeração de enumeração da [**\_ operação de propriedade \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .</span><span class="sxs-lookup"><span data-stu-id="e19cf-117">The value is defined in the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration.</span></span>

<dt>

<span data-ttu-id="e19cf-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e19cf-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e19cf-119">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="e19cf-119">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ControlCode(
  [out] LONG* pControlCode
);
HRESULT put_ControlCode(
  [in] LONG lnControlCode
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e19cf-120">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e19cf-120">**Name**</span></span>
<span data-ttu-id="e19cf-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e19cf-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="e19cf-122">Nome da entrada de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e19cf-122">Name of the property entry.</span></span> <span data-ttu-id="e19cf-123">Esse nome deve corresponder ao nome de um atributo, conforme definido no esquema.</span><span class="sxs-lookup"><span data-stu-id="e19cf-123">This name should correspond to the name of an attribute as defined in the schema.</span></span>

<dt>

<span data-ttu-id="e19cf-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e19cf-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e19cf-125">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="e19cf-125">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
HRESULT put_Name(
  [in] BSTR bstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="e19cf-126">**Valores**</span><span class="sxs-lookup"><span data-stu-id="e19cf-126">**Values**</span></span>
<span data-ttu-id="e19cf-127"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="e19cf-127"></dt> <dd> <dl></span></span>

<span data-ttu-id="e19cf-128">Uma matriz **variante** .</span><span class="sxs-lookup"><span data-stu-id="e19cf-128">A **VARIANT** array.</span></span> <span data-ttu-id="e19cf-129">Cada elemento nessa matriz representa um valor da propriedade nomeada.</span><span class="sxs-lookup"><span data-stu-id="e19cf-129">Each element in this array represents a value of the named property.</span></span> <span data-ttu-id="e19cf-130">Esses valores de propriedade são representados por objetos ADSI que implementam as interfaces [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) e [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) .</span><span class="sxs-lookup"><span data-stu-id="e19cf-130">Such property values are represented by ADSI objects implementing the [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) and [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2) interfaces.</span></span> <span data-ttu-id="e19cf-131">Portanto, a matriz **Variant** contém uma matriz de ponteiros para a interface [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) nos objetos ADSI que implementam as interfaces **IADsPropertyValue** e **IADsPropertyValue2** .</span><span class="sxs-lookup"><span data-stu-id="e19cf-131">Therefore, the **VARIANT** array holds an array of pointers to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface on the ADSI objects implementing the **IADsPropertyValue** and **IADsPropertyValue2** interfaces.</span></span>

<dt>

<span data-ttu-id="e19cf-132">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="e19cf-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="e19cf-133">Tipo de dados de script: **Variant**</span><span class="sxs-lookup"><span data-stu-id="e19cf-133">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Values(
  [out] VARIANT* pvValues
);
HRESULT put_Values(
  [in] VARIANT vValues
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="e19cf-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="e19cf-134">Remarks</span></span>

<span data-ttu-id="e19cf-135">Cada método de propriedade dá suporte aos valores de retorno **HRESULT** padrão, incluindo S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e19cf-135">Each property method supports the standard **HRESULT** return values, including S\_OK.</span></span> <span data-ttu-id="e19cf-136">Para obter mais informações sobre outros valores de retorno, consulte [códigos de erro ADSI](adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e19cf-136">For more information about other return values, see [ADSI Error Codes](adsi-error-codes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e19cf-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e19cf-137">Examples</span></span>

<span data-ttu-id="e19cf-138">O exemplo de código a seguir mostra como recuperar uma propriedade nomeada do cache e criar uma nova entrada de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e19cf-138">The following code example shows how to retrieve a named property from the cache and create a new property entry.</span></span>


```VB
 
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup

'------------------------------------------------------------
'----- Getting IADsPropertyEntry ----------------------------
'------------------------------------------------------------
 
' Create the property list object.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a named property entry object.
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)

' Insert code to do something with propEntry
Set propEntry = Nothing
 
'------------------------------------------------------------
'---- Setting IADsPropertyEntry -----------------------------
'------------------------------------------------------------
 
' Create a property value object.
Set propVal = New PropertyValue
 
'---- Property Value -----
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'---- Create a new Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' ---- Put the newly created property entry to the cache ----
propList.PutPropertyItem (propEntry)
 
' Commit the entry to the directory store.
propList.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing
```



<span data-ttu-id="e19cf-139">O exemplo de código a seguir mostra como obter uma propriedade nomeada de um cache.</span><span class="sxs-lookup"><span data-stu-id="e19cf-139">The following code example shows how to get a named property from a cache.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADs *pObj = NULL;
VARIANT var;
long valType = ADSTYPE_CASE_IGNORE_STRING;
 
VariantInit(&var);
 
// Bind to directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&pList);
if(FAILED(hr)){return;}
 
// Initialize the property cache.
hr = pList->QueryInterface(IID_IADs,(void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
pObj->GetInfo();
pObj->Release();
 
// Get a property entry.
hr = pList->GetPropertyItem(CComBSTR("description"), valType, &var);
pList->Release();
if(FAILED(hr)){goto Cleanup;}
hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&pEntry);
VariantClear(&var);
if(FAILED(hr)){goto Cleanup;}
 
// Get the name and the type of the property entry.
BSTR nm = NULL;
hr = pEntry->get_Name(&nm);
printf("Property name = %S\n",nm);
VariantClear(&var);
long at;
hr = pEntry->get_ADsType(&at);
printf("Property type = %d\n",a);

Cleanup:
    if(nm)
        SysFreeString(nm);

    if(pList)
        pList->Release();

    if(pEntry)
        pEntry->Release();

    if(pObj)
        pObj->Release();

    VariantClear(&var);
```



## <a name="requirements"></a><span data-ttu-id="e19cf-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e19cf-140">Requirements</span></span>



| <span data-ttu-id="e19cf-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e19cf-141">Requirement</span></span> | <span data-ttu-id="e19cf-142">Valor</span><span class="sxs-lookup"><span data-stu-id="e19cf-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e19cf-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e19cf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e19cf-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e19cf-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e19cf-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e19cf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e19cf-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e19cf-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e19cf-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e19cf-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19cf-148"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="e19cf-148"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="e19cf-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e19cf-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e19cf-150"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e19cf-150"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="e19cf-151">IID</span><span class="sxs-lookup"><span data-stu-id="e19cf-151">IID</span></span><br/>                      | <span data-ttu-id="e19cf-152">IID \_ IADsPropertyEntry é definido como 05792C8E-941F-11D0-8529-00C04FD8D503</span><span class="sxs-lookup"><span data-stu-id="e19cf-152">IID\_IADsPropertyEntry is defined as 05792C8E-941F-11D0-8529-00C04FD8D503</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="e19cf-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="e19cf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19cf-154">**\_enumeração de \_ operação de propriedade ADS \_**</span><span class="sxs-lookup"><span data-stu-id="e19cf-154">**ADS\_PROPERTY\_OPERATION\_ENUM**</span></span>](/windows/win32/api/iads/ne-iads-ads_property_operation_enum)
</dt> <dt>

[<span data-ttu-id="e19cf-155">Códigos de erro ADSI</span><span class="sxs-lookup"><span data-stu-id="e19cf-155">ADSI Error Codes</span></span>](adsi-error-codes.md)
</dt> <dt>

[<span data-ttu-id="e19cf-156">**ADSTYPEENUM**</span><span class="sxs-lookup"><span data-stu-id="e19cf-156">**ADSTYPEENUM**</span></span>](/windows/win32/api/iads/ne-iads-adstypeenum)
</dt> <dt>

[<span data-ttu-id="e19cf-157">**IADsPropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="e19cf-157">**IADsPropertyEntry**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)
</dt> <dt>

[<span data-ttu-id="e19cf-158">**IADsPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="e19cf-158">**IADsPropertyValue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)
</dt> <dt>

[<span data-ttu-id="e19cf-159">**IADsPropertyValue2**</span><span class="sxs-lookup"><span data-stu-id="e19cf-159">**IADsPropertyValue2**</span></span>](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)
</dt> <dt>

[<span data-ttu-id="e19cf-160">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="e19cf-160">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> </dl>

 

