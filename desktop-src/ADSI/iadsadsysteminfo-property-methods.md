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
# <a name="iadsadsysteminfo-property-methods"></a>Métodos de propriedade IADsADSystemInfo

Os métodos de propriedade da interface [**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo) obtêm ou definem as propriedades descritas na tabela a seguir. Para obter mais informações, consulte [interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Propriedades

<dl> <dt>

**ComputerName**
</dt> <dd> <dl>

Recupera o nome distinto do computador local.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ComputerName(
  [out] BSTR* pbstrComputer
);
```


</dt> </dl> </dd> <dt>

**DomainDNSName**
</dt> <dd> <dl>

Recupera o nome DNS do domínio do computador local, como "domainName.companyName.com".

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**DomainShortName**
</dt> <dd> <dl>

Recupera o nome curto do domínio do computador local, como "nome_do_domínio".

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DomainShortName(
  [out] BSTR* pbstrDSN
);
```


</dt> </dl> </dd> <dt>

**ForestDNSName**
</dt> <dd> <dl>

Recupera o nome DNS da floresta do computador local.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ForestDNSName(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**Isnativomode**
</dt> <dd> <dl>

Determina se o domínio do computador local está no modo nativo ou misto.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **bool**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsNativeMode(
  [out] BOOL* pvBool
);
```


</dt> </dl> </dd> <dt>

**PDCRoleOwner**
</dt> <dd> <dl>

Recupera o nome distinto do objeto DSA (agente de serviço de diretório) para o DC que possui a função de controlador de domínio primário no domínio do computador local.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PDCRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**SchemaRoleOwner**
</dt> <dd> <dl>

Recupera o nome distinto do objeto DSA (agente de serviço de diretório) para o controlador de domínio que possui a função de mestre de esquema na floresta do computador local.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SchemaRoleOwner(
  [out] BSTR* pbstr
);
```


</dt> </dl> </dd> <dt>

**SiteName**
</dt> <dd> <dl>

Recupera o nome do site do computador local.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_SiteName(
  [out] BSTR* pbstrSite
);
```


</dt> </dl> </dd> <dt>

**UserName**
</dt> <dd> <dl>

Recupera o Active Directory nome distinto do usuário atual, que é o usuário conectado ou o usuário representado pelo thread de chamada.

<dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Tipo de dados de script: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserName(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemplos

O exemplo de código C++ a seguir recupera as informações do sistema do Windows. Para brevidade, a verificação de erros é omitida.


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



O exemplo de código a seguir Visual Basic recupera as informações do sistema do Windows.


```VB
Dim sys As New ADSystemInfo
Debug.print "User: " & sys.UserName
Debug.print "Computer: " & sys.ComputerName
Debug.print "Domain: " & sys.DomainDNSName
Debug.print "PDC Role Owner: " & sys.PDCRoleOwner
```



O exemplo de código VBScript/ASP a seguir recupera as informações do sistema do Windows.


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsADSystemInfo é definido como 5BB11929-AFD1-11D2-9CB9-0000F87A369E<br/>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IADsADSystemInfo**](/windows/desktop/api/Iads/nn-iads-iadsadsysteminfo)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

