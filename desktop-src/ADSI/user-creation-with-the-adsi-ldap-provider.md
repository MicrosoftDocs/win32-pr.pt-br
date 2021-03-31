---
title: Criação de usuário com o provedor LDAP ADSI
description: Com o provedor de LDAP ADSI, você só pode criar uma conta de usuário global.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI do provedor LDAP, objeto de usuário, criação de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843bb5bc9d0696c3af7c5f06ce8c76123ae93c3a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104012064"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Criação de usuário com o provedor LDAP ADSI

Com o provedor de LDAP ADSI, você só pode criar uma conta de usuário global. As contas locais residem no banco de dados SAM e devem ser criadas usando o provedor WinNT. Para obter mais informações sobre como criar um objeto de usuário com o provedor WinNT, consulte [WinNT User Object](winnt-user-object.md).

**Para criar um objeto de usuário**

1.  Associe-se ao contêiner em que o objeto de usuário residirá e obtenha a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para o contêiner.
2.  Use o método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para criar o objeto de usuário.
3.  Os atributos mínimos necessários para criar um objeto de usuário dependerão do serviço de diretório usado. Para obter mais informações sobre como criar um usuário Active Directory, consulte [criando um usuário](/windows/desktop/AD/creating-a-user).
4.  Se a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) for usada, o novo objeto não será criado de fato até que o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.

    Se a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) for usada, o novo objeto será criado quando o método [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) for chamado. Os atributos mínimos, incluindo o [**objectClass**](/windows/desktop/ADSchema/a-objectclass), devem ser especificados na matriz de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) passada para o método **CreateDSObject** .

## <a name="example-1"></a>Exemplo 1

O exemplo de código a seguir cria uma conta de usuário com os atributos padrão.


```VB
Dim ou As IADs
Dim usr as IADsUser

On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Finance,DC=Fabrikam,DC=COM")
Set usr = ou.Create("user", "cn=Jeff Smith")
usr.Put "samAccountName", "jeffsmith"
usr.SetInfo

Cleanup:
   If (Err.Number <> 0) Then
      MsgBox ("An error has occurred. " &  Err.Number)
   End If
   Set ou = Nothing
   Set usr = Nothing
```



## <a name="example-2"></a>Exemplo 2

O exemplo de código a seguir cria uma conta de usuário com os atributos padrão. Para brevidade, a verificação de erros é omitida.


```C++
#include <activeds.h>

int main()
{
   HRESULT hr = CoInitialize(NULL);

   IADsContainer *pCont;
   IADsUser *pUser;

   LPWSTR adsPath = L"LDAP://serv1/CN=Users,dc=Fabrikam,dc=com";
   LPWSTR usrPass = NULL;
   LPWSTR usrName = NULL;

   // Add code to securely get the user name and password or leave
   // as NULL to use the current security context.

   hr = ADsOpenObject(adsPath, 
                      usrName,
                      usrPass,
                      ADS_SECURE_AUTHENTICATION,
                      IID_IADsContainer,
                      (void**)&pCont);

   IDispatch *pDisp;
   hr = pCont->Create(CComBSTR("user"), CComBSTR("cn=Jeff Smith"), &pDisp);
   pCont->Release();

   hr = pDisp->QueryInterface(IID_IADsUser,(void**)&pUser);
   pDisp->Release();

   VARIANT var;
   VariantInit(&var);
   V_BSTR(&var) = L"jeffsmith";
   V_VT(&var)=VT_BSTR;
   hr = pUser->Put(CComBSTR("samAccountName"), var);

   hr = pUser->SetInfo();

   VariantClear(&var);
   pUser->Release();

   CoUninitialize();

   return 0;
}
```



 

 