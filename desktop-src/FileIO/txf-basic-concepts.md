---
description: Descreve a consistência de leitura confirmada, isolamento de confirmação de leitura e conceitos de bloqueio transacional em NTFS Transacional.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Conceitos básicos do TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297213"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="898a4-103">Conceitos básicos do TxF</span><span class="sxs-lookup"><span data-stu-id="898a4-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="898a4-104">Isolamento de leitura</span><span class="sxs-lookup"><span data-stu-id="898a4-104">Read Isolation</span></span>

<span data-ttu-id="898a4-105">O NTFS Transacional (TxF) fornece consistência de leitura confirmada.</span><span class="sxs-lookup"><span data-stu-id="898a4-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="898a4-106">Um [*gravador transacionado*](glossary.md) refere-se a um identificador de arquivo transacionado aberto com qualquer permissão que não faça parte do acesso de leitura genérico, mas que faz parte do acesso de gravação genérico.</span><span class="sxs-lookup"><span data-stu-id="898a4-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="898a4-107">Um *gravador transacionado* exibe a versão mais recente de um arquivo que inclui todas as alterações feitas pela mesma transação.</span><span class="sxs-lookup"><span data-stu-id="898a4-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="898a4-108">Pode haver apenas um gravador transacionado por arquivo.</span><span class="sxs-lookup"><span data-stu-id="898a4-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="898a4-109">Os gravadores não transacionais sempre são bloqueados por um gravador transacionado, mesmo que o arquivo seja aberto com permissões de gravação compartilhada.</span><span class="sxs-lookup"><span data-stu-id="898a4-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="898a4-110">Um [*leitor transacionado*](glossary.md) refere-se a um identificador de arquivo transacionado aberto com qualquer permissão que faça parte do acesso de leitura genérico, mas que não faz parte do acesso de gravação genérico.</span><span class="sxs-lookup"><span data-stu-id="898a4-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="898a4-111">Um *leitor transacionado* exibe uma versão confirmada do arquivo que existia no momento em que o identificador de arquivo foi aberto.</span><span class="sxs-lookup"><span data-stu-id="898a4-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="898a4-112">O leitor transacionado é isolado dos efeitos dos gravadores transacionados.</span><span class="sxs-lookup"><span data-stu-id="898a4-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="898a4-113">Isso fornece uma exibição consistente do arquivo apenas para a vida útil do identificador de arquivo e bloqueia gravadores não transacionados.</span><span class="sxs-lookup"><span data-stu-id="898a4-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="898a4-114">Quando um identificador é aberto para modificação com a função [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , todas as aberturas subsequentes do arquivo nessa transação se aplicam somente leitura ou não são convertidas pelo sistema para serem um gravador transacionado para fins de isolamento e outras semânticas transacionais.</span><span class="sxs-lookup"><span data-stu-id="898a4-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="898a4-115">Isso significa que, subsequentemente, quando um identificador é aberto para acesso somente leitura, o identificador não recebe uma exibição do arquivo antes do início da transação; Ele recebe a exibição da transação ativa do arquivo.</span><span class="sxs-lookup"><span data-stu-id="898a4-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="898a4-116">Um identificador de arquivo não transacionado não verá nenhuma alteração feita dentro de uma transação até que a transação seja confirmada.</span><span class="sxs-lookup"><span data-stu-id="898a4-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="898a4-117">O identificador de arquivo não transacionado recebe uma exibição isolada que é semelhante a um leitor transacionado, mas ao contrário de um leitor transacionado, ele recebe a atualização do arquivo quando um gravador transacionado confirma a transação.</span><span class="sxs-lookup"><span data-stu-id="898a4-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="898a4-118">Níveis de isolamento</span><span class="sxs-lookup"><span data-stu-id="898a4-118">Isolation Levels</span></span>

<span data-ttu-id="898a4-119">O TxF fornece isolamento de leitura confirmada.</span><span class="sxs-lookup"><span data-stu-id="898a4-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="898a4-120">Isso significa que as atualizações de arquivo não são vistas fora da transação.</span><span class="sxs-lookup"><span data-stu-id="898a4-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="898a4-121">Além disso, se um arquivo for aberto mais de uma vez durante a leitura de arquivos na transação, você poderá ver resultados diferentes com cada abertura subsequente.</span><span class="sxs-lookup"><span data-stu-id="898a4-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="898a4-122">Os arquivos que estavam disponíveis na primeira vez que você os acessou podem não estar disponíveis (porque foram excluídos) ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="898a4-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="898a4-123">Bloqueio transacional</span><span class="sxs-lookup"><span data-stu-id="898a4-123">Transactional Locking</span></span>

<span data-ttu-id="898a4-124">A criação de um gravador transacionado em um arquivo *bloqueia transacionalmente* o arquivo.</span><span class="sxs-lookup"><span data-stu-id="898a4-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="898a4-125">Depois que um arquivo é bloqueado por uma transação, outras operações do sistema de arquivos externas à transação de bloqueio que tentam modificar o arquivo bloqueado de forma transacional falharão com a **\_ \_ violação de compartilhamento de erro** ou com o erro de **\_ \_ conflito transacional**.</span><span class="sxs-lookup"><span data-stu-id="898a4-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="898a4-126">A tabela a seguir resume o bloqueio transacional.</span><span class="sxs-lookup"><span data-stu-id="898a4-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="898a4-127">Arquivo aberto atualmente por</span><span class="sxs-lookup"><span data-stu-id="898a4-127">File currently opened by</span></span>

<span data-ttu-id="898a4-128">Tentativa de abertura de arquivo por</span><span class="sxs-lookup"><span data-stu-id="898a4-128">File open attempted by</span></span>

<span data-ttu-id="898a4-129">Transacionado</span><span class="sxs-lookup"><span data-stu-id="898a4-129">Transacted</span></span>

<span data-ttu-id="898a4-130">Não transacionado</span><span class="sxs-lookup"><span data-stu-id="898a4-130">Non-Transacted</span></span>

<span data-ttu-id="898a4-131">Leitor</span><span class="sxs-lookup"><span data-stu-id="898a4-131">Reader</span></span>

<span data-ttu-id="898a4-132">Leitor/gravador</span><span class="sxs-lookup"><span data-stu-id="898a4-132">Reader/Writer</span></span>

<span data-ttu-id="898a4-133">Leitor</span><span class="sxs-lookup"><span data-stu-id="898a4-133">Reader</span></span>

<span data-ttu-id="898a4-134">Leitor/gravador</span><span class="sxs-lookup"><span data-stu-id="898a4-134">Reader/Writer</span></span>

<span data-ttu-id="898a4-135">Leitor transacionado</span><span class="sxs-lookup"><span data-stu-id="898a4-135">Transacted Reader</span></span>

<span data-ttu-id="898a4-136">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-136">Yes</span></span>

<span data-ttu-id="898a4-137">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-137">Yes</span></span>

<span data-ttu-id="898a4-138">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-138">Yes</span></span>

<span data-ttu-id="898a4-139">Não2</span><span class="sxs-lookup"><span data-stu-id="898a4-139">No2</span></span>

<span data-ttu-id="898a4-140">Leitor/gravador transacionado</span><span class="sxs-lookup"><span data-stu-id="898a4-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="898a4-141">Yes</span><span class="sxs-lookup"><span data-stu-id="898a4-141">Yes</span></span>

<span data-ttu-id="898a4-142">Não2</span><span class="sxs-lookup"><span data-stu-id="898a4-142">No2</span></span>

<span data-ttu-id="898a4-143">Yes</span><span class="sxs-lookup"><span data-stu-id="898a4-143">Yes</span></span>

<span data-ttu-id="898a4-144">Não2</span><span class="sxs-lookup"><span data-stu-id="898a4-144">No2</span></span>

<span data-ttu-id="898a4-145">Leitor não transacionado</span><span class="sxs-lookup"><span data-stu-id="898a4-145">Non-Transacted Reader</span></span>

<span data-ttu-id="898a4-146">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-146">Yes</span></span>

<span data-ttu-id="898a4-147">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-147">Yes</span></span>

<span data-ttu-id="898a4-148">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-148">Yes</span></span>

<span data-ttu-id="898a4-149">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-149">Yes</span></span>

<span data-ttu-id="898a4-150">Leitor/gravador não transacionado</span><span class="sxs-lookup"><span data-stu-id="898a4-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="898a4-151">Nº 1</span><span class="sxs-lookup"><span data-stu-id="898a4-151">No1</span></span>

<span data-ttu-id="898a4-152">Nº 1</span><span class="sxs-lookup"><span data-stu-id="898a4-152">No1</span></span>

<span data-ttu-id="898a4-153">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-153">Yes</span></span>

<span data-ttu-id="898a4-154">Sim</span><span class="sxs-lookup"><span data-stu-id="898a4-154">Yes</span></span>

1. <span data-ttu-id="898a4-155">Falha com **erro de \_ \_ conflito transacional**</span><span class="sxs-lookup"><span data-stu-id="898a4-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="898a4-156">2. falha com **\_ \_ violação de compartilhamento de erro**</span><span class="sxs-lookup"><span data-stu-id="898a4-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="898a4-157">Se você abrir um fluxo nomeado para uma modificação que esteja usando uma transação, o arquivo inteiro será necessário para ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="898a4-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="898a4-158">Além do bloqueio transacional, as regras de compartilhamento de arquivos NTFS típicas se aplicam.</span><span class="sxs-lookup"><span data-stu-id="898a4-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="898a4-159">Você precisa considerar os dois modos de compartilhamento de arquivos a seguir em paralelo:</span><span class="sxs-lookup"><span data-stu-id="898a4-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="898a4-160">O modo de bloqueio transacional.</span><span class="sxs-lookup"><span data-stu-id="898a4-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="898a4-161">Modos normais de compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="898a4-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="898a4-162">O modo mais restritivo é aquele que se aplica.</span><span class="sxs-lookup"><span data-stu-id="898a4-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 




