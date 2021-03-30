---
title: Como assinar programaticamente um pacote do aplicativo (C++)
description: Saiba como assinar um pacote de aplicativo usando a função SignerSignEx2.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310ba2a934a6986809329a12afa8ee20b2f6591
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640445"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a><span data-ttu-id="2d9ba-103">Como assinar programaticamente um pacote do aplicativo (C++)</span><span class="sxs-lookup"><span data-stu-id="2d9ba-103">How to programmatically sign an app package (C++)</span></span>

<span data-ttu-id="2d9ba-104">Saiba como assinar um pacote de aplicativo usando a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .</span><span class="sxs-lookup"><span data-stu-id="2d9ba-104">Learn how to sign an app package by using the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span>

<span data-ttu-id="2d9ba-105">Se você quiser criar programaticamente pacotes de aplicativos do Windows usando a [API de empacotamento](interfaces.md), também precisará assinar os pacotes de aplicativos antes que eles possam ser implantados.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-105">If you want to programmatically create Windows app packages by using the [Packaging API](interfaces.md), you also need to sign the app packages before they can be deployed.</span></span> <span data-ttu-id="2d9ba-106">A API de empacotamento não fornece um método especializado para assinar pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-106">The Packaging API doesn't provide a specialized method for signing app packages.</span></span> <span data-ttu-id="2d9ba-107">Em vez disso, use as [funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions) padrão para assinar seus pacotes de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-107">Instead, use the standard [cryptography functions](/windows/desktop/SecCrypto/cryptography-functions) to sign your app packages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2d9ba-108">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="2d9ba-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2d9ba-109">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="2d9ba-109">Technologies</span></span>

-   <span data-ttu-id="2d9ba-110">[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d9ba-110">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   [<span data-ttu-id="2d9ba-111">Empacotamento, implantação e consulta de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="2d9ba-111">Packaging, deployment, and query of Windows apps</span></span>](appx-portal.md)
-   [<span data-ttu-id="2d9ba-112">funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="2d9ba-112">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a><span data-ttu-id="2d9ba-113">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="2d9ba-113">Prerequisites</span></span>

-   <span data-ttu-id="2d9ba-114">Você precisa ter um aplicativo do Windows empacotado.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-114">You need to have a packaged Windows app.</span></span> <span data-ttu-id="2d9ba-115">Para obter informações sobre como criar um pacote de aplicativo, consulte [como criar um pacote de aplicativo](how-to-create-a-package.md).</span><span class="sxs-lookup"><span data-stu-id="2d9ba-115">For info about creating an app package, see [How to create an app package](how-to-create-a-package.md).</span></span>
-   <span data-ttu-id="2d9ba-116">Você precisa ter um certificado de assinatura de código apropriado para assinar o pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-116">You need to have a code signing certificate that is appropriate for signing the app package.</span></span> <span data-ttu-id="2d9ba-117">Para obter informações sobre como criar um certificado de assinatura de código de teste, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="2d9ba-117">For info about creating a test code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span> <span data-ttu-id="2d9ba-118">Carregue esse certificado de autenticação em uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="2d9ba-118">Load this signing certificate into a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="2d9ba-119">Por exemplo, você pode usar [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) e [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) para carregar um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-119">For example, you can use [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) and [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) to load a signing certificate.</span></span>
-   <span data-ttu-id="2d9ba-120">O Windows 8 apresenta a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .</span><span class="sxs-lookup"><span data-stu-id="2d9ba-120">Windows 8 introduces the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span> <span data-ttu-id="2d9ba-121">Use **SignerSignEx2** ao assinar pacotes de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-121">Use **SignerSignEx2** when you sign Windows app packages.</span></span>

## <a name="instructions"></a><span data-ttu-id="2d9ba-122">Instruções</span><span class="sxs-lookup"><span data-stu-id="2d9ba-122">Instructions</span></span>

### <a name="step-1-define-the-required-structures-for-signersignex2"></a><span data-ttu-id="2d9ba-123">Etapa 1: definir as estruturas necessárias para SignerSignEx2</span><span class="sxs-lookup"><span data-stu-id="2d9ba-123">Step 1: Define the required structures for SignerSignEx2</span></span>

<span data-ttu-id="2d9ba-124">Além do cabeçalho Wincrypt. h, a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) depende de muitas estruturas que não estão definidas em nenhum arquivo de cabeçalho do SDK.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-124">In addition to the Wincrypt.h header, the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function depends on many structures that aren't defined in any SDK header file.</span></span> <span data-ttu-id="2d9ba-125">Para usar o **SignerSignEx2**, você mesmo deve definir essas estruturas:</span><span class="sxs-lookup"><span data-stu-id="2d9ba-125">To use **SignerSignEx2**, you must define these structures yourself:</span></span>


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a><span data-ttu-id="2d9ba-126">Etapa 2: chamar SignerSignEx2 para assinar o pacote do aplicativo</span><span class="sxs-lookup"><span data-stu-id="2d9ba-126">Step 2: Call SignerSignEx2 to sign the app package</span></span>

<span data-ttu-id="2d9ba-127">Depois de definir as estruturas necessárias que são especificadas na etapa anterior, você pode usar qualquer uma das opções disponíveis na função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) para assinar um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-127">After you define the required structures that are specified in the previous step, you can use any of the options available on the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function to sign an app package.</span></span> <span data-ttu-id="2d9ba-128">Quando você usa o **SignerSignEx2** com pacotes de aplicativos do Windows, essas restrições se aplicam:</span><span class="sxs-lookup"><span data-stu-id="2d9ba-128">When you use **SignerSignEx2** with Windows app packages, these restrictions apply:</span></span>

-   <span data-ttu-id="2d9ba-129">Você deve fornecer um ponteiro para uma estrutura de **dados de cliente do Appx \_ \_ \_ SIP** como o parâmetro *pSipData* ao assinar um pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-129">You must provide a pointer to an **APPX\_SIP\_CLIENT\_DATA** structure as the *pSipData* parameter when you sign an app package.</span></span> <span data-ttu-id="2d9ba-130">Você deve preencher o membro **pSignerParams** dos **\_ \_ \_ dados do cliente do Appx SIP** com os mesmos parâmetros que você usa para assinar o pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-130">You must populate the **pSignerParams** member of **APPX\_SIP\_CLIENT\_DATA** with the same parameters that you use to sign the app package.</span></span> <span data-ttu-id="2d9ba-131">Para fazer isso, defina os parâmetros desejados na estrutura de **\_ \_ \_ parâmetros de EX2 do assinante** , atribua o endereço dessa estrutura a **pSignerParams** e, em seguida, referencie diretamente os membros da estrutura também ao chamar [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span><span class="sxs-lookup"><span data-stu-id="2d9ba-131">To do this, define your desired parameters on the **SIGNER\_SIGN\_EX2\_PARAMS** structure, assign the address of this structure to **pSignerParams**, and then directly reference the structure's members as well when you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span></span>
-   <span data-ttu-id="2d9ba-132">Depois de chamar [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), você deverá liberar o **pAppxSipState** no *PSipData* chamando [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em **pAppxSipState** se ele não for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-132">After you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), you must free the **pAppxSipState** on the *pSipData* by calling [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on **pAppxSipState** if it's not **NULL**.</span></span>
-   <span data-ttu-id="2d9ba-133">O membro **algidHash** da estrutura **de \_ \_ informações de assinatura do signatário** deve ser o mesmo algoritmo de hash que foi usado na criação do pacote do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-133">The **algidHash** member of the **SIGNER\_SIGNATURE\_INFO** structure must be the same hash algorithm that was used in creating the app package.</span></span> <span data-ttu-id="2d9ba-134">Para obter informações sobre como determinar o algoritmo de hash do pacote do aplicativo, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="2d9ba-134">For info about how to determine the hash algorithm from the app package, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="2d9ba-135">O algoritmo padrão do Windows 8 que o [MakeAppx](make-appx-package--makeappx-exe-.md) e o Visual Studio usam para criar pacotes de aplicativos é "ALGIDHASH = CALG \_ Sha \_ 256".</span><span class="sxs-lookup"><span data-stu-id="2d9ba-135">The Windows 8 default algorithm that [MakeAppx](make-appx-package--makeappx-exe-.md) and Visual Studio use to create app packages is “algidHash = CALG\_SHA\_256”.</span></span>
-   <span data-ttu-id="2d9ba-136">Se você quiser carimbar o tempo da assinatura no pacote do aplicativo também, deverá fazê-lo durante a chamada para [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) fornecendo os parâmetros opcionais de carimbo de hora (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*) do **SignerSignEx2**.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-136">If you want to time stamp the signature on the app package as well, you must do so during the call to [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) by providing **SignerSignEx2**'s optional time stamping parameters (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*).</span></span> <span data-ttu-id="2d9ba-137">Não há suporte para a chamada de [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) ou suas variantes em um pacote de aplicativo que já esteja assinado.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-137">Calling [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) or its variants on an app package that is already signed is unsupported.</span></span>

<span data-ttu-id="2d9ba-138">Aqui está um código de exemplo que mostra como chamar [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span><span class="sxs-lookup"><span data-stu-id="2d9ba-138">Here is some example code that shows how to call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span></span>


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="2d9ba-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d9ba-139">Remarks</span></span>

<span data-ttu-id="2d9ba-140">Depois de assinar o pacote do aplicativo, você também pode tentar validar a assinatura programaticamente usando a função [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) com a **ação de WINTRUST \_ \_ \_ Verify \_ v2**.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-140">After you sign the app package, you can also attempt to validate the signature programmatically by using the [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) function with **WINTRUST\_ACTION\_GENERIC\_VERIFY\_V2**.</span></span> <span data-ttu-id="2d9ba-141">Não há considerações especiais nesse caso para o uso de **WinVerifyTrust** com pacotes de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="2d9ba-141">There are no special considerations in this case for using **WinVerifyTrust** with Windows app packages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d9ba-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2d9ba-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2d9ba-143">[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2d9ba-143">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2d9ba-144">API de empacotamento</span><span class="sxs-lookup"><span data-stu-id="2d9ba-144">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="2d9ba-145">funções de criptografia</span><span class="sxs-lookup"><span data-stu-id="2d9ba-145">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 