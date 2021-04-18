---
title: Métodos da propriedade IADsproperty (IADs. h)
description: Leia e grave as propriedades descritas na tabela a seguir.
ms.assetid: dd348a3c-0386-4fa2-984d-cdea6f09bd72
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADsproperty ADSI
topic_type:
- apiref
api_name:
- IADsProperty Property Methods
- IADsProperty.OID
- IADsProperty.get_OID
- IADsProperty.put_OID
- IADsProperty.Syntax
- IADsProperty.get_Syntax
- IADsProperty.put_Syntax
- IADsProperty.MaxRange
- IADsProperty.get_MaxRange
- IADsProperty.put_MaxRange
- IADsProperty.MinRange
- IADsProperty.get_MinRange
- IADsProperty.put_MinRange
- IADsProperty.MultiValued
- IADsProperty.get_MultiValued
- IADsProperty.put_MultiValued
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233bd5411e1c82956ef745255418a1b176af5900
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771761"
---
# <a name="iadsproperty-property-methods"></a><span data-ttu-id="390eb-104">Métodos da propriedade IADsproperty</span><span class="sxs-lookup"><span data-stu-id="390eb-104">IADsProperty Property Methods</span></span>

<span data-ttu-id="390eb-105">Os métodos de propriedade da interface [**iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) lêem e gravam as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="390eb-105">The property methods of the [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) interface read and write the properties described in the following table.</span></span> <span data-ttu-id="390eb-106">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="390eb-106">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="390eb-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="390eb-107">Properties</span></span>

<dl> <dt>

<span data-ttu-id="390eb-108">**MaxRange**</span><span class="sxs-lookup"><span data-stu-id="390eb-108">**MaxRange**</span></span>
<span data-ttu-id="390eb-109"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="390eb-109"></dt> <dd> <dl></span></span>

<span data-ttu-id="390eb-110">Limite superior de valores.</span><span class="sxs-lookup"><span data-stu-id="390eb-110">Upper limit of values.</span></span>

<dt>

<span data-ttu-id="390eb-111">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="390eb-111">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="390eb-112">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="390eb-112">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxRange(
  [out] LONG* lnMaxRange
);
HRESULT put_MaxRange(
  [in] LONG lnMaxRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="390eb-113">**MinRange**</span><span class="sxs-lookup"><span data-stu-id="390eb-113">**MinRange**</span></span>
<span data-ttu-id="390eb-114"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="390eb-114"></dt> <dd> <dl></span></span>

<span data-ttu-id="390eb-115">Limite inferior de valores.</span><span class="sxs-lookup"><span data-stu-id="390eb-115">Lower limit of values.</span></span>

<dt>

<span data-ttu-id="390eb-116">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="390eb-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="390eb-117">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="390eb-117">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinRange(
  [out] LONG* lnMinRange
);
HRESULT put_MinRange(
  [in] LONG lnMinRange
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="390eb-118">**Múltiplos valores**</span><span class="sxs-lookup"><span data-stu-id="390eb-118">**MultiValued**</span></span>
<span data-ttu-id="390eb-119"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="390eb-119"></dt> <dd> <dl></span></span>

<span data-ttu-id="390eb-120">Se a propriedade oferece suporte a valores únicos ou múltiplos.</span><span class="sxs-lookup"><span data-stu-id="390eb-120">Whether property supports single or multiple values.</span></span>

<dt>

<span data-ttu-id="390eb-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="390eb-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="390eb-122">Tipo de dados Scripting: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="390eb-122">Scripting data type: **VARIANT\_BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MultiValued(
  [out] VARIANT_BOOL* fMultivalued
);
HRESULT put_MultiValued(
  [in] VARIANT_BOOL fMultivalued
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="390eb-123">**OIDs**</span><span class="sxs-lookup"><span data-stu-id="390eb-123">**OID**</span></span>
<span data-ttu-id="390eb-124"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="390eb-124"></dt> <dd> <dl></span></span>

<span data-ttu-id="390eb-125">Identificador de objeto específico do diretório.</span><span class="sxs-lookup"><span data-stu-id="390eb-125">Directory-specific object identifier.</span></span>

<dt>

<span data-ttu-id="390eb-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="390eb-126">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="390eb-127">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="390eb-127">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OID(
  [out] BSTR* bstrOID
);
HRESULT put_OID(
  [out] BSTR* bstrOID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="390eb-128">**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="390eb-128">**Syntax**</span></span>
<span data-ttu-id="390eb-129"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="390eb-129"></dt> <dd> <dl></span></span>

<span data-ttu-id="390eb-130">Caminho relativo do objeto de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="390eb-130">Relative path of syntax object.</span></span>

<dt>

<span data-ttu-id="390eb-131">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="390eb-131">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="390eb-132">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="390eb-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Syntax(
  [out] BSTR* bstrSyntax
);
HRESULT put_Syntax(
  [in] BSTR* bstrSyntax
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="390eb-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="390eb-133">Examples</span></span>

<span data-ttu-id="390eb-134">O exemplo de código a seguir examina o atributo **OperatingSystem** de um computador em uma rede por meio do provedor Winnt.</span><span class="sxs-lookup"><span data-stu-id="390eb-134">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sc As IADsContainer

On Error GoTo Cleanup
 
Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystem")
 
MsgBox "Attribute:  " & pr.Name
MsgBox "Syntax:     " & pr.Syntax
MsgBox "MaxRange:   " & pr.MaxRange
MsgBox "MinRange:   " & pr.MinRange
MsgBox "Multivalued:" & pr.Multivalued

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sc = Nothing
```



<span data-ttu-id="390eb-135">O exemplo de código a seguir examina o atributo **OperatingSystem** de um computador em uma rede por meio do provedor Winnt.</span><span class="sxs-lookup"><span data-stu-id="390eb-135">The following code example examines the **OperatingSystem** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="390eb-136">Para brevidade, a verificação de erros é omitida.</span><span class="sxs-lookup"><span data-stu-id="390eb-136">For brevity, error checking is omitted.</span></span>


```C++
IADs *pADs = NULL;
IADsClass *pCls = NULL;
IADsProperty* pProp = NULL;
IADsContainer *pCont = NULL;
long lval;
short bval;
HRESULT hr = CoInitialize(NULL);
 
hr = ADsGetObject(L"WinNT://myMachine,computer",
                  IID_IADs, (void**)&pADs);
if(FAILED(hr))
    goto Cleanup;

BSTR bstr;
hr = pADs->get_Schema(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsClass, (void**)&pCls);
hr = pCls->get_Parent(&bstr);
if(FAILED(hr))
    goto Cleanup;

hr = ADsGetObject(bstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr))
    goto Cleanup;
SysFreeString(bstr);

hr = pCont->GetObject(CComBSTR("Property"), CComBSTR("OperatingSystem"), (IDispatch**)&pProp);
if(FAILED(hr))
    goto Cleanup;

hr = pProp->get_Name(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Name : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_Syntax(&bstr);
if(FAILED(hr))
    goto Cleanup;
printf(" Syntax : %S\n",bstr);
SysFreeString(bstr);

hr = pProp->get_MaxRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MaxRange : %d\n",lval);
SysFreeString(bstr);

hr = pProp->get_MinRange(&lval);
if(FAILED(hr))
    goto Cleanup;
printf(" MinRange : %d\n", lval);
SysFreeString(bstr);

hr = pProp->get_Multivalued(&bval);
if(FAILED(hr))
    goto Cleanup;
printf(" MultiValued : %b\n",bval);
SysFreeString(bstr);

Cleanup:
    if(pADs)
        pADs->Release();

    if(pCls)
        pCls->Release();

    if(pCont)
        pCont->Release();

    if(pProp)
        pProp->Release(); 
 
CoUninitialize();
```



## <a name="requirements"></a><span data-ttu-id="390eb-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="390eb-137">Requirements</span></span>



| <span data-ttu-id="390eb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="390eb-138">Requirement</span></span> | <span data-ttu-id="390eb-139">Valor</span><span class="sxs-lookup"><span data-stu-id="390eb-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="390eb-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="390eb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="390eb-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="390eb-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="390eb-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="390eb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="390eb-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="390eb-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="390eb-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="390eb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="390eb-145"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="390eb-145"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="390eb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="390eb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="390eb-147"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="390eb-147"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="390eb-148">IID</span><span class="sxs-lookup"><span data-stu-id="390eb-148">IID</span></span><br/>                      | <span data-ttu-id="390eb-149">IID \_ iadsproperty é definido como C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="390eb-149">IID\_IADsProperty is defined as C8F93DD3-4AE0-11CF-9E73-00AA004A5691</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="390eb-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="390eb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390eb-151">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="390eb-151">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="390eb-152">**IADsproperty**</span><span class="sxs-lookup"><span data-stu-id="390eb-152">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="390eb-153">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="390eb-153">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





