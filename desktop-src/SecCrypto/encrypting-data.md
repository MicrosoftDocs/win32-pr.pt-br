---
description: Descreve as etapas a serem seguidas para criptografar uma mensagem com as funções de criptografia base.
ms.assetid: 34167767-96c5-4a20-b629-07e4d036b4d1
title: Criptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44db44db08268241e399107d8af4088dac3c0c2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568706"
---
# <a name="encrypting-data"></a><span data-ttu-id="5fa55-103">Criptografando dados</span><span class="sxs-lookup"><span data-stu-id="5fa55-103">Encrypting Data</span></span>

<span data-ttu-id="5fa55-104">O procedimento a seguir descreve as etapas a serem seguidas para criptografar uma mensagem com as funções de criptografia base.</span><span class="sxs-lookup"><span data-stu-id="5fa55-104">The following procedure describes steps to take to encrypt a message with the Base Cryptography Functions.</span></span> <span data-ttu-id="5fa55-105">Para criptografar mensagens usando os \# padrões PKCS 7, consulte [funções de mensagens de baixo nível](cryptography-functions.md) e [funções de mensagens simplificadas](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="5fa55-105">To encrypt messages using PKCS \#7 standards, see [Low-level Message Functions](cryptography-functions.md) and [Simplified Message Functions](cryptography-functions.md).</span></span>

<span data-ttu-id="5fa55-106">**Para criptografar uma mensagem**</span><span class="sxs-lookup"><span data-stu-id="5fa55-106">**To encrypt a message**</span></span>

1.  <span data-ttu-id="5fa55-107">Gere uma chave de sessão usando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="5fa55-107">Generate a session key by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>

    <span data-ttu-id="5fa55-108">Fazer essa chamada gera uma chave aleatória e retorna um identificador para que a chave possa ser usada para criptografar e descriptografar dados.</span><span class="sxs-lookup"><span data-stu-id="5fa55-108">Making this call generates a random key and returns a handle so the key can be used to encrypt and decrypt data.</span></span> <span data-ttu-id="5fa55-109">O algoritmo de criptografia a ser usado também é especificado neste ponto.</span><span class="sxs-lookup"><span data-stu-id="5fa55-109">The encryption algorithm to use is also specified at this point.</span></span> <span data-ttu-id="5fa55-110">Como o CryptoAPI não permite que os aplicativos usem algoritmos de chave pública para criptografar dados em massa, especifique um algoritmo simétrico como RC2 ou RC4 com a chamada [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="5fa55-110">Because CryptoAPI does not permit applications to use public key algorithms to encrypt bulk data, specify a symmetric algorithm such as RC2 or RC4 with the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) call.</span></span>

2.  <span data-ttu-id="5fa55-111">Como alternativa, use a função [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar uma senha em uma chave adequada para criptografia.</span><span class="sxs-lookup"><span data-stu-id="5fa55-111">Alternatively, use the [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) function to transform a password into a key suitable for encryption.</span></span>

    <span data-ttu-id="5fa55-112">Se um aplicativo precisar criptografar a mensagem para que qualquer pessoa com uma senha especificada possa descriptografar os dados, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) para transformar a senha em uma chave adequada para criptografia.</span><span class="sxs-lookup"><span data-stu-id="5fa55-112">If an application needs to encrypt the message so that anyone with a specified password can decrypt the data, use [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey) to transform the password into a key suitable for encryption.</span></span>

    > [!Note]  
    > <span data-ttu-id="5fa55-113">Nesse caso, essa função é chamada em vez da função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) e as chamadas [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) subsequentes não são necessárias.</span><span class="sxs-lookup"><span data-stu-id="5fa55-113">In this case, this function is called instead of the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function and the subsequent [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls are not needed.</span></span>

     

3.  <span data-ttu-id="5fa55-114">Se necessário, defina propriedades criptográficas extras da chave usando a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)</span><span class="sxs-lookup"><span data-stu-id="5fa55-114">If necessary, set extra cryptographic properties of the key by using the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) function</span></span>

    <span data-ttu-id="5fa55-115">Depois que a chave tiver sido gerada, as propriedades criptográficas adicionais da chave poderão ser definidas com a função [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam).</span><span class="sxs-lookup"><span data-stu-id="5fa55-115">After the key has been generated, extra cryptographic properties of the key can be set with the [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam)function.</span></span> <span data-ttu-id="5fa55-116">Essa função permite que seções diferentes do arquivo sejam criptografadas com diferentes Salts de chave e fornece uma maneira de alterar o modo de codificação ou o vetor de inicialização da chave.</span><span class="sxs-lookup"><span data-stu-id="5fa55-116">This function allows different sections of the file to be encrypted with different key salts and provides a way to change the cipher mode or initialization vector of the key.</span></span> <span data-ttu-id="5fa55-117">Esses parâmetros podem ser usados para fazer com que a criptografia esteja em conformidade com um padrão de criptografia de dados específico.</span><span class="sxs-lookup"><span data-stu-id="5fa55-117">These parameters can be used to make the encryption conform with a particular data encryption standard.</span></span>

4.  <span data-ttu-id="5fa55-118">Criptografe os dados no arquivo com a função [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) .</span><span class="sxs-lookup"><span data-stu-id="5fa55-118">Encrypt the data in the file with the [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function.</span></span>

    <span data-ttu-id="5fa55-119">A função [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) usa a chave de sessão que foi gerada na etapa anterior e criptografa um buffer de dados.</span><span class="sxs-lookup"><span data-stu-id="5fa55-119">The [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) function takes the session key that was generated in the previous step and encrypts a buffer of data.</span></span>

    > [!Note]  
    > <span data-ttu-id="5fa55-120">À medida que os dados são criptografados, os dados podem ser ligeiramente expandidos pelo algoritmo de criptografia.</span><span class="sxs-lookup"><span data-stu-id="5fa55-120">As the data is encrypted, the data may be slightly expanded by the encryption algorithm.</span></span> <span data-ttu-id="5fa55-121">O aplicativo é responsável por lembrar o comprimento dos dados criptografados para que o comprimento correto possa ser especificado posteriormente para a função [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) .</span><span class="sxs-lookup"><span data-stu-id="5fa55-121">The application is responsible for remembering the length of the encrypted data so the proper length can later be specified for the [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) function.</span></span>

     

5.  <span data-ttu-id="5fa55-122">Opcionalmente, use a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para permitir que o usuário atual descriptografe os dados no futuro.</span><span class="sxs-lookup"><span data-stu-id="5fa55-122">Optionally, use the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function to allow the current user to decrypt the data in the future.</span></span>

    <span data-ttu-id="5fa55-123">Para permitir que o usuário atual descriptografe os dados no futuro, a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) é usada para salvar a chave de descriptografia em um formato criptografado (um blob de chave) que só pode ser descriptografada com a chave privada do usuário.</span><span class="sxs-lookup"><span data-stu-id="5fa55-123">To allow the current user to decrypt the data in the future, the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function is used to save the decryption key in an encrypted form (a key BLOB) that can only be decrypted with the user's private key.</span></span> <span data-ttu-id="5fa55-124">Essa função requer a chave pública de troca de chaves do usuário para essa finalidade, que pode ser obtida usando a função [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) .</span><span class="sxs-lookup"><span data-stu-id="5fa55-124">This function requires the user's key exchange public key for this purpose, which can be obtained by using the [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) function.</span></span> <span data-ttu-id="5fa55-125">A função **CryptExportKey** retornará um blob de chave que deve ser armazenado pelo aplicativo para uso na descriptografia do arquivo</span><span class="sxs-lookup"><span data-stu-id="5fa55-125">The **CryptExportKey** function will return a key BLOB that must be stored by the application for use in decrypting the file</span></span>

> [!Note]  
> <span data-ttu-id="5fa55-126">Se o aplicativo tiver certificados (ou chaves públicas) para outros usuários, ele poderá permitir que outros usuários descriptografem o arquivo executando chamadas [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) para cada usuário que deve receber acesso.</span><span class="sxs-lookup"><span data-stu-id="5fa55-126">If the application has certificates (or public keys) for other users, it can permit other users to decrypt the file by performing [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) calls for each user who should receive access.</span></span> <span data-ttu-id="5fa55-127">Os BLOBs de chave retornados devem ser armazenados pelo aplicativo, como na etapa 5.</span><span class="sxs-lookup"><span data-stu-id="5fa55-127">The returned key BLOBs must be stored by the application, as in step 5.</span></span>

 

## <a name="creating-an-encrypted-message"></a><span data-ttu-id="5fa55-128">Criando uma mensagem criptografada</span><span class="sxs-lookup"><span data-stu-id="5fa55-128">Creating an Encrypted Message</span></span>

<span data-ttu-id="5fa55-129">As funções de mensagens simplificadas facilitam a criptografia e a descriptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="5fa55-129">The simplified message functions make it easier to encrypt and decrypt data.</span></span> <span data-ttu-id="5fa55-130">A ilustração a seguir descreve as tarefas individuais que devem ser realizadas para criptografar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5fa55-130">The following illustration depicts the individual tasks that must be accomplished to encrypt a message.</span></span> <span data-ttu-id="5fa55-131">As etapas são descritas na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5fa55-131">The steps are described in the following list.</span></span>

![Criptografando uma mensagem](images/encmsg.png)

<span data-ttu-id="5fa55-133">**Para criptografar uma mensagem**</span><span class="sxs-lookup"><span data-stu-id="5fa55-133">**To encrypt a message**</span></span>

1.  <span data-ttu-id="5fa55-134">Obtenha um ponteiro para a mensagem de texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="5fa55-134">Get a pointer to the plaintext message.</span></span>
2.  <span data-ttu-id="5fa55-135">Gere uma chave simétrica (sessão).</span><span class="sxs-lookup"><span data-stu-id="5fa55-135">Generate a symmetric (session) key.</span></span>
3.  <span data-ttu-id="5fa55-136">Usando a chave simétrica e o algoritmo de criptografia especificado, criptografe os dados da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5fa55-136">Using the symmetric key and specified encryption algorithm, encrypt the message data.</span></span>
4.  <span data-ttu-id="5fa55-137">Abra um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="5fa55-137">Open a certificate store.</span></span>
5.  <span data-ttu-id="5fa55-138">Obtenha o certificado do destinatário.</span><span class="sxs-lookup"><span data-stu-id="5fa55-138">Get the recipient's certificate.</span></span>
6.  <span data-ttu-id="5fa55-139">Obtenha a chave pública do certificado do destinatário.</span><span class="sxs-lookup"><span data-stu-id="5fa55-139">Get the public key from the recipient's certificate.</span></span>
7.  <span data-ttu-id="5fa55-140">Usando a chave pública do destinatário, criptografe a chave simétrica.</span><span class="sxs-lookup"><span data-stu-id="5fa55-140">Using the recipient's public key, encrypt the symmetric key.</span></span>
8.  <span data-ttu-id="5fa55-141">Obtenha o identificador do destinatário do certificado do destinatário.</span><span class="sxs-lookup"><span data-stu-id="5fa55-141">Get the recipient's identifier from the recipient's certificate.</span></span>
9.  <span data-ttu-id="5fa55-142">Inclua o seguinte na mensagem digitalmente envelopada: o algoritmo de criptografia de dados, os dados criptografados, a chave simétrica criptografada e o identificador do destinatário.</span><span class="sxs-lookup"><span data-stu-id="5fa55-142">Include the following in the digitally enveloped message: the data encryption algorithm, the encrypted data, the encrypted symmetric key, and the recipient identifier.</span></span>

 

 



