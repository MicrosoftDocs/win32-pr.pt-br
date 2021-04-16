---
description: As credenciais Schannel são representadas internamente como estruturas de contexto de certificado \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 chaves privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750103"
---
# <a name="cryptoapi-20-private-keys"></a><span data-ttu-id="5d462-103">CryptoAPI 2.0 chaves privadas</span><span class="sxs-lookup"><span data-stu-id="5d462-103">CryptoAPI 2.0 Private Keys</span></span>

<span data-ttu-id="5d462-104">As credenciais Schannel são representadas internamente como estruturas de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="5d462-104">Schannel credentials are represented internally as [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structures.</span></span> <span data-ttu-id="5d462-105">O Schannel localiza a [*chave privada*](/windows/desktop/SecGloss/p-gly) associada a um contexto de certificado específico usando a propriedade de \_ \_ ID de \_ prop info da chave de certificado Prov do certificado \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5d462-105">Schannel locates the [*private key*](/windows/desktop/SecGloss/p-gly) associated with a particular certificate context using the certificate's CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span> <span data-ttu-id="5d462-106">Usando essa propriedade, o Schannel acessa a *chave privada* chamando a função [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) .</span><span class="sxs-lookup"><span data-stu-id="5d462-106">Using this property, Schannel accesses the *private key* by calling the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) function.</span></span> <span data-ttu-id="5d462-107">Para obter detalhes adicionais, consulte [pares de chaves pública/privada](/windows/desktop/SecCrypto/public-private-key-pairs).</span><span class="sxs-lookup"><span data-stu-id="5d462-107">For additional details, see [Public/Private Key Pairs](/windows/desktop/SecCrypto/public-private-key-pairs).</span></span>

<span data-ttu-id="5d462-108">Cada credencial Schannel contém uma referência a uma ou mais chaves privadas, cada uma associada a um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="5d462-108">Every Schannel credential contains a reference to one or more private keys, each associated with a particular certificate.</span></span> <span data-ttu-id="5d462-109">As [*chaves privadas*](/windows/desktop/SecGloss/p-gly) são tratadas de forma muito diferente, dependendo se a credencial é para um cliente ou um servidor.</span><span class="sxs-lookup"><span data-stu-id="5d462-109">The [*private keys*](/windows/desktop/SecGloss/p-gly) are handled quite differently depending on whether the credential is for a client or a server.</span></span>

## <a name="client-private-keys"></a><span data-ttu-id="5d462-110">Chaves privadas do cliente</span><span class="sxs-lookup"><span data-stu-id="5d462-110">Client Private Keys</span></span>

<span data-ttu-id="5d462-111">[*As chaves privadas*](/windows/desktop/SecGloss/p-gly) do cliente são gerenciadas pelo CSP ( [*provedor de serviços de criptografia*](/windows/desktop/SecGloss/c-gly) ) em uso.</span><span class="sxs-lookup"><span data-stu-id="5d462-111">Client [*private keys*](/windows/desktop/SecGloss/p-gly) are managed by the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) in use.</span></span> <span data-ttu-id="5d462-112">As chaves privadas do cliente normalmente são armazenadas por CSPs do tipo [Prov \_ RSA \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) ou Prov \_ RSA \_ Signature.</span><span class="sxs-lookup"><span data-stu-id="5d462-112">Client private keys are typically stored by CSPs of type [PROV\_RSA\_FULL](/windows/desktop/SecCrypto/prov-rsa-full) or PROV\_RSA\_SIGNATURE.</span></span>

<span data-ttu-id="5d462-113">Se o aplicativo cliente fizer a chamada de [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) manualmente antes de chamar [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), o cliente deverá associar o identificador do CSP ao contexto do certificado usando a \_ propriedade de ID de prop Handle chave de certificado \_ Prov \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5d462-113">If the client application makes the [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) call manually then before calling [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), the client must bind the CSP's handle to the certificate context using the CERT\_KEY\_PROV\_HANDLE\_PROP\_ID property.</span></span> <span data-ttu-id="5d462-114">Se o Schannel encontrar esse conjunto de propriedades, ele não usará \_ a \_ \_ propriedade de \_ ID prop de informações da chave de certificado Prov \_ .</span><span class="sxs-lookup"><span data-stu-id="5d462-114">If Schannel finds this property set, it does not use the CERT\_KEY\_PROV\_INFO\_PROP\_ID property.</span></span>

## <a name="server-private-keys"></a><span data-ttu-id="5d462-115">Chaves privadas do servidor</span><span class="sxs-lookup"><span data-stu-id="5d462-115">Server Private Keys</span></span>

<span data-ttu-id="5d462-116">As chaves privadas do servidor são armazenadas por um dos seguintes CSPs:</span><span class="sxs-lookup"><span data-stu-id="5d462-116">Server private keys are stored by one of the following CSPs:</span></span>

-   <span data-ttu-id="5d462-117">PROV \_ RSA \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="5d462-117">PROV\_RSA\_SCHANNEL</span></span>
-   <span data-ttu-id="5d462-118">PROV \_ DH \_ Schannel</span><span class="sxs-lookup"><span data-stu-id="5d462-118">PROV\_DH\_SCHANNEL</span></span>
-   <span data-ttu-id="5d462-119">CSP do PROV \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="5d462-119">PROV\_FORTEZZA CSP</span></span>

<span data-ttu-id="5d462-120">A escolha do CSP depende do algoritmo de [*troca de chaves*](/windows/desktop/SecGloss/k-gly)selecionado.</span><span class="sxs-lookup"><span data-stu-id="5d462-120">The choice of CSP depends on the selected [*key exchange algorithm*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="5d462-121">As chaves privadas do servidor devem ser do tipo em troca de chave \_ .</span><span class="sxs-lookup"><span data-stu-id="5d462-121">Server private keys must be of type AT\_KEYEXCHANGE.</span></span>

 

 
