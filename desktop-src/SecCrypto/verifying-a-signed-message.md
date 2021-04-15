---
description: Estas etapas verificam a assinatura de dados assinados.
ms.assetid: 18246cc1-d3c4-4426-a342-ce3864cc412e
title: Verificando uma mensagem assinada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f85a5bcde56df7bb41bb92276123bcd26024e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768426"
---
# <a name="verifying-a-signed-message"></a><span data-ttu-id="8e63b-103">Verificando uma mensagem assinada</span><span class="sxs-lookup"><span data-stu-id="8e63b-103">Verifying a Signed Message</span></span>

<span data-ttu-id="8e63b-104">Estas etapas verificam a assinatura de dados assinados.</span><span class="sxs-lookup"><span data-stu-id="8e63b-104">These steps verify the signature of signed data.</span></span> <span data-ttu-id="8e63b-105">A ilustração a seguir descreve as tarefas individuais que devem ser realizadas, conforme mostrado na lista que a segue.</span><span class="sxs-lookup"><span data-stu-id="8e63b-105">The following illustration depicts the individual tasks that must be accomplished, as shown in the list that follows it.</span></span>

![Verificando uma mensagem assinada](images/verifmsg.png)

<span data-ttu-id="8e63b-107">**Para verificar a assinatura de uma mensagem assinada**</span><span class="sxs-lookup"><span data-stu-id="8e63b-107">**To verify the signature of a signed message**</span></span>

1.  <span data-ttu-id="8e63b-108">Obtenha um ponteiro para a mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="8e63b-108">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="8e63b-109">Abra um [*repositório de certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8e63b-109">Open a [*certificate store*](../secgloss/c-gly.md).</span></span>
3.  <span data-ttu-id="8e63b-110">Usando a ID de signatário contida na mensagem, obtenha o certificado do remetente e obtenha um identificador para sua [*chave pública*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="8e63b-110">Using the signer ID contained in the message, get the sender's certificate and get a handle to its [*public key*](../secgloss/p-gly.md).</span></span>

    <span data-ttu-id="8e63b-111">Como alternativa às etapas 2 e 3, você pode usar o certificado contido na mensagem para recuperar a chave pública do signatário.</span><span class="sxs-lookup"><span data-stu-id="8e63b-111">As an alternative to steps 2 and 3, you can use the certificate contained in the message to retrieve the signer's public key.</span></span>

4.  <span data-ttu-id="8e63b-112">Usando a chave pública do signatário, descriptografe a assinatura digital, produzindo o resumo original dos dados na mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e63b-112">Using the signer's public key, decrypt the digital signature, producing the original digest of the data in the message.</span></span>
5.  <span data-ttu-id="8e63b-113">Usando o algoritmo de hash contido na mensagem, gere o [*hash*](../secgloss/h-gly.md) dos dados contidos na mensagem, produzindo um novo Resumo.</span><span class="sxs-lookup"><span data-stu-id="8e63b-113">Using the hash algorithm contained in the message, [*hash*](../secgloss/h-gly.md) the data contained in the message, yielding a new digest.</span></span>
6.  <span data-ttu-id="8e63b-114">Compare o resumo recuperado da mensagem com o novo Resumo recém-criado.</span><span class="sxs-lookup"><span data-stu-id="8e63b-114">Compare the digest retrieved from the message with the new digest just created.</span></span>
7.  <span data-ttu-id="8e63b-115">Se os dois resumos forem correspondentes, a assinatura será verificada.</span><span class="sxs-lookup"><span data-stu-id="8e63b-115">If the two digests match, the signature is verified.</span></span> <span data-ttu-id="8e63b-116">Isso significa que a [*chave privada*](../secgloss/p-gly.md) usada para assinar os dados corresponde à chave pública usada apenas para descriptografar a assinatura e que os dados não foram alterados desde que os dados foram assinados.</span><span class="sxs-lookup"><span data-stu-id="8e63b-116">This means that the [*private key*](../secgloss/p-gly.md) that was used to sign the data matches the public key just used to decrypt the signature, and that the data has not changed since the data was signed.</span></span>

    <span data-ttu-id="8e63b-117">Se os dois resumos não corresponderem, a assinatura não será verificada e as chaves privada/pública não corresponderão, ou os dados foram alterados desde que os dados foram assinados, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="8e63b-117">If the two digests do not match, the signature is not verified, and either the private/public keys do not match, or the data has been changed since the data was signed, or both.</span></span>

<span data-ttu-id="8e63b-118">Uma única função, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), pode ser usada para verificar uma assinatura, conforme mostrado no procedimento a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e63b-118">A single function, [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature), can be used to verify a signature, as shown in the following procedure.</span></span>

<span data-ttu-id="8e63b-119">**Para verificar uma mensagem assinada**</span><span class="sxs-lookup"><span data-stu-id="8e63b-119">**To verify a signed message**</span></span>

1.  <span data-ttu-id="8e63b-120">Obtenha um ponteiro para a mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="8e63b-120">Get a pointer to the signed message.</span></span>
2.  <span data-ttu-id="8e63b-121">Obtenha o tamanho da mensagem assinada.</span><span class="sxs-lookup"><span data-stu-id="8e63b-121">Get the size of the signed message.</span></span>
3.  <span data-ttu-id="8e63b-122">Obtenha um identificador em um provedor criptográfico.</span><span class="sxs-lookup"><span data-stu-id="8e63b-122">Get a handle on a cryptographic provider.</span></span>
4.  <span data-ttu-id="8e63b-123">Inicialize a estrutura da [**\_ \_ mensagem \_ de verificação cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) .</span><span class="sxs-lookup"><span data-stu-id="8e63b-123">Initialize the [**CRYPT\_VERIFY\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) structure.</span></span>
5.  <span data-ttu-id="8e63b-124">Chame [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) para verificar a assinatura.</span><span class="sxs-lookup"><span data-stu-id="8e63b-124">Call [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature) to verify the signature.</span></span>

<span data-ttu-id="8e63b-125">O código que implementa esse procedimento está incluído no [programa de exemplo C: assinando uma mensagem e verificando uma assinatura de mensagem](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span><span class="sxs-lookup"><span data-stu-id="8e63b-125">Code that implements this procedure is included in [Example C Program: Signing a Message and Verifying a Message Signature](example-c-program-signing-a-message-and-verifying-a-message-signature.md).</span></span>

 

 
