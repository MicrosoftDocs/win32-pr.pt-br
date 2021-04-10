---
description: Os exemplos a seguir usam as funções de gerenciamento de arquivos.
ms.assetid: 0879898b-b661-48b3-af94-9ba24811503f
title: Usando o gerenciamento de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88838ee99dde16c5c2288c00e2e2f3b35747dae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011604"
---
# <a name="using-file-management"></a><span data-ttu-id="4cd2a-103">Usando o gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="4cd2a-103">Using File Management</span></span>

<span data-ttu-id="4cd2a-104">Os exemplos a seguir usam as funções de gerenciamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-104">The following samples use the file management functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4cd2a-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="4cd2a-105">In this section</span></span>



| <span data-ttu-id="4cd2a-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="4cd2a-106">Topic</span></span>                                                                                                   | <span data-ttu-id="4cd2a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cd2a-107">Description</span></span>                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cd2a-108">Adicionando usuários a um arquivo criptografado</span><span class="sxs-lookup"><span data-stu-id="4cd2a-108">Adding Users to an Encrypted File</span></span>](adding-users-to-an-encrypted-file.md)<br/>                   | <span data-ttu-id="4cd2a-109">Código de exemplo que mostra como adicionar um novo usuário a um arquivo criptografado existente usando a função [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) .</span><span class="sxs-lookup"><span data-stu-id="4cd2a-109">Example code that shows how to add a new user to an existing encrypted file by using the [**AddUsersToEncryptedFile**](/windows/desktop/api/Winefs/nf-winefs-adduserstoencryptedfile) function.</span></span><br/>                         |
| [<span data-ttu-id="4cd2a-110">Anexando um arquivo a outro arquivo</span><span class="sxs-lookup"><span data-stu-id="4cd2a-110">Appending One File to Another File</span></span>](appending-one-file-to-another-file.md)<br/>                 | <span data-ttu-id="4cd2a-111">Código de exemplo que mostra como um aplicativo pode acrescentar um arquivo ao final de outro arquivo, incluindo como abrir e fechar arquivos, ler e gravar em arquivos, e bloquear e desbloquear arquivos.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-111">Example code that shows how an application can append one file to the end of another file, including how to open and close files, read and write to files, and lock and unlock files.</span></span><br/> |
| [<span data-ttu-id="4cd2a-112">Criando e usando um arquivo temporário</span><span class="sxs-lookup"><span data-stu-id="4cd2a-112">Creating and Using a Temporary File</span></span>](creating-and-using-a-temporary-file.md)<br/>               | <span data-ttu-id="4cd2a-113">Código de exemplo que mostra como criar um arquivo temporário para fins de manipulação de dados usando as funções GetTempFileName e GetTempPath.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-113">Example code that shows how to create a temporary file for data manipulation purposes by using the GetTempFileName and GetTempPath functions.</span></span><br/>                                         |
| [<span data-ttu-id="4cd2a-114">Bloqueio e desbloqueio de intervalos de bytes em arquivos</span><span class="sxs-lookup"><span data-stu-id="4cd2a-114">Locking and Unlocking Byte Ranges in Files</span></span>](locking-and-unlocking-byte-ranges-in-files.md)<br/> | <span data-ttu-id="4cd2a-115">Código de exemplo que mostra o bloqueio de intervalo de bytes e o desbloqueio usando as funções LockFileEx e UnlockFileEx.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-115">Example code that shows byte range locking and unlocking by using the LockFileEx and UnlockFileEx functions.</span></span><br/>                                                                          |
| [<span data-ttu-id="4cd2a-116">Abrir um arquivo para leitura ou gravação</span><span class="sxs-lookup"><span data-stu-id="4cd2a-116">Opening a File for Reading or Writing</span></span>](opening-a-file-for-reading-or-writing.md)<br/>           | <span data-ttu-id="4cd2a-117">Código de exemplo que mostra como usar a função CreateFile para criar um novo arquivo ou abrir um arquivo existente.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-117">Example code that shows how to use the CreateFile function to create a new file or open an existing file.</span></span><br/>                                                                             |
| [<span data-ttu-id="4cd2a-118">Recuperando e alterando atributos de arquivo</span><span class="sxs-lookup"><span data-stu-id="4cd2a-118">Retrieving and Changing File Attributes</span></span>](retrieving-and-changing-file-attributes.md)<br/>       | <span data-ttu-id="4cd2a-119">Código de exemplo que mostra como usar a função GetFileAttributesEx para recuperar atributos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-119">Example code that shows how to use the GetFileAttributesEx function to retrieve file attributes.</span></span><br/>                                                                                      |
| [<span data-ttu-id="4cd2a-120">Teste para o final de um arquivo</span><span class="sxs-lookup"><span data-stu-id="4cd2a-120">Testing for the End of a File</span></span>](testing-for-the-end-of-a-file.md)<br/>                           | <span data-ttu-id="4cd2a-121">Código de exemplo que mostra como testar o fim do arquivo durante uma operação de leitura síncrona e durante uma operação de leitura assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-121">Example code that shows how to test for the end of file during a synchronous read operation and during an asynchronous read operation.</span></span><br/>                                                |
| [<span data-ttu-id="4cd2a-122">Usando fluxos</span><span class="sxs-lookup"><span data-stu-id="4cd2a-122">Using Streams</span></span>](using-streams.md)<br/>                                                           | <span data-ttu-id="4cd2a-123">Código de exemplo que mostra como usar fluxos básicos do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="4cd2a-123">Example code that shows how to use basic NTFS file system streams.</span></span><br/>                                                                                                                    |



 

 

 




