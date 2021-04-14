---
description: Mostra como enviar uma mensagem criptografada.
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: Troca manual de chaves de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0114f8173084126a72519d291158f15f3e1c171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552951"
---
# <a name="manual-session-key-exchanges"></a><span data-ttu-id="9db07-103">Troca manual de chaves de sessão</span><span class="sxs-lookup"><span data-stu-id="9db07-103">Manual Session Key Exchanges</span></span>

> [!Note]  
> <span data-ttu-id="9db07-104">O procedimento descrito nesta seção pressupõe que os usuários (ou clientes CryptoAPI) já possuem seu próprio conjunto de [*pares de chaves públicas/privadas*](../secgloss/p-gly.md) e também obteram [*as chaves públicas*](../secgloss/p-gly.md)de cada um deles.</span><span class="sxs-lookup"><span data-stu-id="9db07-104">The procedure described in this section assumes that the users (or CryptoAPI clients) already possess their own set of [*public/private key pairs*](../secgloss/p-gly.md) and have also obtained each other's [*public keys*](../secgloss/p-gly.md).</span></span>

 

<span data-ttu-id="9db07-105">A ilustração a seguir mostra como usar esse procedimento para enviar uma mensagem criptografada.</span><span class="sxs-lookup"><span data-stu-id="9db07-105">The following illustration shows how to use this procedure to send an encrypted message.</span></span>

![enviando uma mensagem criptografada](images/capi04.png)

<span data-ttu-id="9db07-107">Essa abordagem é vulnerável a pelo menos uma forma comum de ataque.</span><span class="sxs-lookup"><span data-stu-id="9db07-107">This approach is vulnerable to at least one common form of attack.</span></span> <span data-ttu-id="9db07-108">Um bisbilhoteiro pode adquirir cópias de uma ou mais mensagens criptografadas e as chaves criptografadas.</span><span class="sxs-lookup"><span data-stu-id="9db07-108">An eavesdropper can acquire copies of one or more encrypted messages and the encrypted keys.</span></span> <span data-ttu-id="9db07-109">Em seguida, em algum momento posterior, o bisbilhoteiro pode enviar uma dessas mensagens para o receptor e o receptor não terá como saber que a mensagem não foi proveniente diretamente do remetente original.</span><span class="sxs-lookup"><span data-stu-id="9db07-109">Then, at some later time, the eavesdropper can send one of these messages to the receiver and the receiver will have no way of knowing the message did not come directly from the original sender.</span></span> <span data-ttu-id="9db07-110">Esse risco pode ser reduzido pelo carimbo de data/hora de todas as mensagens ou por meio de números de série.</span><span class="sxs-lookup"><span data-stu-id="9db07-110">This risk can be reduced by time-stamping all messages or by using serial numbers.</span></span>

<span data-ttu-id="9db07-111">A maneira mais fácil de enviar mensagens criptografadas para outro usuário é enviar a mensagem criptografada com uma chave de sessão aleatória junto com a chave de sessão criptografada com a chave [*pública de troca de chaves*](../secgloss/k-gly.md)do destinatário.</span><span class="sxs-lookup"><span data-stu-id="9db07-111">The easiest way to send encrypted messages to another user is to send the message encrypted with a random session key along with the session key encrypted with the receiver's [*key exchange public key*](../secgloss/k-gly.md).</span></span>

<span data-ttu-id="9db07-112">A seguir estão as etapas para enviar uma chave de sessão criptografada.</span><span class="sxs-lookup"><span data-stu-id="9db07-112">Following are the steps for sending an encrypted session key.</span></span>

<span data-ttu-id="9db07-113">**Para enviar uma chave de sessão criptografada**</span><span class="sxs-lookup"><span data-stu-id="9db07-113">**To send an encrypted session key**</span></span>

1.  <span data-ttu-id="9db07-114">Crie uma [*chave de sessão*](../secgloss/s-gly.md) aleatória usando a função [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) .</span><span class="sxs-lookup"><span data-stu-id="9db07-114">Create a random [*session key*](../secgloss/s-gly.md) by using the [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) function.</span></span>
2.  <span data-ttu-id="9db07-115">Criptografe a mensagem usando a chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="9db07-115">Encrypt the message by using the session key.</span></span> <span data-ttu-id="9db07-116">Esse procedimento é discutido em [criptografia e](data-encryption-and-decryption.md)descriptografia de dados.</span><span class="sxs-lookup"><span data-stu-id="9db07-116">This procedure is discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>
3.  <span data-ttu-id="9db07-117">Exporte a chave de sessão para um [*blob de chave*](../secgloss/k-gly.md) com a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) , especificando que a chave seja criptografada com a chave pública de troca de chaves do usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="9db07-117">Export the session key into a [*key BLOB*](../secgloss/k-gly.md) with the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function, specifying that the key be encrypted with the destination user's key exchange public key.</span></span>
4.  <span data-ttu-id="9db07-118">Envie a mensagem criptografada e o BLOB de chave criptografada para o usuário de destino.</span><span class="sxs-lookup"><span data-stu-id="9db07-118">Send both the encrypted message and the encrypted key BLOB to the destination user.</span></span>
5.  <span data-ttu-id="9db07-119">O usuário de destino importa o BLOB de chave para seu CSP usando a função [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="9db07-119">The destination user imports the key BLOB into his or her CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span> <span data-ttu-id="9db07-120">Isso descriptografará automaticamente a chave de sessão, desde que a chave pública de troca de chaves do usuário de destino tenha sido especificada na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="9db07-120">This will automatically decrypt the session key, provided the destination user's key exchange public key was specified in step 3.</span></span>
6.  <span data-ttu-id="9db07-121">O usuário de destino pode então descriptografar a mensagem usando a chave de sessão, seguindo o procedimento discutido em [criptografia e descriptografia de dados](data-encryption-and-decryption.md).</span><span class="sxs-lookup"><span data-stu-id="9db07-121">The destination user can then decrypt the message by using the session key, following the procedure discussed in [Data Encryption and Decryption](data-encryption-and-decryption.md).</span></span>

 

 
