---
title: Autenticação (ADSI)
description: No ADSI, as credenciais que consistem em um nome de usuário e senha são usadas para fornecer ou restringir o acesso a objetos no serviço de diretório.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- ADSI de autenticação
- ADSI, usando, autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104453854"
---
# <a name="authentication-adsi"></a><span data-ttu-id="0ef40-105">Autenticação (ADSI)</span><span class="sxs-lookup"><span data-stu-id="0ef40-105">Authentication (ADSI)</span></span>

<span data-ttu-id="0ef40-106">No ADSI, as credenciais que consistem em um nome de usuário e senha são usadas para fornecer ou restringir o acesso a objetos no serviço de diretório.</span><span class="sxs-lookup"><span data-stu-id="0ef40-106">In ADSI, credentials that consist of a user name and password are used to provide or restrict access to objects in the directory service.</span></span> <span data-ttu-id="0ef40-107">A função [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa as credenciais do thread de chamada para autenticação.</span><span class="sxs-lookup"><span data-stu-id="0ef40-107">The [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function uses the credentials of the calling thread for authentication.</span></span> <span data-ttu-id="0ef40-108">A função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) podem ser usados para especificar as credenciais que não sejam as do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="0ef40-108">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method can be used to specify credentials other than those of the calling thread.</span></span> <span data-ttu-id="0ef40-109">Quando um objeto está associado a um usuário autenticado, o usuário tem permissão para acessar o objeto com suporte dos requisitos de segurança do serviço de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="0ef40-109">When an object is bound to with an authenticated user, the user is allowed access to the object as supported by the underlying directory service security requirements.</span></span>

> [!Note]  
> <span data-ttu-id="0ef40-110">A função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) não devem ser usados para validar as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="0ef40-110">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method should not be used to validate user credentials.</span></span> <span data-ttu-id="0ef40-111">Para obter mais informações sobre como validar as credenciais do usuário, consulte o artigo 180548 da base de dados de conhecimento Microsoft, como [validar as credenciais do usuário em sistemas operacionais da Microsoft](https://support.microsoft.com/kb/180548).</span><span class="sxs-lookup"><span data-stu-id="0ef40-111">For more information about validating user credentials, see Microsoft Knowledge Base article 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).</span></span>

 

<span data-ttu-id="0ef40-112">O exemplo de código a seguir mostra como usar o método [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) para autenticar um usuário.</span><span class="sxs-lookup"><span data-stu-id="0ef40-112">The following code example shows how to use the [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method to authenticate a user.</span></span>


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




