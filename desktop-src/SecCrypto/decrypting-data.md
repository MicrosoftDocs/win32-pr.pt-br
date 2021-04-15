---
description: Apresenta as etapas para descriptografar uma mensagem criptografada.
ms.assetid: 6af7dd28-325e-431a-9cdb-109d93af6302
title: Descriptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970f16862bb8c6693b2ff11f519af3f7c412024b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297680"
---
# <a name="decrypting-data"></a><span data-ttu-id="9ce94-103">Descriptografando dados</span><span class="sxs-lookup"><span data-stu-id="9ce94-103">Decrypting Data</span></span>

<span data-ttu-id="9ce94-104">Esta seção apresenta as etapas para descriptografar uma mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="9ce94-104">This section presents the steps to decrypt an encrypted message.</span></span>

<span data-ttu-id="9ce94-105">**Para descriptografar uma mensagem criptografada**</span><span class="sxs-lookup"><span data-stu-id="9ce94-105">**To decrypt an encrypted message**</span></span>

1.  <span data-ttu-id="9ce94-106">Obtenha um ponteiro para a mensagem digitalmente envelopada.</span><span class="sxs-lookup"><span data-stu-id="9ce94-106">Get a pointer to the digitally enveloped message.</span></span>
2.  <span data-ttu-id="9ce94-107">Abra um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ce94-107">Open a certificate store.</span></span>
3.  <span data-ttu-id="9ce94-108">Na mensagem, recupere o identificador de destinatário (minha ID).</span><span class="sxs-lookup"><span data-stu-id="9ce94-108">From the message, retrieve the recipient identifier (My ID).</span></span>
4.  <span data-ttu-id="9ce94-109">Use o identificador de destinatário para recuperar o certificado.</span><span class="sxs-lookup"><span data-stu-id="9ce94-109">Use the recipient identifier to retrieve the certificate.</span></span>
5.  <span data-ttu-id="9ce94-110">Obtenha a chave privada para o certificado.</span><span class="sxs-lookup"><span data-stu-id="9ce94-110">Get the private key for the certificate.</span></span>
6.  <span data-ttu-id="9ce94-111">Use a chave privada para descriptografar a chave simétrica (sessão).</span><span class="sxs-lookup"><span data-stu-id="9ce94-111">Use the private key to decrypt the symmetric (session) key.</span></span>
7.  <span data-ttu-id="9ce94-112">Recupere o algoritmo de criptografia da mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ce94-112">Retrieve the encryption algorithm from the message.</span></span>
8.  <span data-ttu-id="9ce94-113">Usando a chave de sessão descriptografada e o algoritmo de criptografia, descriptografe os dados.</span><span class="sxs-lookup"><span data-stu-id="9ce94-113">Using the decrypted session key and the encryption algorithm, decrypt the data.</span></span>

<span data-ttu-id="9ce94-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) faz todas as tarefas para descriptografar uma mensagem; no entanto, a inicialização de estruturas e outros dados ainda é necessária.</span><span class="sxs-lookup"><span data-stu-id="9ce94-114">[**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) does all of the tasks for decrypting a message; however, initialization of structures and other data is still necessary.</span></span>

<span data-ttu-id="9ce94-115">**Para descriptografar dados usando CryptDecryptMessage**</span><span class="sxs-lookup"><span data-stu-id="9ce94-115">**To decrypt data using CryptDecryptMessage**</span></span>

1.  <span data-ttu-id="9ce94-116">Obtenha um ponteiro para o BLOB criptografado.</span><span class="sxs-lookup"><span data-stu-id="9ce94-116">Get a pointer to the encrypted BLOB.</span></span>
2.  <span data-ttu-id="9ce94-117">Abra um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ce94-117">Open a certificate store.</span></span>
3.  <span data-ttu-id="9ce94-118">Criar uma matriz de repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="9ce94-118">Create a certificate store array.</span></span>
4.  <span data-ttu-id="9ce94-119">Inicialize a [**estrutura \_ criptografar \_ mensagem \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) .</span><span class="sxs-lookup"><span data-stu-id="9ce94-119">Initialize the [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para) structure.</span></span>
5.  <span data-ttu-id="9ce94-120">Chame [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para descriptografar os dados contidos na mensagem.</span><span class="sxs-lookup"><span data-stu-id="9ce94-120">Call [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to decrypt the data contained in the message.</span></span>

<span data-ttu-id="9ce94-121">[Programa C de exemplo: usar CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implementa o procedimento que acabou de ser apresentado.</span><span class="sxs-lookup"><span data-stu-id="9ce94-121">[Example C Program: Using CryptEncryptMessage and CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) implements the procedure just presented.</span></span> <span data-ttu-id="9ce94-122">Os comentários mostram quais elementos de código realizam cada etapa no procedimento.</span><span class="sxs-lookup"><span data-stu-id="9ce94-122">Comments show which code elements accomplish each step in the procedure.</span></span> <span data-ttu-id="9ce94-123">Para obter detalhes sobre a função, consulte [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)e para obter detalhes sobre a estrutura de dados, consulte [**\_ \_ mensagens \_ de descriptografia cript**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span><span class="sxs-lookup"><span data-stu-id="9ce94-123">For details about the function, see [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage), and for details about the data structure, see [**CRYPT\_DECRYPT\_MESSAGE\_PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_decrypt_message_para).</span></span>

 

 



