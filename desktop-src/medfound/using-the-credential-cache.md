---
description: Usando o cache de credenciais
ms.assetid: b58d0a6e-ecae-48a1-a3af-d4246caa272b
title: Usando o cache de credenciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d512d0bab8f45f50a587e3c8eda2a73c4832685f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790415"
---
# <a name="using-the-credential-cache"></a><span data-ttu-id="438f0-103">Usando o cache de credenciais</span><span class="sxs-lookup"><span data-stu-id="438f0-103">Using the Credential Cache</span></span>

<span data-ttu-id="438f0-104">Media Foundation fornece uma implementação padrão da interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="438f0-104">Media Foundation provides a default implementation of the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface.</span></span> <span data-ttu-id="438f0-105">Um aplicativo que implementa a interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) pode usar o objeto de cache de credencial padrão para armazenar as credenciais do usuário.</span><span class="sxs-lookup"><span data-stu-id="438f0-105">An application that implements the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface can use the default credential cache object to store the user's credentials.</span></span>

<span data-ttu-id="438f0-106">Para criar o objeto de cache de credencial padrão, chame a função [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) .</span><span class="sxs-lookup"><span data-stu-id="438f0-106">To create the default credential cache object, call the [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) function.</span></span>


```C++
HRESULT hr = S_OK;
IMFNetCredentialCache *pCredentialCache = NULL;
hr = MFCreateCredentialCache(&pCredentialCache);
```



<span data-ttu-id="438f0-107">Depois que o cache de credenciais é criado, o aplicativo pode usar os métodos a seguir para obter um objeto de credencial, definir as credenciais do usuário e especificar as opções de cache.</span><span class="sxs-lookup"><span data-stu-id="438f0-107">After the credential cache is created, the application can use the following methods to get a credential object, set user credentials, and specify the caching options.</span></span>

-   <span data-ttu-id="438f0-108">Para obter o objeto de credencial para uma URL, chame [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="438f0-108">To get the credential object for a URL, call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span>

    ```C++
    hr = pCredentialCache-> GetCredential(
            pszUrl,
            pszRealm,
            dwAuthenticationFlags,
            &pCredential,
            &dwRequirementsFlags);
    ```

    

    <span data-ttu-id="438f0-109">Se as credenciais para a URL especificada não existirem no cache de credenciais, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) criará um novo objeto de credencial com valores de senha e nome de usuário vazios.</span><span class="sxs-lookup"><span data-stu-id="438f0-109">If the credentials for the specified URL do not exist in the credential cache, [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) creates a new credential object with empty user name and password values.</span></span>

-   <span data-ttu-id="438f0-110">Para definir o nome de usuário e a senha no objeto Credential, chame [**IMFNetCredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span><span class="sxs-lookup"><span data-stu-id="438f0-110">To set the user name and password on the credential object, call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword).</span></span>
-   <span data-ttu-id="438f0-111">Para definir as opções de cache no objeto Credential, chame [**IMFNetCredentialCache:: Setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span><span class="sxs-lookup"><span data-stu-id="438f0-111">To set the caching options on the credential object, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions).</span></span>

    ```C++
    hr = pCredentialCache-> SetUserOptions( 
            pCredentialCache,
            MFNET_CREDENTIAL_SAVE);
    ```

    

    <span data-ttu-id="438f0-112">Os valores de parâmetro *dwOptionsFlags* são definidos na enumeração [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) .</span><span class="sxs-lookup"><span data-stu-id="438f0-112">The *dwOptionsFlags* parameter values are defined in the [**MFNetCredentialOptions**](/windows/desktop/api/mfidl/ne-mfidl-mfnetcredentialoptions) enumeration.</span></span> <span data-ttu-id="438f0-113">Para salvar as credenciais do usuário de uma URL em um armazenamento persistente, defina o \_ sinalizador de salvamento da credencial MFNET \_ .</span><span class="sxs-lookup"><span data-stu-id="438f0-113">To save user credentials for a URL in a persistent storage, set the MFNET\_CREDENTIAL\_SAVE flag.</span></span> <span data-ttu-id="438f0-114">Se a chamada [**Setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) for concluída com êxito, a chamada subsequente para [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) pesquisará as credenciais no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="438f0-114">If the [**SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) call completes successfully, then the subsequent call to [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) searches for the credentials in the persistent storage.</span></span> <span data-ttu-id="438f0-115">Se uma correspondência for encontrada, esse método retornará um ponteiro para o objeto de credencial que contém as informações.</span><span class="sxs-lookup"><span data-stu-id="438f0-115">If a match is found, this method returns a pointer to the credential object that contains the information.</span></span>

    <span data-ttu-id="438f0-116">Por padrão, as credenciais de usuário enviadas pela rede são criptografadas.</span><span class="sxs-lookup"><span data-stu-id="438f0-116">By default, user credentials sent over the network are encrypted.</span></span> <span data-ttu-id="438f0-117">Para alterar isso para texto não criptografado, defina o sinalizador de MFNET \_ credencial \_ permitir \_ texto não criptografado \_ .</span><span class="sxs-lookup"><span data-stu-id="438f0-117">To change this to clear text, set the MFNET\_CREDENTIAL\_ALLOW\_CLEAR\_TEXT flag.</span></span>

    <span data-ttu-id="438f0-118">Para remover informações do registro, chame [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) para obter o objeto de credencial e, em seguida, chame [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) e defina *dwOptionsFlags* para MFNET \_ Credential não \_ \_ cache.</span><span class="sxs-lookup"><span data-stu-id="438f0-118">To remove information from the registry, call [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) to get the credential object, and then call [**SetUserOption**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) and set *dwOptionsFlags* to MFNET\_CREDENTIAL\_DONT\_CACHE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="438f0-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="438f0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="438f0-120">Autenticação de origem da rede</span><span class="sxs-lookup"><span data-stu-id="438f0-120">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



