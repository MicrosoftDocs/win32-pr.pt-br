---
description: As funções a seguir estão entre as funções de CryptoAPI que podem ser estendidas.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Criando a nova funcionalidade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501550"
---
# <a name="creating-the-new-functionality"></a><span data-ttu-id="ad2d7-103">Criando a nova funcionalidade</span><span class="sxs-lookup"><span data-stu-id="ad2d7-103">Creating the New Functionality</span></span>

<span data-ttu-id="ad2d7-104">As funções a seguir estão entre as funções de CryptoAPI que podem ser estendidas.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-104">The following functions are among the CryptoAPI functions that can be extended.</span></span>



| <span data-ttu-id="ad2d7-105">Função CryptoAPI</span><span class="sxs-lookup"><span data-stu-id="ad2d7-105">CryptoAPI function</span></span>                                   | <span data-ttu-id="ad2d7-106">Definição de nome da função de OID</span><span class="sxs-lookup"><span data-stu-id="ad2d7-106">OID function name define</span></span>                         | <span data-ttu-id="ad2d7-107">Cadeia de nome da função de OID</span><span class="sxs-lookup"><span data-stu-id="ad2d7-107">OID function name string</span></span>  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="ad2d7-108">**CryptEncodeObject**</span><span class="sxs-lookup"><span data-stu-id="ad2d7-108">**CryptEncodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | <span data-ttu-id="ad2d7-109">objeto de codificação de OID cript. \_ \_ \_ \_ Func</span><span class="sxs-lookup"><span data-stu-id="ad2d7-109">CRYPT\_OID\_ENCODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="ad2d7-110">"CryptDllEncodeObject"</span><span class="sxs-lookup"><span data-stu-id="ad2d7-110">"CryptDllEncodeObject"</span></span>    |
| [<span data-ttu-id="ad2d7-111">**CryptDecodeObject**</span><span class="sxs-lookup"><span data-stu-id="ad2d7-111">**CryptDecodeObject**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | <span data-ttu-id="ad2d7-112">\_objeto de \_ decodificação de OID cript \_ . \_</span><span class="sxs-lookup"><span data-stu-id="ad2d7-112">CRYPT\_OID\_DECODE\_ OBJECT\_FUNC</span></span><br/>     | <span data-ttu-id="ad2d7-113">"CryptDllDecodeObject"</span><span class="sxs-lookup"><span data-stu-id="ad2d7-113">"CryptDllDecodeObject"</span></span>    |
| [<span data-ttu-id="ad2d7-114">**CertOpenStore**</span><span class="sxs-lookup"><span data-stu-id="ad2d7-114">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | <span data-ttu-id="ad2d7-115">\_identificação de \_ Prov aberto do \_ repositório de \_ OID cript \_</span><span class="sxs-lookup"><span data-stu-id="ad2d7-115">CRYPT\_OID\_OPEN\_ STORE\_PROV\_FUNC</span></span><br/>  | <span data-ttu-id="ad2d7-116">"CertDllOpenStoreProv"</span><span class="sxs-lookup"><span data-stu-id="ad2d7-116">"CertDllOpenStoreProv"</span></span>    |
| [<span data-ttu-id="ad2d7-117">**CertVerifyCTLUsage**</span><span class="sxs-lookup"><span data-stu-id="ad2d7-117">**CertVerifyCTLUsage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | <span data-ttu-id="ad2d7-118">\_identificação da \_ CTL de verificação de OID cript \_ \_ . \_</span><span class="sxs-lookup"><span data-stu-id="ad2d7-118">CRYPT\_OID\_VERIFY\_ CTL\_USAGE\_FUNC</span></span><br/> | <span data-ttu-id="ad2d7-119">"CertDllVerifyCTLUsage"</span><span class="sxs-lookup"><span data-stu-id="ad2d7-119">"CertDllVerifyCTLUsage"</span></span>   |
| [<span data-ttu-id="ad2d7-120">**CertVerifyRevocation**</span><span class="sxs-lookup"><span data-stu-id="ad2d7-120">**CertVerifyRevocation**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | <span data-ttu-id="ad2d7-121">\_ \_ \_ FUNCde verificar revogação de OID \_ cript</span><span class="sxs-lookup"><span data-stu-id="ad2d7-121">CRYPT\_OID\_VERIFY\_ REVOCATION\_FUNC</span></span><br/> | <span data-ttu-id="ad2d7-122">"CertDllVerifyRevocation"</span><span class="sxs-lookup"><span data-stu-id="ad2d7-122">"CertDllVerifyRevocation"</span></span> |



 

<span data-ttu-id="ad2d7-123">No uso normal com um OID e um tipo de codificação existentes, o código na função CryptoAPI, em si, é usado.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-123">In normal use with an existing OID and encoding type, the code in the CryptoAPI function, itself, is used.</span></span> <span data-ttu-id="ad2d7-124">Se uma dessas funções for chamada com um tipo de OID e codificação que o código na função CryptoAPI não foi projetado para manipular, uma nova função, contendo a nova funcionalidade, deverá ser criada em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-124">If one of these functions is called with an OID and encoding type that code in the CryptoAPI function was not designed to handle, a new function, containing the new functionality, must be created in a DLL.</span></span> <span data-ttu-id="ad2d7-125">Essa DLL deve ser registrada no registro ou instalada na memória.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-125">That DLL must be registered in the registry or installed in memory.</span></span>

<span data-ttu-id="ad2d7-126">Quando uma das funções listadas é chamada com o OID e o tipo de codificação designados recentemente, o código na nova DLL é usado em vez do código fornecido como parte da função CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-126">When one of the listed functions is called with the newly designated OID and encoding type, the code in the new DLL is used rather than the code provided as part of the CryptoAPI function.</span></span>

<span data-ttu-id="ad2d7-127">O nome da função desenvolvida recentemente pode ser o nome listado em "cadeia de nome da função OID" na tabela anterior ou um nome diferente pode ser fornecido quando o novo código de função é registrado.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-127">The name of the newly developed function can be the name listed under "OID function name string" in the previous table or a different name can be given when the new function code is registered.</span></span>

<span data-ttu-id="ad2d7-128">A nova função deve usar um protótipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-128">The new function must use an appropriate prototype.</span></span> <span data-ttu-id="ad2d7-129">Em todos os casos, exceto para [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), esse protótipo é o mesmo que a função CryptoAPI que chama a nova função.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-129">In all cases except for [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), this prototype is the same as the CryptoAPI function that calls the new function.</span></span> <span data-ttu-id="ad2d7-130">No caso do **CertOpenStore** , o protótipo é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-130">In the case of **CertOpenStore** the prototype is as follows.</span></span>


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> <span data-ttu-id="ad2d7-131">Se os protótipos não corresponderem, a pilha do sistema será corrompida.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-131">If the prototypes do not match, the system stack will be corrupted.</span></span>

 

<span data-ttu-id="ad2d7-132">Além de fornecer o código para a nova função em uma DLL, estender a funcionalidade de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) ou [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requer uma definição de tipo para que a nova estrutura de dados C seja colocada em um arquivo de cabeçalho incluído quando o programa do usuário é compilado.</span><span class="sxs-lookup"><span data-stu-id="ad2d7-132">In addition to providing the code for the new function in a DLL, extending the functionality of [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) or [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requires a type definition for the new C data structure to be placed in a header file included when the user's program is compiled.</span></span>

 

 




