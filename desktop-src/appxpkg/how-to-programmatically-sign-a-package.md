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
# <a name="how-to-programmatically-sign-an-app-package-c"></a>Como assinar programaticamente um pacote do aplicativo (C++)

Saiba como assinar um pacote de aplicativo usando a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .

Se você quiser criar programaticamente pacotes de aplicativos do Windows usando a [API de empacotamento](interfaces.md), também precisará assinar os pacotes de aplicativos antes que eles possam ser implantados. A API de empacotamento não fornece um método especializado para assinar pacotes de aplicativos. Em vez disso, use as [funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions) padrão para assinar seus pacotes de aplicativos.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Empacotamento, implantação e consulta de aplicativos do Windows](appx-portal.md)
-   [funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>Pré-requisitos

-   Você precisa ter um aplicativo do Windows empacotado. Para obter informações sobre como criar um pacote de aplicativo, consulte [como criar um pacote de aplicativo](how-to-create-a-package.md).
-   Você precisa ter um certificado de assinatura de código apropriado para assinar o pacote do aplicativo. Para obter informações sobre como criar um certificado de assinatura de código de teste, consulte [como criar um certificado de assinatura de pacote de aplicativo](how-to-create-a-package-signing-certificate.md). Carregue esse certificado de autenticação em uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Por exemplo, você pode usar [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) e [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) para carregar um certificado de autenticação.
-   O Windows 8 apresenta a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) . Use **SignerSignEx2** ao assinar pacotes de aplicativos do Windows.

## <a name="instructions"></a>Instruções

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>Etapa 1: definir as estruturas necessárias para SignerSignEx2

Além do cabeçalho Wincrypt. h, a função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) depende de muitas estruturas que não estão definidas em nenhum arquivo de cabeçalho do SDK. Para usar o **SignerSignEx2**, você mesmo deve definir essas estruturas:


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



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>Etapa 2: chamar SignerSignEx2 para assinar o pacote do aplicativo

Depois de definir as estruturas necessárias que são especificadas na etapa anterior, você pode usar qualquer uma das opções disponíveis na função [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) para assinar um pacote de aplicativo. Quando você usa o **SignerSignEx2** com pacotes de aplicativos do Windows, essas restrições se aplicam:

-   Você deve fornecer um ponteiro para uma estrutura de **dados de cliente do Appx \_ \_ \_ SIP** como o parâmetro *pSipData* ao assinar um pacote de aplicativo. Você deve preencher o membro **pSignerParams** dos **\_ \_ \_ dados do cliente do Appx SIP** com os mesmos parâmetros que você usa para assinar o pacote do aplicativo. Para fazer isso, defina os parâmetros desejados na estrutura de **\_ \_ \_ parâmetros de EX2 do assinante** , atribua o endereço dessa estrutura a **pSignerParams** e, em seguida, referencie diretamente os membros da estrutura também ao chamar [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).
-   Depois de chamar [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), você deverá liberar o **pAppxSipState** no *PSipData* chamando [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em **pAppxSipState** se ele não for **nulo**.
-   O membro **algidHash** da estrutura **de \_ \_ informações de assinatura do signatário** deve ser o mesmo algoritmo de hash que foi usado na criação do pacote do aplicativo. Para obter informações sobre como determinar o algoritmo de hash do pacote do aplicativo, consulte [como assinar um pacote de aplicativo usando Signtool](how-to-sign-a-package-using-signtool.md). O algoritmo padrão do Windows 8 que o [MakeAppx](make-appx-package--makeappx-exe-.md) e o Visual Studio usam para criar pacotes de aplicativos é "ALGIDHASH = CALG \_ Sha \_ 256".
-   Se você quiser carimbar o tempo da assinatura no pacote do aplicativo também, deverá fazê-lo durante a chamada para [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) fornecendo os parâmetros opcionais de carimbo de hora (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*) do **SignerSignEx2**. Não há suporte para a chamada de [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) ou suas variantes em um pacote de aplicativo que já esteja assinado.

Aqui está um código de exemplo que mostra como chamar [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):


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



## <a name="remarks"></a>Comentários

Depois de assinar o pacote do aplicativo, você também pode tentar validar a assinatura programaticamente usando a função [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) com a **ação de WINTRUST \_ \_ \_ Verify \_ v2**. Não há considerações especiais nesse caso para o uso de **WinVerifyTrust** com pacotes de aplicativos do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução à assinatura de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[API de empacotamento](interfaces.md)
</dt> <dt>

[funções de criptografia](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 