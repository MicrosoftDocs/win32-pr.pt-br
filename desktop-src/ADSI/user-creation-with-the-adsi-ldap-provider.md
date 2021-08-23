---
title: Criação de usuário com o provedor LDAP ADSI
description: Com o provedor ADSI LDAP, você só pode criar uma conta de usuário global.
ms.assetid: f99f85a8-9ced-4006-b95b-bd5671ba4c60
ms.tgt_platform: multiple
keywords:
- ADSI do provedor LDAP, objeto de usuário, Criação de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32d076805b9480ed0344712f7b023efab4ef0a025f367cc9c5ebb0bb7dfc0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023064"
---
# <a name="user-creation-with-the-adsi-ldap-provider"></a>Criação de usuário com o provedor LDAP ADSI

Com o provedor ADSI LDAP, você só pode criar uma conta de usuário global. As contas locais residem no banco de dados SAM e devem ser criadas usando o provedor WinNT. Para obter mais informações sobre como criar um objeto de usuário com o provedor WinNT, consulte [Objeto de usuário do WinNT.](winnt-user-object.md)

**Para criar um objeto de usuário**

1.  A bind ao contêiner em que o objeto de usuário residirá e obterá a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**ou IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para o contêiner.
2.  Use o [**método IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para criar o objeto de usuário.
3.  Os atributos mínimos necessários para criar um objeto de usuário dependerão do serviço de diretório usado. Para obter mais informações sobre como criar um usuário do Active Directory, consulte [Criando um usuário.](/windows/desktop/AD/creating-a-user)
4.  Se a [**interface IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) for usada, o novo objeto não será realmente criado até que o [**método IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.

    Se a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) for usada, o novo objeto será criado quando [**o método CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) for chamado. Os atributos mínimos, incluindo [**objectClass**](/windows/desktop/ADSchema/a-objectclass), devem ser especificados na matriz [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) passada para o **método CreateDSObject.**

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

O exemplo de código a seguir cria uma conta de usuário com os atributos padrão. Para a brevidade, a verificação de erros é omitida.


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



 

 