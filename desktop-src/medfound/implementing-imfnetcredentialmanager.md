---
description: Implementando IMFNetCredentialManager
ms.assetid: 3eb2afec-195c-4d8d-8e08-7e6ec7c572f8
title: Implementando IMFNetCredentialManager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c026f2c12b2ff248032a56d9c48a0e0e1576c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785149"
---
# <a name="implementing-imfnetcredentialmanager"></a><span data-ttu-id="3f4c4-103">Implementando IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="3f4c4-103">Implementing IMFNetCredentialManager</span></span>

<span data-ttu-id="3f4c4-104">No método [**IMFNetCredentialManager:: BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) , faça o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-104">In the [**IMFNetCredentialManager::BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method, do the following.</span></span>

1.  <span data-ttu-id="3f4c4-105">Se você ainda não tiver um ponteiro [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , chame [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) para criar o objeto de cache de credencial.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-105">If you do not have an [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) pointer already, call [**MFCreateCredentialCache**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatecredentialcache) to create the credential cache object.</span></span> <span data-ttu-id="3f4c4-106">Armazene esse ponteiro.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-106">Store this pointer.</span></span>
2.  <span data-ttu-id="3f4c4-107">Chame [**IMFNetCredentialCache:: GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span><span class="sxs-lookup"><span data-stu-id="3f4c4-107">Call [**IMFNetCredentialCache::GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential).</span></span> <span data-ttu-id="3f4c4-108">Defina os sinalizadores no parâmetro *dwAuthenticationFlags* da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3f4c4-108">Set the flags in the *dwAuthenticationFlags* parameter as follows:</span></span>
    -   <span data-ttu-id="3f4c4-109">Se o membro **hrOp** da estrutura [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) for igual a **ns \_ E \_ \_ ACCESSDENIED de proxy**, defina o sinalizador de **\_ \_ proxy de autenticação MFNET** .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-109">If the **hrOp** member of the [**MFNetCredentialManagerGetParam**](/windows/desktop/api/mfidl/ns-mfidl-mfnetcredentialmanagergetparam) structure equals **NS\_E\_PROXY\_ACCESSDENIED**, set the **MFNET\_AUTHENTICATION\_PROXY** flag.</span></span>
    -   <span data-ttu-id="3f4c4-110">Se **fClearTextPackage** for **true**, defina o sinalizador de **\_ \_ \_ texto não criptografado de autenticação MFNET** .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-110">If **fClearTextPackage** is **TRUE**, set the **MFNET\_AUTHENTICATION\_CLEAR\_TEXT** flag.</span></span>
    -   <span data-ttu-id="3f4c4-111">Se **fAllowLoggedOnUser** for **true**, defina o sinalizador **autenticação do MFNET \_ \_ registrado \_ no \_ usuário** .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-111">If **fAllowLoggedOnUser** is **TRUE**, set the **MFNET\_AUTHENTICATION\_LOGGED\_ON\_USER** flag.</span></span>
3.  <span data-ttu-id="3f4c4-112">O método [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) retorna um ponteiro [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) e, possivelmente, o sinalizador requerer \_ prompt.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-112">The [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) method returns an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer and possibly the REQUIRE\_PROMPT flag.</span></span> <span data-ttu-id="3f4c4-113">Armazene o ponteiro **IMFNetCredential** .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-113">Store the **IMFNetCredential** pointer.</span></span>
4.  <span data-ttu-id="3f4c4-114">Se [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) não retornar o sinalizador **exigir \_ aviso** , você estará pronto.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-114">If [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) does not return the **REQUIRE\_PROMPT** flag, you are done.</span></span> <span data-ttu-id="3f4c4-115">Pule para a etapa 9.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-115">Skip to step 9.</span></span>
5.  <span data-ttu-id="3f4c4-116">Caso contrário, se [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) retornar o sinalizador de **\_ solicitação require** , você deverá solicitar ao usuário seu nome de usuário e senha.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-116">Otherwise, if [**GetCredential**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential) returns the **REQUIRE\_PROMPT** flag, you must prompt the user for his or her user name and password.</span></span>
6.  <span data-ttu-id="3f4c4-117">Se **fClearTextPackage** for **false**, criptografe as credenciais.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-117">If **fClearTextPackage** is **FALSE**, encrypt the credentials.</span></span>
7.  <span data-ttu-id="3f4c4-118">Chame [**IMFNetCredential:: SETUSER**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) e [**IMFNetCredential:: SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) para definir o nome do usuário e a senha no objeto de credenciais.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-118">Call [**IMFNetCredential::SetUser**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setuser) and [**IMFNetCredential::SetPassword**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredential-setpassword) to set the user's name and password on the credentials object.</span></span>
8.  <span data-ttu-id="3f4c4-119">Opcionalmente, chame [**IMFNetCredentialCache:: Setuseroptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) para atualizar o objeto de cache de credencial com as preferências do usuário para armazenar e enviar credenciais.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-119">Optionally, call [**IMFNetCredentialCache::SetUserOptions**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions) to update the credential cache object with the user's preferences for storing and sending credentials.</span></span>
9.  <span data-ttu-id="3f4c4-120">Invoque o retorno de chamada [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) chamando [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span><span class="sxs-lookup"><span data-stu-id="3f4c4-120">Invoke the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) callback by calling [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).</span></span>

<span data-ttu-id="3f4c4-121">No método [**IMFNetCredentialManager:: EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) , retorna o ponteiro [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) obtido no método [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-121">In the [**IMFNetCredentialManager::EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method, return the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer obtained in the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method.</span></span>

<span data-ttu-id="3f4c4-122">No método [**IMFNetCredentialManager:: setbom**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) , passe os parâmetros de entrada diretamente para o método [**IMFNetCredentialCache:: setbom**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-122">In the [**IMFNetCredentialManager::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-setgood) method, pass the input parameters directly to the [**IMFNetCredentialCache::SetGood**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setgood) method.</span></span> <span data-ttu-id="3f4c4-123">Isso notifica o cache de credenciais se as credenciais foram aceitas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-123">This notifies the credential cache whether the credentials were accepted by the server.</span></span>

<span data-ttu-id="3f4c4-124">Se você precisar solicitar o usuário (etapa 5) ou criptografar as credenciais (etapa 6), faça isso em um thread de fila de trabalho, para que você não bloqueie o pipeline de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-124">If you need to prompt the user (step 5) or encrypt the credentials (step 6), you should do so on a work-queue thread, so that you do not block the Microsoft Media Foundation pipeline.</span></span> <span data-ttu-id="3f4c4-125">Chame [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) e execute as etapas restantes dentro do retorno de chamada da fila de trabalho.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-125">Call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) and then perform the remaining steps inside the work-queue callback.</span></span>

> [!Note]  
> <span data-ttu-id="3f4c4-126">Lembre-se de que [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) pode ser invocado enquanto a fonte de rede está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-126">Be aware that [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) might be invoked while the network source is being created.</span></span> <span data-ttu-id="3f4c4-127">Portanto, se você criar a origem da rede chamando o método [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) síncrono, seu thread de chamada poderá bloquear enquanto as credenciais forem adquiridas.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-127">Therefore, if you create the network source by calling the synchronous [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) method, your calling thread might block while the credentials are acquired.</span></span> <span data-ttu-id="3f4c4-128">Portanto, é recomendável usar o método assíncrona [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-128">Therefore, it is recommended to use the asynchronous [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) method instead.</span></span>

 

## <a name="example"></a><span data-ttu-id="3f4c4-129">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3f4c4-129">Example</span></span>

<span data-ttu-id="3f4c4-130">Este exemplo mostra um tipo de comportamento que um Gerenciador de credenciais pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-130">This example shows one type of behavior that a credential manager could provide.</span></span>

<span data-ttu-id="3f4c4-131">Aqui está uma declaração da classe que implementa [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span><span class="sxs-lookup"><span data-stu-id="3f4c4-131">Here is a declaration of the class that implements [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager).</span></span>


```C++
class CCredentialManager : public IMFNetCredentialManager, IMFAsyncCallback 
{
    long                    m_cRef;
    IMFNetCredentialCache   *m_pCredentialCache;

public:
    CCredentialManager () : m_cRef(1), m_pCredentialCache(NULL)
    { 
    }
    ~CCredentialManager()
    {
        SafeRelease(&m_pCredentialCache);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CCredentialManager, IMFNetCredentialManager),
            QITABENT(CCredentialManager, IMFAsyncCallback),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }

    STDMETHODIMP BeginGetCredentials(
        MFNetCredentialManagerGetParam* pParam,
        IMFAsyncCallback* pCallback,
        IUnknown* pState
        );

    STDMETHODIMP EndGetCredentials(
        IMFAsyncResult* pResult, 
        IMFNetCredential** ppCred);

    STDMETHODIMP SetGood(IMFNetCredential* pCred, BOOL fGood)
    {
        if (!pCred)
        {
            return E_POINTER;
        }

        return m_pCredentialCache->SetGood(pCred, fGood);
    }


    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        return E_NOTIMPL;
    }

    STDMETHODIMP Invoke(IMFAsyncResult* pResult);
};
```



<span data-ttu-id="3f4c4-132">Para acompanhar o estado da operação [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) , a classe usa o seguinte objeto auxiliar:</span><span class="sxs-lookup"><span data-stu-id="3f4c4-132">To track the state of the [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) operation, the class uses the following helper object:</span></span>


```C++
// Holds state information for the GetCredentials operation, so that work can 
// be moved to a work-queue thread.

struct CredentialOp : public IUnknown
{
    long                m_cRef;
    IMFNetCredential    *m_pCredential;
    DWORD               m_dwFlags;

    CredentialOp(IMFNetCredential *pCredential) 
        : m_cRef(1), m_dwFlags(0), m_pCredential(pCredential)
    {
        m_pCredential->AddRef();
    }

    ~CredentialOp()
    {
        SafeRelease(&m_pCredential);
    }

    STDMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(CredentialOp, IUnknown),
            { 0 }
        };
        return QISearch(this, qit, riid, ppv);
    }      

    STDMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    STDMETHODIMP_(ULONG) Release()
    {
        LONG cRef = InterlockedDecrement(&m_cRef);
        if (cRef == 0)
        {
            delete this;
        }
        return cRef;
    }
};
```



<span data-ttu-id="3f4c4-133">O método [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) cria o cache de credencial e Obtém um ponteiro [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="3f4c4-133">The [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials) method creates the credential cache and gets an [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer.</span></span> <span data-ttu-id="3f4c4-134">Se o usuário precisar ser solicitado (indicado pelo sinalizador **require \_ prompt** ), o método chamará [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) para enfileirar um novo item de trabalho:</span><span class="sxs-lookup"><span data-stu-id="3f4c4-134">If the user must be prompted (indicated by the **REQUIRE\_PROMPT** flag), the method calls [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) to queue a new work item:</span></span>


```C++
STDMETHODIMP CCredentialManager::BeginGetCredentials(
    MFNetCredentialManagerGetParam* pParam,
    IMFAsyncCallback* pCallback,
    IUnknown* pState
    )
{
    if (!pParam || !pCallback)
    {
        return E_POINTER;
    }

    DWORD dwAuthenticationFlags = 0;
    DWORD dwRequirementFlags = 0;

    if (pParam->hrOp == NS_E_PROXY_ACCESSDENIED)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_PROXY;
    }

    if (pParam->fAllowLoggedOnUser)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_LOGGED_ON_USER;
    }

    if (pParam->fClearTextPackage)
    {
        dwAuthenticationFlags |= MFNET_AUTHENTICATION_CLEAR_TEXT;
    }

    IMFNetCredential *pCredential =  NULL;
    IMFAsyncResult* pResult = NULL;

    HRESULT hr = S_OK;

    if (m_pCredentialCache == NULL)
    {
        hr = MFCreateCredentialCache(&m_pCredentialCache);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    hr = m_pCredentialCache->GetCredential(
        pParam->pszUrl, 
        pParam->pszRealm, 
        dwAuthenticationFlags, 
        &pCredential, 
        &dwRequirementFlags
        );

    if (FAILED(hr))
    {
        goto done;
    }

    if( ( dwRequirementFlags & REQUIRE_PROMPT ) == 0 )
    {
        // The credential is good to use. Prompting the user is not required.
        hr = S_OK;
        goto done;
    }

    // The credential requires prompting the user. 
    CredentialOp *pOp = new (std::nothrow) CredentialOp(pCredential);

    if (pOp == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    // Set flags. Use these to inform the user if the credentials will
    // be sent in plaintext or saved in the credential cache.

    if (pParam->fClearTextPackage)
    {
        // Notify the user that credentials will be sent in plaintext.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT;
    }

    if(dwRequirementFlags & REQUIRE_SAVE_SELECTED )
    {
        // Credentials will be saved in the cache by default.
        pOp->m_dwFlags |= MFNET_CREDENTIAL_SAVE;
    }

    // NOTE: The application should enable to user to deselect these two flags;
    // for example, through check boxes in the prompt dialog.


    // Now queue the work item.

    hr = MFCreateAsyncResult(pOp, pCallback, pState, &pResult);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFPutWorkItem(MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION, this, pResult);

done:
    SafeRelease(&pResult);
    SafeRelease(&pCredential);
    SafeRelease(&pOp);
    return hr;
}
```



<span data-ttu-id="3f4c4-135">O thread de fila de trabalho chama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), que solicita o usuário e, em seguida, chama [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) para invocar o ponteiro de retorno de chamada que foi fornecido em [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span><span class="sxs-lookup"><span data-stu-id="3f4c4-135">The work-queue thread calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke), which prompts the user and then calls [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback) to invoke the callback pointer that was provided in [**BeginGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-begingetcredentials).</span></span>


```C++
STDMETHODIMP CCredentialManager::Invoke(IMFAsyncResult* pResult)
{
    IUnknown *pState = NULL;
    IMFAsyncResult *pGetCredentialsResult = NULL;
    IUnknown *pOpState = NULL;

    CredentialOp *pOp = NULL;   // not AddRef'd

    HRESULT hr = pResult->GetState(&pState);

    if (SUCCEEDED(hr))
    {
        hr = pState->QueryInterface(IID_PPV_ARGS(&pGetCredentialsResult));
    }

    if (SUCCEEDED(hr))
    {
        hr = pGetCredentialsResult->GetObject(&pOpState);
    }

    if (SUCCEEDED(hr))
    {
        pOp = static_cast<CredentialOp*>(pOpState);

        // Display a dialog for the user to enter user name and password.
        hr = PromptUserCredentials(pOp);
    }

    if (SUCCEEDED(hr) && m_pCredentialCache)
    {
        // Update with options set by the user.
        hr = m_pCredentialCache->SetUserOptions(
            pOp->m_pCredential, 
            pOp->m_dwFlags
            );
    }

    if (pGetCredentialsResult)
    {
        pGetCredentialsResult->SetStatus(hr);
        MFInvokeCallback(pGetCredentialsResult);
    }

    SafeRelease(&pState);
    SafeRelease(&pGetCredentialsResult);
    SafeRelease(&pOpState);
    return S_OK;
}
```



<span data-ttu-id="3f4c4-136">O método [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) conclui a operação retornando o ponteiro [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) para o chamador.</span><span class="sxs-lookup"><span data-stu-id="3f4c4-136">The [**EndGetCredentials**](/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialmanager-endgetcredentials) method completes the operation by returning the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) pointer to the caller.</span></span>


```C++
STDMETHODIMP CCredentialManager::EndGetCredentials(
    IMFAsyncResult* pResult, 
    IMFNetCredential** ppCred
    )
{
    if (!pResult || !ppCred)
    {
        return E_POINTER;
    }

    *ppCred = NULL;

    IUnknown *pUnk = NULL;

    // Check the result of the asynchronous operation.
    HRESULT hr = pResult->GetStatus();

    if (FAILED(hr))
    {
        // The operation failed.
        goto done;
    }

    hr = pResult->GetObject(&pUnk);
    if (FAILED(hr))
    {
        goto done;
    }

    CredentialOp *pOp = static_cast<CredentialOp*>(pUnk);

    *ppCred = pOp->m_pCredential;
    pOp->m_pCredential = NULL;

done:
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="3f4c4-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f4c4-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f4c4-138">Autenticação de origem da rede</span><span class="sxs-lookup"><span data-stu-id="3f4c4-138">Network Source Authentication</span></span>](network-source-authentication.md)
</dt> </dl>

 

 



