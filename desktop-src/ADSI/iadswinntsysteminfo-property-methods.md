---
title: Métodos de propriedade IADsWinNTSystemInfo (IADs. h)
description: Os métodos de propriedade da interface IADsWinNTSystemInfo obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte interface Property Methods.
ms.assetid: 5ba36851-3d03-4179-8cee-dbebe24b7c4e
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propriedade IADsWinNTSystemInfo
topic_type:
- apiref
api_name:
- IADsWinNTSystemInfo Property Methods
- IADsWinNTSystemInfo.UserName
- IADsWinNTSystemInfo.get_UserName
- IADsWinNTSystemInfo.ComputerName
- IADsWinNTSystemInfo.get_ComputerName
- IADsWinNTSystemInfo.DomainName
- IADsWinNTSystemInfo.get_DomainName
- IADsWinNTSystemInfo.PDC
- IADsWinNTSystemInfo.get_PDC
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d647cf672032a4a06967ee034eb7b6430faf8dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755486"
---
# <a name="iadswinntsysteminfo-property-methods"></a><span data-ttu-id="c98da-105">Métodos de propriedade IADsWinNTSystemInfo</span><span class="sxs-lookup"><span data-stu-id="c98da-105">IADsWinNTSystemInfo Property Methods</span></span>

<span data-ttu-id="c98da-106">Os métodos de propriedade da interface [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) obtêm ou definem as propriedades descritas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c98da-106">The property methods of the [**IADsWinNTSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="c98da-107">Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c98da-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="c98da-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c98da-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="c98da-109">**ComputerName**</span><span class="sxs-lookup"><span data-stu-id="c98da-109">**ComputerName**</span></span>
<span data-ttu-id="c98da-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c98da-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="c98da-111">Nome do computador host onde o aplicativo está em execução.</span><span class="sxs-lookup"><span data-stu-id="c98da-111">Name of the host computer where the application is running.</span></span>

<dt>

<span data-ttu-id="c98da-112">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c98da-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98da-113">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c98da-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c98da-114">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c98da-114">**DomainName**</span></span>
<span data-ttu-id="c98da-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c98da-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="c98da-116">Nome do domínio ao qual o usuário pertence.</span><span class="sxs-lookup"><span data-stu-id="c98da-116">Name of the domain to which the user belongs.</span></span>

<dt>

<span data-ttu-id="c98da-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c98da-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98da-118">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c98da-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainName(
  [out] BSTR* pbstrDomain
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c98da-119">**PRIMÁRIO**</span><span class="sxs-lookup"><span data-stu-id="c98da-119">**PDC**</span></span>
<span data-ttu-id="c98da-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c98da-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="c98da-121">Nome do controlador de domínio primário ao qual o computador host pertence.</span><span class="sxs-lookup"><span data-stu-id="c98da-121">Name of the primary domain controller to which the host computer belongs.</span></span>

<dt>

<span data-ttu-id="c98da-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c98da-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98da-123">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c98da-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDC(
  [out] BSTR* pbstrPDC
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="c98da-124">**UserName**</span><span class="sxs-lookup"><span data-stu-id="c98da-124">**UserName**</span></span>
<span data-ttu-id="c98da-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="c98da-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="c98da-126">Nome da conta de usuário sob a qual o objeto **WinNTSystemInfo** é criado.</span><span class="sxs-lookup"><span data-stu-id="c98da-126">Name of the user account under which the **WinNTSystemInfo** object is created.</span></span>

<dt>

<span data-ttu-id="c98da-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c98da-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c98da-128">Tipo de dados de script: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c98da-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="c98da-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c98da-129">Examples</span></span>

<span data-ttu-id="c98da-130">O exemplo de código C/C++ a seguir recupera as informações do sistema WinNT.</span><span class="sxs-lookup"><span data-stu-id="c98da-130">The following C/C++ code example retrieves the WinNT system information.</span></span> <span data-ttu-id="c98da-131">Para brevidade, a verificação de erros é omitida.</span><span class="sxs-lookup"><span data-stu-id="c98da-131">For brevity, error checking is omitted.</span></span>


```C++
#include <activeds.h>
#include <stdio.h>
 
int main()
{
   HRESULT hr;
 
   hr = CoInitialize(NULL);
 
    IADsWinNTSystemInfo *pNtSys;
    hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsWinNTSystemInfo,
                          (void**)&pNTsys);
 
   BSTR bstr;
   hr = pNtSys->get_UserName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("User: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_ComputerName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Computer: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_DomainName(&bstr);
   if (SUCCEEDED(hr)) {
      printf("Domain: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   hr = pNtSys->get_PDC(&bstr);
   if (SUCCEEDED(hr)) {
      printf("PDC: %S\n", bstr);
      SysFreeString(bstr);
   }
 
   if(pNtSys) {
      pNtSys->Release();
   }
 
   CoUninitialize();
   return 0;
}
```



<span data-ttu-id="c98da-132">O exemplo de código a seguir Visual Basic recupera as informações do sistema WinNT.</span><span class="sxs-lookup"><span data-stu-id="c98da-132">The following Visual Basic code example retrieves the WinNT system information.</span></span>


```VB
Dim ntsys As New WinNTSystemInfo
Debug.print "User: " & ntsys.UserName
Debug.print "Computer: " & ntsys.ComputerName
Debug.print "Domain: " & ntsys.DomainName
Debug.print "PDC: " & ntsys.PDC
```



<span data-ttu-id="c98da-133">O exemplo de código de páginas Visual Basic Scripting Edition/Active Server a seguir recupera as informações do sistema WinNT.</span><span class="sxs-lookup"><span data-stu-id="c98da-133">The following Visual Basic Scripting Edition/Active Server Pages code example retrieves the WinNT system information.</span></span>


```VB
<%
Dim ntsys
Set ntsys = CreateObject("WinNTSystemInfo")
Response.Write "User: " & ntsys.UserName
Response.Write "Computer: " & ntsys.ComputerName
Response.Write "Domain: " & ntsys.DomainName
Response.Write "PDC: " & ntsys.PDC
%>
```



## <a name="requirements"></a><span data-ttu-id="c98da-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c98da-134">Requirements</span></span>



| <span data-ttu-id="c98da-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c98da-135">Requirement</span></span> | <span data-ttu-id="c98da-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c98da-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c98da-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c98da-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c98da-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c98da-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c98da-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c98da-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c98da-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c98da-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c98da-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c98da-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c98da-142"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="c98da-142"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="c98da-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c98da-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c98da-144"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c98da-144"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="c98da-145">IID</span><span class="sxs-lookup"><span data-stu-id="c98da-145">IID</span></span><br/>                      | <span data-ttu-id="c98da-146">IID \_ IADsWinNTSystemInfo é definido como 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span><span class="sxs-lookup"><span data-stu-id="c98da-146">IID\_IADsWinNTSystemInfo is defined as 6C6D65DC-AFD1-11D2-9CB9-0000F87A369E</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c98da-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="c98da-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98da-148">**IADsWinNTSystemInfo**</span><span class="sxs-lookup"><span data-stu-id="c98da-148">**IADsWinNTSystemInfo**</span></span>](/windows/desktop/api/Iads/nn-iads-iadswinntsysteminfo)
</dt> </dl>

 

 





