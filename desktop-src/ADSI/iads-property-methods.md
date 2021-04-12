---
title: Métodos de propriedade IADs (IADs. h)
description: Os métodos de propriedade da interface IADs obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações sobre métodos de propriedade, consulte interface Property Methods.
ms.assetid: d2f6f686-a35a-4a9a-9b57-2ceb2f26ef12
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade IADs ADSI
topic_type:
- apiref
api_name:
- IADs Property Methods
- IADs.ADsPath
- IADs.get_ADsPath
- IADs.Class
- IADs.get_Class
- IADs.GUID
- IADs.get_GUID
- IADs.Name
- IADs.get_Name
- IADs.Parent
- IADs.get_Parent
- IADs.Schema
- IADs.get_Schema
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1134260c780958bcdba8d1f14eac535ddbf4ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499259"
---
# <a name="iads-property-methods"></a><span data-ttu-id="7f69e-105">Métodos de propriedade IADs</span><span class="sxs-lookup"><span data-stu-id="7f69e-105">IADs Property Methods</span></span>

<span data-ttu-id="7f69e-106">Os métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f69e-106">The property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="7f69e-107">Para obter mais informações sobre métodos de propriedade, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="7f69e-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="7f69e-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7f69e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="7f69e-109">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="7f69e-109">**ADsPath**</span></span>
<span data-ttu-id="7f69e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7f69e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="7f69e-111">A cadeia de caracteres ADsPath deste objeto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-111">The ADsPath string of this object.</span></span> <span data-ttu-id="7f69e-112">A cadeia de caracteres identifica exclusivamente esse objeto em um ambiente de rede.</span><span class="sxs-lookup"><span data-stu-id="7f69e-112">The string uniquely identifies this object in a network environment.</span></span> <span data-ttu-id="7f69e-113">O objeto sempre pode ser recuperado usando esse caminho.</span><span class="sxs-lookup"><span data-stu-id="7f69e-113">The object can always be retrieved using this path.</span></span>

<dt>

<span data-ttu-id="7f69e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f69e-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f69e-115">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f69e-115">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ADsPath(
  [out] BSTR* pbstrADsPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7f69e-116">**Classe**</span><span class="sxs-lookup"><span data-stu-id="7f69e-116">**Class**</span></span>
<span data-ttu-id="7f69e-117"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7f69e-117"></dt> <dd> <dl></span></span>

<span data-ttu-id="7f69e-118">O nome da classe de esquema de objeto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-118">The name of the object Schema class.</span></span>

<dt>

<span data-ttu-id="7f69e-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f69e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f69e-120">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f69e-120">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Class(
  [out] BSTR* pbstrClass
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7f69e-121">**GUID**</span><span class="sxs-lookup"><span data-stu-id="7f69e-121">**GUID**</span></span>
<span data-ttu-id="7f69e-122"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7f69e-122"></dt> <dd> <dl></span></span>

<span data-ttu-id="7f69e-123">O identificador global exclusivo do objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="7f69e-123">The globally unique identifier of the directory object.</span></span> <span data-ttu-id="7f69e-124">A interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) converte o **GUID** de uma cadeia de caracteres de octeto, como armazenado em um servidor de diretório, em um formato de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7f69e-124">The [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface converts the **GUID** from an octet string, as stored on a directory server, into a string format.</span></span>

<dt>

<span data-ttu-id="7f69e-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f69e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f69e-126">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f69e-126">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_GUID(
  [out] BSTR* pbstrGUID
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7f69e-127">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7f69e-127">**Name**</span></span>
<span data-ttu-id="7f69e-128"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7f69e-128"></dt> <dd> <dl></span></span>

<span data-ttu-id="7f69e-129">O nome relativo do objeto como nomeado no serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="7f69e-129">The relative name of the object as named within the underlying directory service.</span></span> <span data-ttu-id="7f69e-130">Esse nome distingue esse objeto de seus irmãos.</span><span class="sxs-lookup"><span data-stu-id="7f69e-130">This name distinguishes this object from its siblings.</span></span>

<dt>

<span data-ttu-id="7f69e-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f69e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f69e-132">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f69e-132">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] BSTR* pbstrName
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7f69e-133">**Pai**</span><span class="sxs-lookup"><span data-stu-id="7f69e-133">**Parent**</span></span>
<span data-ttu-id="7f69e-134"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7f69e-134"></dt> <dd> <dl></span></span>

<span data-ttu-id="7f69e-135">A cadeia de caracteres ADsPath do contêiner pai.</span><span class="sxs-lookup"><span data-stu-id="7f69e-135">The ADsPath string of the parent container.</span></span> <span data-ttu-id="7f69e-136">Active Directory não permite a formação do ADsPath de um determinado objeto concatenando as propriedades **pai** e **nome** .</span><span class="sxs-lookup"><span data-stu-id="7f69e-136">Active Directory does not permit the formation of the ADsPath of a given object by concatenating the **Parent** and **Name** properties.</span></span> <span data-ttu-id="7f69e-137">Embora essa operação possa funcionar em alguns provedores, não há garantia de que ele funcione para todas as implementações.</span><span class="sxs-lookup"><span data-stu-id="7f69e-137">While this operation might work in some providers, it is not guaranteed to work for all implementations.</span></span> <span data-ttu-id="7f69e-138">É garantido que o ADsPath seja válido e sempre deve ser usado para recuperar o ponteiro de interface de um objeto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-138">The ADsPath is guaranteed to be valid and should always be used to retrieve an object's interface pointer.</span></span>

<dt>

<span data-ttu-id="7f69e-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f69e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f69e-140">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f69e-140">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Parent(
  [out] BSTR* pbstrParent
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="7f69e-141">**Esquema**</span><span class="sxs-lookup"><span data-stu-id="7f69e-141">**Schema**</span></span>
<span data-ttu-id="7f69e-142"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="7f69e-142"></dt> <dd> <dl></span></span>

<span data-ttu-id="7f69e-143">A cadeia de caracteres ADsPath do objeto de classe de esquema deste objeto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-143">The ADsPath string of the Schema class object of this object.</span></span>

<dt>

<span data-ttu-id="7f69e-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7f69e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f69e-145">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="7f69e-145">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Schema(
  [out] BSTR* pbstrSchema
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a><span data-ttu-id="7f69e-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f69e-146">Remarks</span></span>

<span data-ttu-id="7f69e-147">Em Active Directory, o **GUID** RETORNADO de GUID é uma cadeia de caracteres hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="7f69e-147">In Active Directory, the **GUID** returned from GUID is a string of hexadecimals.</span></span> <span data-ttu-id="7f69e-148">Use o **GUID** resultante para associar diretamente ao objeto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-148">Use the resultant **GUID** to bind to the object directly.</span></span>


```VB
Dim x As IADs
Set x = GetObject("LDAP://servername/<GUID=xxx>")
```



<span data-ttu-id="7f69e-149">em que xxx é o valor retornado da propriedade GUID.</span><span class="sxs-lookup"><span data-stu-id="7f69e-149">where xxx is the value returned from the GUID property.</span></span> <span data-ttu-id="7f69e-150">Para obter mais informações, consulte [usando objectGUID para associar a um objeto](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span><span class="sxs-lookup"><span data-stu-id="7f69e-150">For more information, see [Using objectGUID to Bind to an Object](/windows/desktop/AD/using-objectguid-to-bind-to-an-object).</span></span> <span data-ttu-id="7f69e-151">Lembre-se de que, se você usar um GUID para associar a um objeto, o método de propriedade **ADsPath** retornará valores diferentes dos valores normais que seriam retornados se você usava um DN (nome distinto) para ligar ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="7f69e-151">Be aware that if you use a GUID to bind to an object, the **ADsPath** property method returns values that are different from the normal values that would be returned if you used a distinguished name (DN) to bind to the same object.</span></span> <span data-ttu-id="7f69e-152">Por exemplo, a tabela a seguir lista os valores retornados ao usar os dois métodos de associação diferentes para associar ao mesmo objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="7f69e-152">For example, the following table lists the values returned when using the two different binding methods to bind to the same user object.</span></span>



|             | <span data-ttu-id="7f69e-153">Associar usando DN</span><span class="sxs-lookup"><span data-stu-id="7f69e-153">Bind using DN</span></span>                                           | <span data-ttu-id="7f69e-154">Associar usando GUID</span><span class="sxs-lookup"><span data-stu-id="7f69e-154">Bind using GUID</span></span>                                             |
|-------------|---------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="7f69e-155">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7f69e-155">**Name**</span></span>    | <span data-ttu-id="7f69e-156">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="7f69e-156">CN=Jeff Smith</span></span>                                           | <span data-ttu-id="7f69e-157">CN = Jeff Smith</span><span class="sxs-lookup"><span data-stu-id="7f69e-157">CN=Jeff Smith</span></span>                                               |
| <span data-ttu-id="7f69e-158">**Pai**</span><span class="sxs-lookup"><span data-stu-id="7f69e-158">**Parent**</span></span>  | <span data-ttu-id="7f69e-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="7f69e-159">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>               | <span data-ttu-id="7f69e-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span><span class="sxs-lookup"><span data-stu-id="7f69e-160">LDAP://server/CN=Users,DC=Fabrikam,DC=com</span></span>                   |
| <span data-ttu-id="7f69e-161">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="7f69e-161">**ADsPath**</span></span> | <span data-ttu-id="7f69e-162">LDAP://server/CN=Jeff Smith, CN = Users, DC = Fabrikam, DC = com</span><span class="sxs-lookup"><span data-stu-id="7f69e-162">LDAP://server/CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=com</span></span> | <span data-ttu-id="7f69e-163">LDAP://server/<GUID = c0f59dfcf507d311a99e0000f879f7c7></span><span class="sxs-lookup"><span data-stu-id="7f69e-163">LDAP://server/<GUID=c0f59dfcf507d311a99e0000f879f7c7></span></span> |



 

> [!Note]  
> <span data-ttu-id="7f69e-164">O provedor WinNT não dá suporte à vinculação usando o **GUID** do objeto e retorna a propriedade **GUID** em um formato de cadeia de caracteres ligeiramente diferente.</span><span class="sxs-lookup"><span data-stu-id="7f69e-164">The WinNT provider does not support binding using the object **GUID**, and returns the **GUID** property in a slightly different string format.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7f69e-165">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f69e-165">Examples</span></span>

<span data-ttu-id="7f69e-166">O exemplo de código a seguir mostra como recuperar dados de objeto usando métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="7f69e-166">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
Dim x As IADs
Dim parent As IADsContainer
Dim cls As IADsClass
Dim op As Variant

On Error GoTo Cleanup

Set x = GetObject("WinNT://Fabrikam/Administrator")
Debug.Print "Object Name: " & x.Name
Debug.Print "Object Path: " & x.ADsPath
Debug.Print "Object Class: " & x.Class
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Debug.Print "Class Name is: " & cls.Name
For Each op In cls.OptionalProperties
    Debug.Print "Optional Property: " & op
Next op

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set x = Nothing
    Set parent = Nothing
    Set cls = Nothing
```



<span data-ttu-id="7f69e-167">O exemplo de código a seguir mostra como recuperar dados de objeto usando métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="7f69e-167">The following code example shows how to retrieve object data using property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```VB
<HTML>
<head><title></title></head>

<body>
<%
Dim x 
On Error Resume Next
 
Set x = GetObject("WinNT://Fabrikam/Administrator")
Response.Write "Object Name: " & x.Name & "<br>"
Response.Write "Object Path: " & x.ADsPath & "<br>"
Response.Write "Object Class: " & x.Class & "<br>"
 
' Get more data about the object schema.
Set cls = GetObject(x.Schema)
Response.Write "Class Name is: " & cls.Name & "<br>"
For Each op In cls.OptionalProperties
    Response.Write "Optional Property: " & op & "<br>"
Next op
%>

</body>
</html>
```



<span data-ttu-id="7f69e-168">O exemplo de código a seguir mostra como trabalhar com os métodos de propriedade da interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="7f69e-168">The following code example shows how to work with the property methods of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span>


```C++
#include <stdio.h>
#include <activeds.h>
 
int main(int argc, char* argv[])
{
    IADs *pADs = NULL;
    IADsUser *pADsUser = NULL;
    IADsClass *pCls = NULL;
    CComBSTR sbstr;
 
    HRESULT hr = CoInitialize(NULL);
    if (hr != S_OK) { return 0; }
 
    hr=ADsGetObject(L"WinNT://Fabrikam/Administrator",
                IID_IADsUser,
                (void**) &pADsUser);
    if (hr != S_OK) { goto Cleanup; }
 
    hr = pADsUser->QueryInterface(IID_IADs, (void**) &pADs);
    if( hr !=S_OK) { goto Cleanup;}
 
    pADsUser->Release();
 
    if( S_OK == pADs->get_Name(&sbstr) ) {
        printf("Object Name: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_ADsPath(&sbstr) ) {
        printf("Object path: %S\n",sbstr);
    }
 
    if( S_OK == pADs->get_Class(&sbstr) ) {
        printf("Object class: %S\n",sbstr);
    }
 
    hr = pADs->get_Schema(&sbstr);
    if ( hr != S_OK) {goto Cleanup;}
 
    hr = ADsGetObject(sbstr,IID_IADsClass, (void**)&pCls);
    if ( hr != S_OK) {goto Cleanup;}
    if( S_OK == pCls->get_Name(&sbstr) ) {
        printf("Class name is %S\n", sbstr);
    }
 
 Cleanup:
    if(pADs)
        pADs->Release();

    if(pIADsUser)
        pADsUser->Release();

    if(IADsClass)
        pADsClass->Release();

    CoUninitialize();

    if(hr==S_OK)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}
```



## <a name="requirements"></a><span data-ttu-id="7f69e-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f69e-169">Requirements</span></span>



| <span data-ttu-id="7f69e-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f69e-170">Requirement</span></span> | <span data-ttu-id="7f69e-171">Valor</span><span class="sxs-lookup"><span data-stu-id="7f69e-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f69e-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f69e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="7f69e-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f69e-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f69e-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f69e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="7f69e-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f69e-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f69e-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f69e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f69e-177"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f69e-177"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="7f69e-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7f69e-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f69e-179"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f69e-179"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="7f69e-180">IID</span><span class="sxs-lookup"><span data-stu-id="7f69e-180">IID</span></span><br/>                      | <span data-ttu-id="7f69e-181">IID \_ IADs é definido como FD8256D0-FD15-11CE-ABC4-02608C9E7553</span><span class="sxs-lookup"><span data-stu-id="7f69e-181">IID\_IADs is defined as FD8256D0-FD15-11CE-ABC4-02608C9E7553</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="7f69e-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f69e-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f69e-183">**IADs**</span><span class="sxs-lookup"><span data-stu-id="7f69e-183">**IADs**</span></span>](/windows/desktop/api/Iads/nn-iads-iads)
</dt> <dt>

[<span data-ttu-id="7f69e-184">**IADsContainer**</span><span class="sxs-lookup"><span data-stu-id="7f69e-184">**IADsContainer**</span></span>](/windows/desktop/api/Iads/nn-iads-iadscontainer)
</dt> </dl>

 

