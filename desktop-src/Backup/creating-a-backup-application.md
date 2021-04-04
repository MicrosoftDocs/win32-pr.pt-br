---
title: Criando um aplicativo de backup
description: Para executar a entrada ou saída em uma fita, um aplicativo de backup deve primeiro obter um identificador do dispositivo de fita. O exemplo de código a seguir mostra como usar a função CreateFile para abrir um dispositivo de fita.
ms.assetid: a2d367e1-13a9-47a8-8329-6e550c09ad58
keywords:
- Backup de aplicativos de backup
- Criando backup de aplicativos de backup
- Backup de backup, criando aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77409a0c74ee61e333b92dad8b22d9c68ed92eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007918"
---
# <a name="creating-a-backup-application"></a><span data-ttu-id="373d1-107">Criando um aplicativo de backup</span><span class="sxs-lookup"><span data-stu-id="373d1-107">Creating a Backup Application</span></span>

<span data-ttu-id="373d1-108">Para executar a entrada ou saída em uma fita, um aplicativo de backup deve primeiro obter um identificador do dispositivo de fita.</span><span class="sxs-lookup"><span data-stu-id="373d1-108">To perform input or output on a tape, a backup application must first obtain a handle of the tape device.</span></span> <span data-ttu-id="373d1-109">O exemplo de código a seguir mostra como usar a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um dispositivo de fita.</span><span class="sxs-lookup"><span data-stu-id="373d1-109">The following code sample shows you how to use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a tape device.</span></span>


```C++
HANDLE hTape;   // handle to tape device
 
hTape = CreateFile(TEXT("\\\\.\\TAPE0"),         // tape dev to open
                   GENERIC_READ | GENERIC_WRITE, // read/write access
                   0,                            // not used
                   0,                            // not used
                   OPEN_EXISTING,                // req for tape devs
                   0,                            // not used
                   NULL);                        // not used
```



<span data-ttu-id="373d1-110">Para fazer backup de uma árvore de diretórios em uma fita, um aplicativo deve usar as funções [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) e [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) para atravessar a árvore de diretórios.</span><span class="sxs-lookup"><span data-stu-id="373d1-110">To back up a directory tree to a tape, an application must use the [**FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/fileapi/nf-fileapi-findnextfilea) functions to traverse the directory tree.</span></span> <span data-ttu-id="373d1-111">Cada vez que um arquivo é encontrado, o aplicativo deve obter os atributos do arquivo usando a função [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="373d1-111">Each time a file is found, the application should get the file attributes by using the [**GetFileAttributes**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) function.</span></span>

<span data-ttu-id="373d1-112">Se houver links físicos, um aplicativo deverá determinar o número de links e salvar o identificador exclusivo do arquivo em uma tabela para comparações futuras.</span><span class="sxs-lookup"><span data-stu-id="373d1-112">If there are hard links, an application should determine the number of links, and save the unique identifier of the file in a table for future comparisons.</span></span> <span data-ttu-id="373d1-113">Na primeira vez em que um arquivo é encontrado, o aplicativo deve usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir o arquivo e a função [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) para iniciar o backup.</span><span class="sxs-lookup"><span data-stu-id="373d1-113">The first time a file is found, the application should use [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open the file, and the [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) function to begin the backup.</span></span> <span data-ttu-id="373d1-114">Em seguida, ele pode usar a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) repetidamente para transferir todas as informações no buffer usado pelo **BackupRead** para a fita.</span><span class="sxs-lookup"><span data-stu-id="373d1-114">Then it can use the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function repeatedly to transfer all the information in the buffer used by **BackupRead** to the tape.</span></span> <span data-ttu-id="373d1-115">Na segunda vez que um arquivo é encontrado (verificado em relação à tabela de identificadores de arquivo quando há links físicos), o aplicativo pode gravar as informações gerais do arquivo na fita, seguido por um fluxo que tem um identificador que é um **\_ link de backup**.</span><span class="sxs-lookup"><span data-stu-id="373d1-115">The second time a file is found (checked against the table of file identifiers when there are hard links), the application can write the general file information to the tape, followed by a stream that has an identifier that is **BACKUP\_LINK**.</span></span>

<span data-ttu-id="373d1-116">Ao restaurar arquivos de fita para disco, um aplicativo deve usar as funções [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)e [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) .</span><span class="sxs-lookup"><span data-stu-id="373d1-116">When restoring files from tape to disk, an application must use the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite), and [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) functions.</span></span> <span data-ttu-id="373d1-117">Para cada arquivo em uma fita, o aplicativo deve usar **CreateFile** para criar um novo arquivo em disco e **BackupWrite** para começar a restaurar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="373d1-117">For each file on a tape, the application should use **CreateFile** to create a new file on disk, and **BackupWrite** to begin restoring the file.</span></span> <span data-ttu-id="373d1-118">Em seguida, o aplicativo deve usar **ReadFile** repetidamente até que todas as informações do arquivo sejam lidas da fita no buffer preenchido por **BackupWrite**.</span><span class="sxs-lookup"><span data-stu-id="373d1-118">Then the application should use **ReadFile** repeatedly until all the information for the file is read from the tape into the buffer filled by **BackupWrite**.</span></span>

<span data-ttu-id="373d1-119">Se um dos fluxos no buffer [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) tiver um identificador de fluxo de **\_ link de backup** , o aplicativo deverá estabelecer um vínculo físico.</span><span class="sxs-lookup"><span data-stu-id="373d1-119">If one of the streams in the [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) buffer has a **BACKUP\_LINK** stream identifier, the application must establish a hard link.</span></span> <span data-ttu-id="373d1-120">Se os dados necessários para estabelecer o link não existirem, o **BackupWrite** falhará.</span><span class="sxs-lookup"><span data-stu-id="373d1-120">If the data needed to establish the link does not exist, **BackupWrite** fails.</span></span> <span data-ttu-id="373d1-121">O aplicativo pode usar um catálogo pré-existente para localizar e restaurar os dados originais, ou pode notificar o usuário de que os dados de arquivo a serem restaurados estão em um local diferente.</span><span class="sxs-lookup"><span data-stu-id="373d1-121">The application can use a pre-existing catalog to locate and restore the original data, or it can notify the user that the file data to be restored is in a different location.</span></span>

 

 