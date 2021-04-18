---
description: Explica o procedimento usado para armazenar uma chave de sessão.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Armazenando uma chave de sessão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789490"
---
# <a name="storing-a-session-key"></a><span data-ttu-id="fa82c-103">Armazenando uma chave de sessão</span><span class="sxs-lookup"><span data-stu-id="fa82c-103">Storing a Session Key</span></span>

> [!Note]  
> <span data-ttu-id="fa82c-104">Esta seção pressupõe que os usuários possuam um conjunto de [*pares de chaves públicas/privadas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fa82c-104">This section assumes that users possess a set of [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="fa82c-105">As instruções e um exemplo para a criação de pares de chaves podem ser encontrados no [programa C de exemplo: Criando um contêiner de chave e gerando chaves](example-c-program-creating-a-key-container-and-generating-keys.md).</span><span class="sxs-lookup"><span data-stu-id="fa82c-105">Instructions and an example for creating key pairs can be found in [Example C Program: Creating a Key Container and Generating Keys](example-c-program-creating-a-key-container-and-generating-keys.md).</span></span>

 

<span data-ttu-id="fa82c-106">**Para armazenar uma chave de sessão**</span><span class="sxs-lookup"><span data-stu-id="fa82c-106">**To store a session key**</span></span>

1.  <span data-ttu-id="fa82c-107">Crie um [*blob de chave*](../secgloss/k-gly.md) simples usando a função [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) .</span><span class="sxs-lookup"><span data-stu-id="fa82c-107">Create a simple [*key BLOB*](../secgloss/k-gly.md) by using the [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) function.</span></span> <span data-ttu-id="fa82c-108">Isso transferirá a chave de sessão do CSP para o espaço de memória de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fa82c-108">This will transfer the session key from the CSP to an application's memory space.</span></span> <span data-ttu-id="fa82c-109">Especifique que uma chave pública do Exchange seja usada para assinar o BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="fa82c-109">Specify that an exchange public key be used to sign the key BLOB.</span></span>
2.  <span data-ttu-id="fa82c-110">Armazene o BLOB de chave assinado em disco.</span><span class="sxs-lookup"><span data-stu-id="fa82c-110">Store the signed key BLOB to disk.</span></span> <span data-ttu-id="fa82c-111">Supõe-se que todos os discos não sejam seguros.</span><span class="sxs-lookup"><span data-stu-id="fa82c-111">It is assumed that all disks are nonsecure.</span></span>
3.  <span data-ttu-id="fa82c-112">Quando a chave for necessária, leia o BLOB de chave do disco.</span><span class="sxs-lookup"><span data-stu-id="fa82c-112">When the key is needed, read the key BLOB from disk.</span></span>
4.  <span data-ttu-id="fa82c-113">Importe o BLOB de chave de volta para o CSP usando a função [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .</span><span class="sxs-lookup"><span data-stu-id="fa82c-113">Import the key BLOB back into the CSP by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function.</span></span>

<span data-ttu-id="fa82c-114">Para obter um exemplo de como criar uma [*chave de sessão*](../secgloss/s-gly.md) e exportar essa chave para um [*blob de chave simples*](../secgloss/s-gly.md) que pode ser gravado em um arquivo de disco, consulte [o programa de exemplo C: exportando uma chave de sessão](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="fa82c-114">For an example of creating a [*session key*](../secgloss/s-gly.md) and exporting that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

<span data-ttu-id="fa82c-115">Este procedimento fornece apenas a segurança mínima.</span><span class="sxs-lookup"><span data-stu-id="fa82c-115">This procedure provides only minimal security.</span></span> <span data-ttu-id="fa82c-116">Se a chave de sessão armazenada for usada para criptografar dados em uma data posterior, o procedimento anterior não fornecerá segurança adequada.</span><span class="sxs-lookup"><span data-stu-id="fa82c-116">If the stored session key will be used to encrypt data at a later date, the preceding procedure does not provide adequate security.</span></span>

<span data-ttu-id="fa82c-117">Para fornecer maior segurança, assine o BLOB de chave com uma chave privada do Exchange antes de armazená-lo no disco.</span><span class="sxs-lookup"><span data-stu-id="fa82c-117">To provide greater security, sign the key BLOB with an exchange private key before it is stored to disk.</span></span> <span data-ttu-id="fa82c-118">Quando o BLOB de chave é lido posteriormente do disco, sua assinatura pode ser validada para garantir que o BLOB de chave esteja intacto.</span><span class="sxs-lookup"><span data-stu-id="fa82c-118">When the key BLOB is later read from disk, its signature can be validated to ensure that the key BLOB is intact.</span></span>

<span data-ttu-id="fa82c-119">Se o BLOB de chave não for assinado, qualquer pessoa com acesso ao disco ou outra mídia na qual a chave é armazenada poderá criar uma nova chave de sessão.</span><span class="sxs-lookup"><span data-stu-id="fa82c-119">If the key BLOB is not signed, anyone with access to the disk or other media where the key is stored can create a new session key.</span></span>

<span data-ttu-id="fa82c-120">A nova chave de sessão pode ser criptografada com a [*chave de troca*](../secgloss/e-gly.md)de [*chave pública*](../secgloss/p-gly.md) do usuário original e essa nova chave pode ser substituída pelo original.</span><span class="sxs-lookup"><span data-stu-id="fa82c-120">The new session key can be encrypted with the original user's [*public key*](../secgloss/p-gly.md) [*exchange key*](../secgloss/e-gly.md), and this new key can be substituted for the original.</span></span> <span data-ttu-id="fa82c-121">Se o usuário utilizou inadvertidamente a chave de sessão substituída para criptografar arquivos e mensagens, o indivíduo que criou a chave substituta poderia descriptografá-los facilmente.</span><span class="sxs-lookup"><span data-stu-id="fa82c-121">If the user unknowingly used the substituted session key to encrypt files and messages, the individual who created the substitute key could easily decrypt them.</span></span>

<span data-ttu-id="fa82c-122">As assinaturas digitais são discutidas em detalhes em [hashes e assinaturas digitais](hashes-and-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="fa82c-122">Digital signatures are discussed in detail in [Hashes and Digital Signatures](hashes-and-digital-signatures.md).</span></span>

 

 
