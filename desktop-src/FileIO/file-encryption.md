---
description: O EFS (sistema de arquivos criptografados) fornece proteção criptográfica de arquivos individuais em volumes do sistema de arquivos NTFS usando um sistema de chave pública.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Criptografia de Arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770234"
---
# <a name="file-encryption"></a><span data-ttu-id="eae0d-103">Criptografia de Arquivo</span><span class="sxs-lookup"><span data-stu-id="eae0d-103">File Encryption</span></span>

<span data-ttu-id="eae0d-104">O sistema de arquivos criptografados, ou EFS, fornece um nível adicional de segurança para arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="eae0d-104">The Encrypted File System, or EFS, provides an additional level of security for files and directories.</span></span> <span data-ttu-id="eae0d-105">Ele fornece proteção criptográfica de arquivos individuais em volumes do sistema de arquivos NTFS usando um sistema de chave pública.</span><span class="sxs-lookup"><span data-stu-id="eae0d-105">It provides cryptographic protection of individual files on NTFS file system volumes using a public-key system.</span></span>

<span data-ttu-id="eae0d-106">Normalmente, o controle de acesso aos objetos de arquivo e diretório fornecidos pelo modelo de segurança do Windows é suficiente para proteger o acesso não autorizado a informações confidenciais.</span><span class="sxs-lookup"><span data-stu-id="eae0d-106">Typically, the access control to file and directory objects provided by the Windows security model is sufficient to protect unauthorized access to sensitive information.</span></span> <span data-ttu-id="eae0d-107">No entanto, se um laptop que contém dados confidenciais for perdido ou roubado, a proteção de segurança desses dados poderá ser comprometida.</span><span class="sxs-lookup"><span data-stu-id="eae0d-107">However, if a laptop that contains sensitive data is lost or stolen, the security protection of that data may be compromised.</span></span> <span data-ttu-id="eae0d-108">A criptografia dos arquivos aumenta a segurança.</span><span class="sxs-lookup"><span data-stu-id="eae0d-108">Encrypting the files increases security.</span></span>

<span data-ttu-id="eae0d-109">Para determinar se um sistema de arquivos dá suporte à criptografia de arquivo para arquivos e diretórios, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine o sinalizador de bit de **\_ \_ criptografia de arquivo FS** .</span><span class="sxs-lookup"><span data-stu-id="eae0d-109">To determine whether a file system supports file encryption for files and directories, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FS\_FILE\_ENCRYPTION** bit flag.</span></span> <span data-ttu-id="eae0d-110">Observe que os seguintes itens não podem ser criptografados:</span><span class="sxs-lookup"><span data-stu-id="eae0d-110">Note that the following items cannot be encrypted:</span></span>

-   <span data-ttu-id="eae0d-111">Arquivos compactados</span><span class="sxs-lookup"><span data-stu-id="eae0d-111">Compressed files</span></span>
-   <span data-ttu-id="eae0d-112">Arquivos do sistema</span><span class="sxs-lookup"><span data-stu-id="eae0d-112">System files</span></span>
-   <span data-ttu-id="eae0d-113">Diretórios do sistema</span><span class="sxs-lookup"><span data-stu-id="eae0d-113">System directories</span></span>
-   <span data-ttu-id="eae0d-114">Diretórios raiz</span><span class="sxs-lookup"><span data-stu-id="eae0d-114">Root directories</span></span>
-   <span data-ttu-id="eae0d-115">Transactions</span><span class="sxs-lookup"><span data-stu-id="eae0d-115">Transactions</span></span>

<span data-ttu-id="eae0d-116">Arquivos esparsos podem ser criptografados.</span><span class="sxs-lookup"><span data-stu-id="eae0d-116">Sparse files can be encrypted.</span></span>

<span data-ttu-id="eae0d-117">O TxF não oferece suporte à maioria das operações em arquivos EFS (sistema de arquivos criptografados).</span><span class="sxs-lookup"><span data-stu-id="eae0d-117">TxF does not support most operations on Encrypted File System (EFS) files.</span></span> <span data-ttu-id="eae0d-118">O único Operations TxF dá suporte a operações de leitura, como [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span><span class="sxs-lookup"><span data-stu-id="eae0d-118">The only operations TxF supports are read operations, such as [**ReadEncryptedFileRaw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="eae0d-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="eae0d-119">In this section</span></span>



| <span data-ttu-id="eae0d-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="eae0d-120">Topic</span></span>                                                                                               | <span data-ttu-id="eae0d-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="eae0d-121">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eae0d-122">Manipulando arquivos e diretórios criptografados</span><span class="sxs-lookup"><span data-stu-id="eae0d-122">Handling Encrypted Files and Directories</span></span>](handling-encrypted-files-and-directories.md)<br/> | <span data-ttu-id="eae0d-123">Um arquivo marcado como criptografado é criptografado pelo sistema de arquivos NTFS usando o driver de criptografia atual.</span><span class="sxs-lookup"><span data-stu-id="eae0d-123">A file marked encrypted is encrypted by the NTFS file system by using the current encryption driver.</span></span><br/>                                                          |
| [<span data-ttu-id="eae0d-124">Arquivos criptografados e chaves de usuário</span><span class="sxs-lookup"><span data-stu-id="eae0d-124">Encrypted Files and User Keys</span></span>](encrypted-files-and-user-keys.md)<br/>                       | <span data-ttu-id="eae0d-125">Lista as funções a serem usadas para criar uma nova chave, adicionar uma chave a um arquivo criptografado, consultar as chaves de um arquivo criptografado e remover chaves de um arquivo criptografado.</span><span class="sxs-lookup"><span data-stu-id="eae0d-125">Lists the functions to use to create a new key, add a key to an encrypted file, query the keys for an encrypted file, and remove keys from an encrypted file.</span></span><br/> |
| [<span data-ttu-id="eae0d-126">Backup e restauração de arquivos criptografados</span><span class="sxs-lookup"><span data-stu-id="eae0d-126">Backup and Restore of Encrypted Files</span></span>](backup-and-restore-of-encrypted-files.md)<br/>       | <span data-ttu-id="eae0d-127">As funções de criptografia brutas permitem o backup de arquivos criptografados.</span><span class="sxs-lookup"><span data-stu-id="eae0d-127">The raw encryption functions enable backup of encrypted files.</span></span><br/>                                                                                                |



 

<span data-ttu-id="eae0d-128">Para obter mais informações sobre criptografia, consulte [adicionando usuários a um arquivo criptografado](adding-users-to-an-encrypted-file.md).</span><span class="sxs-lookup"><span data-stu-id="eae0d-128">For more information about encryption, see [Adding Users to an Encrypted File](adding-users-to-an-encrypted-file.md).</span></span>

<span data-ttu-id="eae0d-129">Para obter mais informações sobre criptografia, consulte [criptografia](/windows/desktop/SecCrypto/cryptography-portal).</span><span class="sxs-lookup"><span data-stu-id="eae0d-129">For more information about cryptography, see [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).</span></span>

 

