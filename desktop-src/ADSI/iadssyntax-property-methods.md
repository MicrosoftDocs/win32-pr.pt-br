---
title: Métodos de propriedade IADsSyntax (IADs. h)
description: Os métodos de propriedade da interface IADsSyntax obtêm ou definem as propriedades listadas na tabela a seguir. Para obter mais informações sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: a216a55d-63eb-4fdf-a67f-8d4b5eb74262
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsSyntax
topic_type:
- apiref
api_name:
- IADsSyntax Property Methods
- IADsSyntax.OleAutoDataType
- IADsSyntax.get_OleAutoDataType
- IADsSyntax.put_OleAutoDataType
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7a41c84efb4f48171913156823e18a301236290
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499334"
---
# <a name="iadssyntax-property-methods"></a><span data-ttu-id="3f826-105">Métodos de propriedade IADsSyntax</span><span class="sxs-lookup"><span data-stu-id="3f826-105">IADsSyntax Property Methods</span></span>

<span data-ttu-id="3f826-106">Os métodos de propriedade da interface [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) obtêm ou definem as propriedades listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f826-106">The property methods of the [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) interface get or set the properties listed in the following table.</span></span> <span data-ttu-id="3f826-107">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3f826-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3f826-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3f826-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3f826-109">**OleAutoDataType**</span><span class="sxs-lookup"><span data-stu-id="3f826-109">**OleAutoDataType**</span></span>
<span data-ttu-id="3f826-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3f826-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3f826-111">Recupera e define um **Long** que contém o valor da constante **VT \_ xxx** para o tipo de dados Automation que representa essa sintaxe.</span><span class="sxs-lookup"><span data-stu-id="3f826-111">Retrieves and sets a **LONG** that contains the value of the **VT\_xxx** constant for the Automation data type that represents this syntax.</span></span>

<span data-ttu-id="3f826-112">Active Directory dá suporte às seguintes constantes **VT \_ xxx** para o tipo de dados de automação que representa essa sintaxe:</span><span class="sxs-lookup"><span data-stu-id="3f826-112">Active Directory supports the following **VT\_xxx** constants for the Automation data type that represents this syntax:</span></span>

-   <span data-ttu-id="3f826-113">**VT \_ bool bool**</span><span class="sxs-lookup"><span data-stu-id="3f826-113">**VT\_BOOL** BOOL</span></span>
-   <span data-ttu-id="3f826-114">**VT \_ BSTR de** BSTR</span><span class="sxs-lookup"><span data-stu-id="3f826-114">**VT\_BSTR** BSTR</span></span>
-   <span data-ttu-id="3f826-115">**VT \_ Bstrt**</span><span class="sxs-lookup"><span data-stu-id="3f826-115">**VT\_BSTRT** BSTRT</span></span>
-   <span data-ttu-id="3f826-116">**VT \_ moeda CY**</span><span class="sxs-lookup"><span data-stu-id="3f826-116">**VT\_CY** CURRENCY</span></span>
-   <span data-ttu-id="3f826-117">**VT \_** Data de data</span><span class="sxs-lookup"><span data-stu-id="3f826-117">**VT\_DATE** Date</span></span>
-   <span data-ttu-id="3f826-118">**VT \_** **nulo** vazio</span><span class="sxs-lookup"><span data-stu-id="3f826-118">**VT\_EMPTY** **NULL**</span></span>
-   <span data-ttu-id="3f826-119">**VT \_ ERRO** inválido</span><span class="sxs-lookup"><span data-stu-id="3f826-119">**VT\_ERROR** Not valid</span></span>
-   <span data-ttu-id="3f826-120">**VT \_ I2** curto</span><span class="sxs-lookup"><span data-stu-id="3f826-120">**VT\_I2** short</span></span>
-   <span data-ttu-id="3f826-121">**VT \_ I4** longo</span><span class="sxs-lookup"><span data-stu-id="3f826-121">**VT\_I4** long</span></span>
-   <span data-ttu-id="3f826-122">**VT \_ R4** real</span><span class="sxs-lookup"><span data-stu-id="3f826-122">**VT\_R4** real</span></span>
-   <span data-ttu-id="3f826-123">**VT \_ R8** dupla</span><span class="sxs-lookup"><span data-stu-id="3f826-123">**VT\_R8** double</span></span>
-   <span data-ttu-id="3f826-124">**VT \_ UI1** byte</span><span class="sxs-lookup"><span data-stu-id="3f826-124">**VT\_UI1** BYTE</span></span>

<dt>

<span data-ttu-id="3f826-125">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3f826-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3f826-126">Tipo de dados de script: **longo**</span><span class="sxs-lookup"><span data-stu-id="3f826-126">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OleAutoDataType(
  [out] LONG* plAutoDataType
);
HRESULT put_OleAutoDataType(
  [in] LONG lAutoDataType
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="3f826-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f826-127">Remarks</span></span>

<span data-ttu-id="3f826-128">Uma matriz de bytes não assinados, a matriz **VT \_ UI1** \| **\_ VT** pode significar que o provedor mapeou uma sintaxe que não pode ser mapeada para um tipo de virtual de automação.</span><span class="sxs-lookup"><span data-stu-id="3f826-128">An array of unsigned bytes, **VT\_UI1**\|**VT\_ARRAY** could mean that the provider has mapped a syntax that cannot be mapped to an Automation virtual type.</span></span>

## <a name="examples"></a><span data-ttu-id="3f826-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3f826-129">Examples</span></span>

<span data-ttu-id="3f826-130">O exemplo de código a seguir examina a sintaxe do atributo **OperatingSystemVersion** de um computador em uma rede por meio do provedor Winnt.</span><span class="sxs-lookup"><span data-stu-id="3f826-130">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="3f826-131">A sintaxe do resultado é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3f826-131">The result syntax is a string.</span></span>


```VB
Dim obj As IADs
Dim cl As IADsClass
Dim pr As IADsProperty
Dim sy As IADsSyntax
Dim sc As IADsContainer
On Error GoTo Cleanup

Set obj = GetObject("WinNT://myMachine,computer")
Set cl = GetObject(obj.Schema)
Set sc = GetObject(cl.Parent)
Set pr = sc.GetObject("Property","OperatingSystemVersion")
Set sy = GetObject(sc.ADsPath & "/" & pr.Syntax)
 
MsgBox "Automation data types: " & sy.OleAutoDataType

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set obj = Nothing
    Set cl = Nothing
    Set pr = Nothing
    Set sy = Nothing
    Set sc = Nothing
```



<span data-ttu-id="3f826-132">O exemplo de código a seguir examina a sintaxe do atributo **OperatingSystemVersion** de um computador em uma rede por meio do provedor Winnt.</span><span class="sxs-lookup"><span data-stu-id="3f826-132">The following code example examines the syntax of the **OperatingSystemVersion** attribute of a computer on a network through the WinNT provider.</span></span> <span data-ttu-id="3f826-133">A sintaxe do resultado é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3f826-133">The result syntax is a string.</span></span> <span data-ttu-id="3f826-134">Para brevidade, a verificação de erros é omitida.</span><span class="sxs-lookup"><span data-stu-id="3f826-134">For brevity, error checking is omitted.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
#include <atlbase.h>
 
IADs *pObj = NULL;
IADsClass *pCls = NULL;
IADsProperty *pProp = NULL;
IADsSyntax *pSyn = NULL;
IADsContainer *pCont = NULL;
 
HRESULT hr = ADsGetObject(L"WinNT://myMachine,computer",
                          IID_IADs,
                          (void**)&pObj);
if(FAILED(hr)){goto Cleanup;}
VARIANT var;
VariantInit(&var);
CComBSTR sbstr;
 
pObj->get_Schema(&sbstr);
printf("Object schema: %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsClass,(void**)&pCls);
if(FAILED(hr)){goto Cleanup;}

pCls->get_Parent(&sbstr);
printf("Object class's container:  %S\n", sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsContainer, (void**)&pCont);
if(FAILED(hr)){goto Cleanup;}
pCont->QueryInterface(IID_IADs,(void**)&pObj);
pObj->get_ADsPath(&sbstr);
printf("Container's AdsPath:  %S\n",sbstr);
 
IDispatch *pDisp;
hr = pCont->GetObject(CComBSTR("Property"),
                      CComBSTR("OperatingSystemVersion"),
                      (IDispatch**)&pDisp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pDisp->QueryInterface(IID_IADsProperty, (void**)&pProp);
if(FAILED(hr)){goto Cleanup;}
 
hr = pProp->get_Syntax(&sbstr);
if(FAILED(hr)){goto Cleanup;}
printf("Property Syntax:  %S\n",sbstr);
 
printf("ADsPath of the syntax object %S\n",sbstr);
 
hr = ADsGetObject(sbstr, IID_IADsSyntax, (void**)&pSyn);
if(FAILED(hr)){goto Cleanup;}

long lType;
pSyn->get_OleAutoDataType(&lType);
printf("Property syntax's OleAutoDataType: %d\n", lType);

Cleanup:
    if(pObj)
        pObj->Release();

    if(pProp)
        pProp->Release();

    if(pCls)
        pCls->Release();

    if(pSyn)
        pSyn->Release();

    if(pCont)
        pCont->Release();
```



## <a name="requirements"></a><span data-ttu-id="3f826-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f826-135">Requirements</span></span>



| <span data-ttu-id="3f826-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f826-136">Requirement</span></span> | <span data-ttu-id="3f826-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3f826-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f826-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f826-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3f826-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f826-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3f826-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f826-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3f826-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3f826-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3f826-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f826-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f826-143"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f826-143"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="3f826-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3f826-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f826-145"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f826-145"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="3f826-146">IID</span><span class="sxs-lookup"><span data-stu-id="3f826-146">IID</span></span><br/>                      | <span data-ttu-id="3f826-147">IID \_ IADsSyntax é definido como C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span><span class="sxs-lookup"><span data-stu-id="3f826-147">IID\_IADsSyntax is defined as C8F93DD2-4AE0-11CF-9E73-00AA004A5691</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="3f826-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f826-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f826-149">**IADsClass**</span><span class="sxs-lookup"><span data-stu-id="3f826-149">**IADsClass**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsclass)
</dt> <dt>

[<span data-ttu-id="3f826-150">**IADsproperty**</span><span class="sxs-lookup"><span data-stu-id="3f826-150">**IADsProperty**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsproperty)
</dt> <dt>

[<span data-ttu-id="3f826-151">**IADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="3f826-151">**IADsSyntax**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssyntax)
</dt> </dl>

 

 





