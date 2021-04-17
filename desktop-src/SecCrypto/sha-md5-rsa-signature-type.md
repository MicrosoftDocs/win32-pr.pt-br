---
description: Os CSPs para \_ o Prov RSA \_ Schannel devem dar suporte ao CALG \_ SSL3 \_ SHAMD5 hash que seja compatível com o provedor criptográfico base da Microsoft usado em SSL 3,0 e autenticação de cliente TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Tipo de assinatura do SHA/MD5 RSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757998"
---
# <a name="shamd5-rsa-signature-type"></a><span data-ttu-id="70613-103">Tipo de assinatura do SHA/MD5 RSA</span><span class="sxs-lookup"><span data-stu-id="70613-103">SHA/MD5 RSA Signature Type</span></span>

<span data-ttu-id="70613-104">Os CSPs para \_ o Prov RSA \_ Schannel devem dar suporte ao CALG \_ SSL3 \_ SHAMD5 [*hash*](../secgloss/h-gly.md) que seja compatível com o provedor CRIPTOGRÁFICO Base da Microsoft usado em SSL 3,0 e autenticação de cliente TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="70613-104">CSPs for PROV\_RSA\_SCHANNEL must support the CALG\_SSL3\_SHAMD5 [*hash*](../secgloss/h-gly.md) that is compatible with the Microsoft Base Cryptographic Provider used in SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="70613-105">Esse hash consiste em uma concatenação de um hash [*MD5*](../secgloss/m-gly.md) e um hash SHA assinado com uma chave privada RSA ou Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="70613-105">This hash consists of a concatenation of an [*MD5*](../secgloss/m-gly.md) hash and a SHA hash signed with an RSA or Diffie-Hellman private key.</span></span> <span data-ttu-id="70613-106">Um identificador para um valor de hash desse tipo é criado usando a função [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) ou [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) com CALG \_ SSL3 \_ SHAMD5 como o parâmetro *algid* .</span><span class="sxs-lookup"><span data-stu-id="70613-106">A handle to a hash value of this type is created by using the [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) or [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) function with CALG\_SSL3\_SHAMD5 as the *Algid* parameter.</span></span> <span data-ttu-id="70613-107">Exemplos de uso de funções de hash podem ser vistos no [programa c de exemplo: Criando e aplicando hash a uma chave de sessão e um](example-c-program-creating-and-hashing-a-session-key.md) [programa de exemplo c: assinando um hash e verificando a assinatura de hash](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span><span class="sxs-lookup"><span data-stu-id="70613-107">Examples of using hash functions can be seen in [Example C Program: Creating and Hashing a Session Key](example-c-program-creating-and-hashing-a-session-key.md) and [Example C Program: Signing a Hash and Verifying the Hash Signature](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span></span>

 

 
