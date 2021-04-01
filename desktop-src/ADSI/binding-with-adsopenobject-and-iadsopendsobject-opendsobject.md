---
title: Associação com ADsOpenObject e IADsOpenDSObject OpenDSObject
description: A função ADsOpenObject e o método IADsOpenDSObject OpenDSObject são usados para associar a objetos de serviço de diretório quando credenciais alternativas devem ser especificadas e quando a criptografia de dados é necessária.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Associação com ADsOpenObject e IADsOpenDSObject OpenDSObject ADSI
- ADSI da ADSI, usando, associação com ADsOpenObject e IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008358"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a><span data-ttu-id="ac2c0-105">Associação com ADsOpenObject e IADsOpenDSObject:: OpenDSObject</span><span class="sxs-lookup"><span data-stu-id="ac2c0-105">Binding With ADsOpenObject and IADsOpenDSObject::OpenDSObject</span></span>

<span data-ttu-id="ac2c0-106">A função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) são usados para associar a objetos de serviço de diretório quando credenciais alternativas devem ser especificadas e quando a criptografia de dados é necessária.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-106">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method are used to bind to directory service objects when alternate credentials must be specified and when data encryption is required.</span></span>

<span data-ttu-id="ac2c0-107">As credenciais do thread de chamada devem ser usadas quando possível.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-107">The credentials of the calling thread should be used when possible.</span></span> <span data-ttu-id="ac2c0-108">No entanto, se credenciais alternativas precisarem ser usadas, a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-108">However, if alternate credentials must be used, the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function or the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method must be used.</span></span> <span data-ttu-id="ac2c0-109">Se forem usadas credenciais alternativas, será importante não armazenar a senha em cache.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-109">If alternate credentials are used, it is important to not cache the password.</span></span> <span data-ttu-id="ac2c0-110">Várias operações de ligação podem ser executadas especificando o nome de usuário e a senha para a primeira operação de ligação e, em seguida, especificando apenas o nome de usuário em associações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-110">Multiple bind operations can be performed by specifying the user name and password for the first bind operation and then specifying only the user name in subsequent binds.</span></span> <span data-ttu-id="ac2c0-111">O sistema configura uma sessão na primeira chamada e usa a mesma sessão em chamadas de ligação subsequentes, desde que as seguintes condições sejam atendidas:</span><span class="sxs-lookup"><span data-stu-id="ac2c0-111">The system sets up a session on the first call and uses the same session on subsequent bind calls as long as the following conditions are met:</span></span>

-   <span data-ttu-id="ac2c0-112">O mesmo nome de usuário em cada operação de ligação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-112">The same user name in each bind operation.</span></span>
-   <span data-ttu-id="ac2c0-113">Implemente a associação sem servidor ou associe-se ao mesmo servidor em cada operação de ligação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-113">Implement serverless binding or bind to the same server in each bind operation.</span></span>
-   <span data-ttu-id="ac2c0-114">Mantenha uma sessão aberta mantendo uma referência de objeto de uma das operações de ligação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-114">Maintain an open session by holding on to an object reference from one of the bind operations.</span></span> <span data-ttu-id="ac2c0-115">A sessão é fechada quando a última referência de objeto é liberada.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-115">The session is closed when the last object reference is released.</span></span>

<span data-ttu-id="ac2c0-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) usam as interfaces do [provedor de suporte de segurança (SSPI)](/windows/desktop/SecAuthN/sspi) do Windows NT para permitir a flexibilidade nas opções de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-116">[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) use the Windows NT [Security Support Provider Interfaces (SSPI)](/windows/desktop/SecAuthN/sspi) to allow flexibility in authentication options.</span></span> <span data-ttu-id="ac2c0-117">A principal vantagem de usar essas interfaces é fornecer tipos diferentes de autenticação para Active Directory clientes e para criptografar a sessão.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-117">The major advantage of using these interfaces is to provide different types of authentication to Active Directory clients and to encrypt the session.</span></span> <span data-ttu-id="ac2c0-118">Atualmente, a ADSI não permite que certificados sejam passados.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-118">Currently, ADSI does not allow certificates to be passed in.</span></span> <span data-ttu-id="ac2c0-119">Portanto, você pode usar SSL para criptografia e, em seguida, Kerberos, NTLM ou autenticação simples, dependendo de como os sinalizadores são definidos no parâmetro *dwReserved* .</span><span class="sxs-lookup"><span data-stu-id="ac2c0-119">Therefore, you can use SSL for encryption and then Kerberos, NTLM, or simple authentication, depending on how the flags are set on the *dwReserved* parameter.</span></span>

<span data-ttu-id="ac2c0-120">Você não pode solicitar um provedor SSPI específico em ADSI, embora sempre obtenha o protocolo de preferência mais alto.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-120">You cannot request a specific SSPI provider in ADSI, although you always get the highest preference protocol.</span></span> <span data-ttu-id="ac2c0-121">No caso de uma associação de cliente Windows a um computador que executa o Windows, o protocolo é Kerberos.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-121">In the case of a Windows client binding to a computer running Windows, the protocol is Kerberos.</span></span> <span data-ttu-id="ac2c0-122">Não permitir um certificado para autenticação é aceitável no caso de uma página da Web, pois a autenticação ocorre antes da execução da página da Web.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-122">Not allowing a certificate for authentication is acceptable in the case of a webpage because authentication occurs prior to running the webpage.</span></span>

<span data-ttu-id="ac2c0-123">Embora as operações abertas permitam que você especifique um usuário e uma senha, você não deve fazê-lo.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-123">Although Open operations allow you to specify a user and password, you should not do so.</span></span> <span data-ttu-id="ac2c0-124">Em vez disso, não especifique nenhuma credencial e use implicitamente as credenciais do contexto de segurança do chamador.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-124">Instead, do not specify any credentials and implicitly use the credentials of the caller's security context.</span></span> <span data-ttu-id="ac2c0-125">Para associar a um objeto de diretório usando as credenciais do chamador com [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), especifique **NULL** para o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-125">To bind to a directory object using the caller's credentials with [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) or [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), specify **NULL** for both user name and password.</span></span>

<span data-ttu-id="ac2c0-126">Por fim, para associar sem autenticação, use o sinalizador **anúncios \_ sem \_ autenticação** .</span><span class="sxs-lookup"><span data-stu-id="ac2c0-126">Finally, to bind with no authentication, use the **ADS\_NO\_AUTHENTICATION** flag.</span></span> <span data-ttu-id="ac2c0-127">Nenhuma autenticação indica que o ADSI tenta ligar como um usuário anônimo ao objeto de destino e não executa nenhuma autenticação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-127">No authentication indicates that ADSI attempts to bind as an anonymous user to the target object and performs no authentication.</span></span> <span data-ttu-id="ac2c0-128">Isso é equivalente a solicitar a associação anônima no LDAP e indica que todos os usuários estão incluídos no contexto de segurança.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-128">This is equivalent to requesting anonymous binding in LDAP and indicates that all users are included in the security context.</span></span>

<span data-ttu-id="ac2c0-129">Se os sinalizadores de autenticação estiverem definidos como zero, a ADSI executará uma associação simples, enviada como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-129">If the authentication flags are set to zero, ADSI performs a simple bind, sent as plaintext.</span></span>

> [!Caution]  
> <span data-ttu-id="ac2c0-130">Se um nome de usuário e senha forem especificados sem especificar sinalizadores de autenticação, o nome de usuário e a senha serão transmitidos pela rede em texto não criptografado, o que representa um risco de segurança.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-130">If a user name and password are specified without specifying authentication flags, the user name and password are transmitted over the network in plaintext, which is a security risk.</span></span> <span data-ttu-id="ac2c0-131">Não especifique um nome de usuário e uma senha sem especificar sinalizadores de autenticação.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-131">Do not specify a user name and password without specifying authentication flags.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ac2c0-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ac2c0-132">Examples</span></span>

<span data-ttu-id="ac2c0-133">O exemplo de código a seguir Visual Basic mostra como usar o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .</span><span class="sxs-lookup"><span data-stu-id="ac2c0-133">The following Visual Basic code example shows how to use the [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method.</span></span>


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



<span data-ttu-id="ac2c0-134">O exemplo de código C++ a seguir mostra como usar a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="ac2c0-134">The following C++ code example shows how to use the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



<span data-ttu-id="ac2c0-135">A interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) também pode ser usada em C++, mas ela duplica a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .</span><span class="sxs-lookup"><span data-stu-id="ac2c0-135">The [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface can also be used in C++, but it duplicates the [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function.</span></span>

<span data-ttu-id="ac2c0-136">O exemplo de código C++ a seguir mostra como usar a interface [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) para executar a mesma operação de associação que no exemplo de código acima.</span><span class="sxs-lookup"><span data-stu-id="ac2c0-136">The following C++ code example shows how to use the [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) interface to perform the same bind operation as in the code example above.</span></span>


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 