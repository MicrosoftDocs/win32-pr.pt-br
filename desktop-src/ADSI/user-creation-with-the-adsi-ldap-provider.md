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
# <a name="user-creation-with-the-adsi-ldap-provider"></a><span data-ttu-id="9fe9c-104">Criação de usuário com o provedor LDAP ADSI</span><span class="sxs-lookup"><span data-stu-id="9fe9c-104">User Creation with the ADSI LDAP Provider</span></span>

<span data-ttu-id="9fe9c-105">Com o provedor de LDAP ADSI, você só pode criar uma conta de usuário global.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-105">With the ADSI LDAP provider, you can only create a global user account.</span></span> <span data-ttu-id="9fe9c-106">As contas locais residem no banco de dados SAM e devem ser criadas usando o provedor WinNT.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-106">Local accounts reside in the SAM database and must be created using the WinNT provider.</span></span> <span data-ttu-id="9fe9c-107">Para obter mais informações sobre como criar um objeto de usuário com o provedor WinNT, consulte [WinNT User Object](winnt-user-object.md).</span><span class="sxs-lookup"><span data-stu-id="9fe9c-107">For more information about creating a user object with the WinNT provider, see [WinNT User Object](winnt-user-object.md).</span></span>

<span data-ttu-id="9fe9c-108">**Para criar um objeto de usuário**</span><span class="sxs-lookup"><span data-stu-id="9fe9c-108">**To create a user object**</span></span>

1.  <span data-ttu-id="9fe9c-109">Associe-se ao contêiner em que o objeto de usuário residirá e obtenha a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) ou [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para o contêiner.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-109">Bind to the container where the user object will reside and obtain either the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) or [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface for the container.</span></span>
2.  <span data-ttu-id="9fe9c-110">Use o método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) ou [**IDirectoryObject:: CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para criar o objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-110">Use the [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) or [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method to create the user object.</span></span>
3.  <span data-ttu-id="9fe9c-111">Os atributos mínimos necessários para criar um objeto de usuário dependerão do serviço de diretório usado.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-111">The minimum attributes required to create a user object will depend on the directory service used.</span></span> <span data-ttu-id="9fe9c-112">Para obter mais informações sobre como criar um usuário Active Directory, consulte [criando um usuário](/windows/desktop/AD/creating-a-user).</span><span class="sxs-lookup"><span data-stu-id="9fe9c-112">For more information about creating an Active Directory user, see [Creating a User](/windows/desktop/AD/creating-a-user).</span></span>
4.  <span data-ttu-id="9fe9c-113">Se a interface [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) for usada, o novo objeto não será criado de fato até que o método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-113">If the [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) interface is used, the new object is not actually created until the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span>

    <span data-ttu-id="9fe9c-114">Se a interface [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) for usada, o novo objeto será criado quando o método [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) for chamado.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-114">If the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface is used, the new object is created when the [**CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) method is called.</span></span> <span data-ttu-id="9fe9c-115">Os atributos mínimos, incluindo o [**objectClass**](/windows/desktop/ADSchema/a-objectclass), devem ser especificados na matriz de [**\_ \_ informações attr do ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) passada para o método **CreateDSObject** .</span><span class="sxs-lookup"><span data-stu-id="9fe9c-115">The minimum attributes, including the [**objectClass**](/windows/desktop/ADSchema/a-objectclass), must be specified in the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) array passed to the **CreateDSObject** method.</span></span>

## <a name="example-1"></a><span data-ttu-id="9fe9c-116">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fe9c-116">Example 1</span></span>

<span data-ttu-id="9fe9c-117">O exemplo de código a seguir cria uma conta de usuário com os atributos padrão.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-117">The following code example creates a user account with the default attributes.</span></span>


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



## <a name="example-2"></a><span data-ttu-id="9fe9c-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9fe9c-118">Example 2</span></span>

<span data-ttu-id="9fe9c-119">O exemplo de código a seguir cria uma conta de usuário com os atributos padrão.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-119">The following code example creates a user account with the default attributes.</span></span> <span data-ttu-id="9fe9c-120">Para brevidade, a verificação de erros é omitida.</span><span class="sxs-lookup"><span data-stu-id="9fe9c-120">For brevity, error checking is omitted.</span></span>


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



 

 