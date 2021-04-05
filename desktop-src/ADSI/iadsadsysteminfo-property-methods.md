---
title: Métodos de propriedade IADsADSystemInfo (IADs. h)
description: Os métodos de propriedade da interface IADsADSystemInfo obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 1cdaa610-4341-4825-b2f9-dd495a9147ff
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsADSystemInfo
topic_type:
- apiref
api_name:
- IADsADSystemInfo Property Methods
- IADsADSystemInfo.UserName
- IADsADSystemInfo.get_UserName
- IADsADSystemInfo.ComputerName
- IADsADSystemInfo.get_ComputerName
- IADsADSystemInfo.SiteName
- IADsADSystemInfo.get_SiteName
- IADsADSystemInfo.DomainShortName
- IADsADSystemInfo.get_DomainShortName
- IADsADSystemInfo.DomainDNSName
- IADsADSystemInfo.get_DomainDNSName
- IADsADSystemInfo.ForestDNSName
- IADsADSystemInfo.get_ForestDNSName
- IADsADSystemInfo.PDCRoleOwner
- IADsADSystemInfo.get_PDCRoleOwner
- IADsADSystemInfo.SchemaRoleOwner
- IADsADSystemInfo.get_SchemaRoleOwner
- IADsADSystemInfo.IsNativeMode
- IADsADSystemInfo.get_IsNativeMode
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8dba53dfda4bb8f4dd3290cb2737cdeb4e8a6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086051"
---
# <a name="iadsadsysteminfo-property-methods"></a><span data-ttu-id="41ba8-105">Métodos de propriedade IADsADSystemInfo</span><span class="sxs-lookup"><span data-stu-id="41ba8-105">IADsADSystemInfo Property Methods</span></span>

<span data-ttu-id="41ba8-106">Os métodos de propriedade da interface [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="41ba8-106">The property methods of the [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="41ba8-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="41ba8-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="41ba8-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="41ba8-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="41ba8-109">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="41ba8-109">**ComputerName**</span></span>
<span data-ttu-id="41ba8-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-111">Recupera o nome distinto do computador local.</span><span class="sxs-lookup"><span data-stu-id="41ba8-111">Retrieves the distinguished name of the local computer.</span></span>

<dt>

<span data-ttu-id="41ba8-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-114">**DomainDNSName**</span><span class="sxs-lookup"><span data-stu-id="41ba8-114">**DomainDNSName**</span></span>
<span data-ttu-id="41ba8-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-116">Recupera o nome DNS do domínio do computador local, como "domainName.companyName.com".</span><span class="sxs-lookup"><span data-stu-id="41ba8-116">Retrieves the DNS name of the local computer's domain, such as "domainName.companyName.com".</span></span>

<dt>

<span data-ttu-id="41ba8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-119">**DomainShortName**</span><span class="sxs-lookup"><span data-stu-id="41ba8-119">**DomainShortName**</span></span>
<span data-ttu-id="41ba8-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-121">Recupera o nome curto do domínio do computador local, como "nome_do_domínio".</span><span class="sxs-lookup"><span data-stu-id="41ba8-121">Retrieves the short name of the local computer's domain, such as "domainName".</span></span>

<dt>

<span data-ttu-id="41ba8-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-124">**ForestDNSName**</span><span class="sxs-lookup"><span data-stu-id="41ba8-124">**ForestDNSName**</span></span>
<span data-ttu-id="41ba8-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-126">Recupera o nome DNS da floresta do computador local.</span><span class="sxs-lookup"><span data-stu-id="41ba8-126">Retrieves the DNS name of the local computer's forest.</span></span>

<dt>

<span data-ttu-id="41ba8-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-129">**Isnativomode**</span><span class="sxs-lookup"><span data-stu-id="41ba8-129">**IsNativeMode**</span></span>
<span data-ttu-id="41ba8-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-131">Determina se o domínio do computador local está no modo nativo ou misto.</span><span class="sxs-lookup"><span data-stu-id="41ba8-131">Determines whether the local computer's domain is in native or mixed mode.</span></span>

<dt>

<span data-ttu-id="41ba8-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-133">Tipo de dados de script: **bool**</span><span class="sxs-lookup"><span data-stu-id="41ba8-133">Scripting data type: **BOOL**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-134">**PDCRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="41ba8-134">**PDCRoleOwner**</span></span>
<span data-ttu-id="41ba8-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-136">Recupera o nome distinto do objeto DSA (agente de serviço de diretório) para o DC que possui a função de controlador de domínio primário no domínio do computador local.</span><span class="sxs-lookup"><span data-stu-id="41ba8-136">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the primary domain controller role in the local computer's domain.</span></span>

<dt>

<span data-ttu-id="41ba8-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-138">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-138">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-139">**SchemaRoleOwner**</span><span class="sxs-lookup"><span data-stu-id="41ba8-139">**SchemaRoleOwner**</span></span>
<span data-ttu-id="41ba8-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-141">Recupera o nome distinto do objeto DSA (agente de serviço de diretório) para o controlador de domínio que possui a função de mestre de esquema na floresta do computador local.</span><span class="sxs-lookup"><span data-stu-id="41ba8-141">Retrieves the distinguished name of the directory service agent (DSA) object for the DC that owns the schema master role in the local computer's forest.</span></span>

<dt>

<span data-ttu-id="41ba8-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-143">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-143">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-144">**SiteName**</span><span class="sxs-lookup"><span data-stu-id="41ba8-144">**SiteName**</span></span>
<span data-ttu-id="41ba8-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-146">Recupera o nome do site do computador local.</span><span class="sxs-lookup"><span data-stu-id="41ba8-146">Retrieves the site name of the local computer.</span></span>

<dt>

<span data-ttu-id="41ba8-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-148">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-148">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="41ba8-149">**UserName**</span><span class="sxs-lookup"><span data-stu-id="41ba8-149">**UserName**</span></span>
<span data-ttu-id="41ba8-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="41ba8-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="41ba8-151">Recupera o Active Directory nome distinto do usuário atual, que é o usuário conectado ou o usuário representado pelo thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="41ba8-151">Retrieves the Active Directory distinguished name of the current user, which is the logged-on user or the user impersonated by the calling thread.</span></span>

<dt>

<span data-ttu-id="41ba8-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="41ba8-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41ba8-153">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="41ba8-153">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="41ba8-154">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41ba8-154">Examples</span></span>

<span data-ttu-id="41ba8-155">O exemplo de código C++ a seguir recupera as informações do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="41ba8-155">The following C++ code example retrieves the Windows system information.</span></span> <span data-ttu-id="41ba8-156">Para brevidade, a verificação de erros é omitida.</span><span class="sxs-lookup"><span data-stu-id="41ba8-156">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsADSystemInfo *pSys;
    hr = CoCreateInstance(CLSID_ADSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsADSystemInfo,
                          (void**)&pSys);
 
   BSTR bstr;
   hr = pSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_DomainDNSName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pSys->get_PDCRoleOwner(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC Role owner: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pSys) {
      pSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="41ba8-157">O exemplo de código a seguir Visual Basic recupera as informações do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="41ba8-157">The following Visual Basic code example retrieves the Windows system information.</span></span>


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



<span data-ttu-id="41ba8-158">O exemplo de código VBScript/ASP a seguir recupera as informações do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="41ba8-158">The following VBScript/ASP code example retrieves the Windows system information.</span></span>


```VB
<%
Dim sys
Set sys = CreateObject("ADSystemInfo")
Response.Write "User: " & sys.UserName
Response.Write "Computer: " & sys.ComputerName
Response.Write "Domain: " & sys.DomainDNSName
Response.Write "PDC Role Owner: " & sys.PDCRoleOwner
%>
```



## <a name="requirements"></a><span data-ttu-id="41ba8-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41ba8-159">Requirements</span></span>



| <span data-ttu-id="41ba8-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="41ba8-160">Requirement</span></span> | <span data-ttu-id="41ba8-161">Valor</span><span class="sxs-lookup"><span data-stu-id="41ba8-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41ba8-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ba8-162">Minimum supported client</span></span><br/> | <span data-ttu-id="41ba8-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41ba8-163">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41ba8-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="41ba8-164">Minimum supported server</span></span><br/> | <span data-ttu-id="41ba8-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41ba8-165">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41ba8-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41ba8-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="41ba8-167"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="41ba8-167"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="41ba8-168">DLL</span><span class="sxs-lookup"><span data-stu-id="41ba8-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41ba8-169"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41ba8-169"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="41ba8-170">IID</span><span class="sxs-lookup"><span data-stu-id="41ba8-170">IID</span></span><br/>                      | <span data-ttu-id="41ba8-171">IID \_ IADsADSystemInfo é definido como 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="41ba8-171">IID\_IADsADSystemInfo is defined as 5BB11929-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>     |



## <a name="see-also"></a><span data-ttu-id="41ba8-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="41ba8-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41ba8-173">**IADsADSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="41ba8-173">**IADsADSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[<span data-ttu-id="41ba8-174">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="41ba8-174">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

