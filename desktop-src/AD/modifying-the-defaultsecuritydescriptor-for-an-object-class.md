---
title: Modificando o defaultSecurityDescriptor para uma classe de objeto
description: O exemplo de código a seguir recupera o descritor de segurança padrão para uma classe de objeto, adiciona uma ACE à DACL e, em seguida, define o descritor de segurança modificado na classe de objeto.
ms.assetid: 38b4d129-f98f-43da-9bd9-1ae23c090657
ms.tgt_platform: multiple
keywords:
- o AD descritores de segurança, modificando o defaultSecurityDescriptor para uma classe de objeto
- AD de objetos, modificando o defaultSecurityDescriptor para uma classe de objeto
- AD de classe, modificando o defaultSecurityDescriptor para uma classe de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0d837530454e8e563718d3f5974be22e5b7d42dfa5e29b8424a51c7a5c993d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186321"
---
# <a name="modifying-the-defaultsecuritydescriptor-for-an-object-class"></a>Modificando o defaultSecurityDescriptor para uma classe de objeto

O exemplo de código a seguir recupera o descritor de segurança padrão para uma classe de objeto, adiciona uma ACE à DACL e, em seguida, define o descritor de segurança modificado na classe de objeto.

lembre-se de que a modificação de esquema está desabilitada, por padrão, em todos os controladores de domínio Windows 2000. Para habilitar a modificação de esquema em um determinado DC, defina um \_ valor reg DWORD denominado "atualização de esquema permitido" na seguinte chave do registro:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Parâmetros** NTDS dos serviços do sistema de máquina local CurrentControlSet

Adicione esse valor se ele ainda não existir. Defina esse valor como 1 para habilitar a modificação do esquema. Se esse valor for zero, a modificação de esquema será desabilitada. O snap-in do MMC do Gerenciador de esquema fornece uma caixa de seleção que seleciona ou limpa essa chave do registro.


```C++
//  Add msvcrt.dll to your project
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include <ACLAPI.h>
#include <winnt.h>
#include <Sddl.h>
#include "atlbase.h"
#include "stdio.h"
#include "iads.h"
 
#define _WIN32_WINNT 0x0500
 
HRESULT ModifyDefaultSecurityDescriptor( IADs *pObject );

//  Entry point for the application.
int main(int argc, char *argv[])
{
LPOLESTR szPath = new OLECHAR[MAX_PATH];
LPOLESTR pszBuffer  = new WCHAR[MAX_PATH];
HRESULT hr = S_OK;
IADs *pObject = NULL;
VARIANT var;
 
wprintf(L"This program modifies the default security descriptor of an object class\n");
wprintf(L"Specify the object class:");
#ifdef _MBCS
_getws_s(pszBuffer);
if (!pszBuffer)
    return TRUE;
wcscpy_s(szPath,L"LDAP://cn=");
wcscat_s(szPath,pszBuffer);
wcscat_s(szPath,L",");
#endif _MBCS
 
//  Initialize COM.
CoInitialize(NULL);
 
//  Get rootDSE and the schema container DN. Bind to the
//  current user's domain using current user's security context.
 
hr = ADsOpenObject(L"LDAP://rootDSE",
            NULL,
            NULL,
            ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
            IID_IADs,
            (void**)&pObject);
 
if (SUCCEEDED(hr)) {
    hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
    if (SUCCEEDED(hr)) {
        #ifdef _MBCS
        wcscat_s(szPath,var.bstrVal);
        #endif _MBCS
        VariantClear(&var);
        if (pObject) {
            pObject->Release();
            pObject = NULL;
    }
    hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION, //  Use Secure Authentication.
               IID_IADs,
               (void**)&pObject);
    if (SUCCEEDED(hr)) {
        wprintf(L"Modify the default SD for the %s class\n", pszBuffer);
        hr = ModifyDefaultSecurityDescriptor( pObject );
    }
  }
}
 
if (FAILED(hr))
    wprintf(L"Failed with the following HRESULT: 0x%x\n", hr);
 
if (pObject)
    pObject->Release();
 
//  Uninitialize COM.
 
CoUninitialize();
return TRUE;
}    
 
 
HRESULT ModifyDefaultSecurityDescriptor(
                          IADs *pObject
                          )
{
HRESULT hr = E_FAIL;
VARIANT var;
PSECURITY_DESCRIPTOR pSDCNV = NULL;
SECURITY_DESCRIPTOR SD = {0};
DWORD dwSDSize = sizeof(SECURITY_DESCRIPTOR);
PSID pOwnerSID = NULL;
DWORD dwOwnerSIDSize = 0;
PSID pGroupSID = NULL;
DWORD dwGroupSIDSize = 0;
PACL pDACL = NULL;
DWORD dwDACLSize = 0;
PACL pSACL = NULL;
DWORD dwSACLSize = 0;
BOOL bDaclPresent = FALSE;
BOOL bDaclDefaulted = FALSE;
PACL pOldDACL, pNewDACL;
ULONG ulLen;
EXPLICIT_ACCESS ea;
DWORD dwRes;
 
//  Get the default security descriptor. Type should be VT_BSTR.
 
hr = pObject->Get(CComBSTR("defaultSecurityDescriptor"), &var);
if (FAILED(hr) || var.vt!=VT_BSTR ) {
    wprintf(L"Error getting default SD: 0x%x\n", hr );
    goto Cleanup;
}
 
wprintf(L"Old Default SD: %s\n", var.bstrVal);
 
//  Convert the security descriptor string to a security descriptor.
 
if ( ! ConvertStringSecurityDescriptorToSecurityDescriptor (
           var.bstrVal, SDDL_REVISION_1, &pSDCNV, NULL )) {
    wprintf(L"Error converting string security descriptor: %d\n", 
           GetLastError() );
    goto Cleanup;
}
 
//  Convert self-relative security descriptor to absolute.
//  First, get the required buffer sizes.
 
if (! MakeAbsoluteSD(pSDCNV, &SD, &dwSDSize, 
           pDACL, &dwDACLSize, 
           pSACL, &dwSACLSize, 
           pOwnerSID, &dwOwnerSIDSize, 
           pGroupSID, &dwGroupSIDSize) ) {
 
  //  Allocate the buffers.
 
  pDACL = (PACL) GlobalAlloc(GPTR, dwDACLSize);
  pSACL = (PACL) GlobalAlloc(GPTR, dwSACLSize);
  pOwnerSID = (PACL) GlobalAlloc(GPTR, dwOwnerSIDSize);
  pGroupSID = (PACL) GlobalAlloc(GPTR, dwGroupSIDSize);
  if (! (pDACL && pSACL && pOwnerSID && pGroupSID) ) {
    wprintf(L"GlobalAlloc failed: %d\n", GetLastError() );
    goto Cleanup;
  }
 
  //  Perform the conversion.
 
  if (! MakeAbsoluteSD(pSDCNV, &SD, &dwSDSize, pDACL, &dwDACLSize, 
           pSACL, &dwSACLSize, pOwnerSID, &dwOwnerSIDSize, 
           pGroupSID, &dwGroupSIDSize) ) {
    wprintf(L"MakeAbsoluteSD: %d\n", GetLastError() );
    goto Cleanup;
  }
}
 
//  Get the DACL from the security descriptor.
 
if (! GetSecurityDescriptorDacl(&SD, &bDaclPresent, 
                  &pOldDACL, &bDaclDefaulted) ) {
    wprintf(L"GetSecurityDescriptorDacl failed: %d\n", GetLastError() );
    goto Cleanup;
} 
 
//  Initialize an EXPLICIT_ACCESS structure for the new ACE.
//  The ACE grants Everyone the right to read properties.
 
ZeroMemory(&ea, sizeof(EXPLICIT_ACCESS));
ea.grfAccessPermissions = ADS_RIGHT_DS_READ_PROP;
ea.grfAccessMode = GRANT_ACCESS;
ea.grfInheritance= 0;
ea.Trustee.TrusteeForm = TRUSTEE_IS_NAME;
ea.Trustee.ptstrName = TEXT("Everyone");
 
//  Create a new ACL that merges the new ACE into the existing DACL.
 
dwRes = SetEntriesInAcl(1, &ea, pOldDACL, &pNewDACL);
if (ERROR_SUCCESS != dwRes)  {
    wprintf(L"SetEntriesInAcl Error %u\n", dwRes );
    goto Cleanup;
}
 
//  Put the modified DACL into the security descriptor.
 
if (! SetSecurityDescriptorDacl(&SD, TRUE, pNewDACL, FALSE) ) {
    wprintf(L"SetSecurityDescriptorOwner failed: %d\n", 
            GetLastError() );
    goto Cleanup;
} 
 
//  Convert the security descriptor back to string format.
 
VariantClear(&var);
if ( ! ConvertSecurityDescriptorToStringSecurityDescriptor (
        &SD, SDDL_REVISION_1, 
        GROUP_SECURITY_INFORMATION | OWNER_SECURITY_INFORMATION |
        DACL_SECURITY_INFORMATION | SACL_SECURITY_INFORMATION, 
        &var.bstrVal, &ulLen )) {
    wprintf(L"Error converting security descriptor to string: %d\n", 
        GetLastError() );
    goto Cleanup;
}
 
wprintf(L"New default SD: %s\n", var.bstrVal);
V_VT(&var) = VT_BSTR;
 
//  Use Put and SetInfo to set the modified security descriptor.
 
hr = pObject->Put(CComBSTR("defaultSecurityDescriptor"), var);
if (FAILED(hr)) {
    wprintf(L"Error putting default SD: 0x%x\n", hr );
    goto Cleanup;
}
 
hr = pObject->SetInfo();
if (FAILED(hr)) {
    wprintf(L"Error setting default SD: 0x%x\n", hr );
    goto Cleanup;
}
 
Cleanup:
 
VariantClear(&var);
if (pSDCNV) 
    LocalFree(pSDCNV);
if (pDACL) 
    GlobalFree(pDACL);
if (pSACL) 
    GlobalFree(pSACL);
if (pOwnerSID) 
    GlobalFree(pOwnerSID);
if (pGroupSID) 
    GlobalFree(pGroupSID);
if (pNewDACL) 
    LocalFree(pNewDACL);
 
return hr;
}
```



 

 




