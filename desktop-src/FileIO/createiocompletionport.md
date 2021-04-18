---
description: Cria uma porta de conclusão de entrada/saída (e/s) e a associa a um identificador de arquivo especificado ou cria uma porta de conclusão de e/s que ainda não está associada a um identificador de arquivo, permitindo a associação em um momento posterior.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Função CreateIoCompletionPort (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810921"
---
# <a name="createiocompletionport-function"></a><span data-ttu-id="3dbec-103">Função CreateIoCompletionPort</span><span class="sxs-lookup"><span data-stu-id="3dbec-103">CreateIoCompletionPort function</span></span>

<span data-ttu-id="3dbec-104">Cria uma porta de conclusão de entrada/saída (e/s) e a associa a um identificador de arquivo especificado ou cria uma porta de conclusão de e/s que ainda não está associada a um identificador de arquivo, permitindo a associação em um momento posterior.</span><span class="sxs-lookup"><span data-stu-id="3dbec-104">Creates an input/output (I/O) completion port and associates it with a specified file handle, or creates an I/O completion port that is not yet associated with a file handle, allowing association at a later time.</span></span>

<span data-ttu-id="3dbec-105">A associação de uma instância de um identificador de arquivo aberto a uma porta de conclusão de e/s permite que um processo receba notificações sobre a conclusão de operações de e/s assíncronas envolvendo esse identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-105">Associating an instance of an opened file handle with an I/O completion port allows a process to receive notification of the completion of asynchronous I/O operations involving that file handle.</span></span>

> [!Note]
>
> <span data-ttu-id="3dbec-106">O termo *identificador de arquivo* conforme usado aqui refere-se a uma abstração de sistema que representa um ponto de extremidade de e/s sobreposto, não apenas um arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="3dbec-106">The term *file handle* as used here refers to a system abstraction that represents an overlapped I/O endpoint, not only a file on disk.</span></span> <span data-ttu-id="3dbec-107">Todos os objetos do sistema que dão suporte a e/s sobreposta, como pontos de extremidade de rede, soquetes TCP, pipes nomeados e slots de email, podem ser usados como identificadores de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-107">Any system objects that support overlapped I/O such as network endpoints, TCP sockets, named pipes, and mail slots can be used as file handles.</span></span> <span data-ttu-id="3dbec-108">Para obter informações adicionais, consulte a seção comentários.</span><span class="sxs-lookup"><span data-stu-id="3dbec-108">For additional information, see the Remarks section.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3dbec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3dbec-109">Syntax</span></span>


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a><span data-ttu-id="3dbec-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dbec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dbec-111">*Identificador de fileHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3dbec-111">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbec-112">Um identificador de arquivo aberto ou um **\_ \_ valor de identificador inválido**.</span><span class="sxs-lookup"><span data-stu-id="3dbec-112">An open file handle or **INVALID\_HANDLE\_VALUE**.</span></span>

<span data-ttu-id="3dbec-113">O identificador deve ser para um objeto que dá suporte a e/s sobreposta.</span><span class="sxs-lookup"><span data-stu-id="3dbec-113">The handle must be to an object that supports overlapped I/O.</span></span>

<span data-ttu-id="3dbec-114">Se um identificador for fornecido, ele precisará ter sido aberto para a conclusão de e/s sobreposta.</span><span class="sxs-lookup"><span data-stu-id="3dbec-114">If a handle is provided, it has to have been opened for overlapped I/O completion.</span></span> <span data-ttu-id="3dbec-115">Por exemplo, você deve especificar o **sinalizador \_ \_ sobreposto do sinalizador de arquivo** ao usar a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para obter o identificador.</span><span class="sxs-lookup"><span data-stu-id="3dbec-115">For example, you must specify the **FILE\_FLAG\_OVERLAPPED** flag when using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function to obtain the handle.</span></span>

<span data-ttu-id="3dbec-116">Se **o \_ \_ valor de identificador inválido** for especificado, a função criará uma porta de conclusão de e/s sem associá-la a um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-116">If **INVALID\_HANDLE\_VALUE** is specified, the function creates an I/O completion port without associating it with a file handle.</span></span> <span data-ttu-id="3dbec-117">Nesse caso, o parâmetro *ExistingCompletionPort* deve ser **nulo** e o parâmetro *CompletionKey* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="3dbec-117">In this case, the *ExistingCompletionPort* parameter must be **NULL** and the *CompletionKey* parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3dbec-118">*ExistingCompletionPort* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3dbec-118">*ExistingCompletionPort* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbec-119">Um identificador para uma porta de conclusão de e/s existente ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3dbec-119">A handle to an existing I/O completion port or **NULL**.</span></span>

<span data-ttu-id="3dbec-120">Se esse parâmetro especificar uma porta de conclusão de e/s existente, a função a associará ao identificador especificado pelo parâmetro *fileHandle* .</span><span class="sxs-lookup"><span data-stu-id="3dbec-120">If this parameter specifies an existing I/O completion port, the function associates it with the handle specified by the *FileHandle* parameter.</span></span> <span data-ttu-id="3dbec-121">A função retorna o identificador da porta de conclusão de e/s existente, se for bem-sucedida; Ele não cria uma nova porta de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="3dbec-121">The function returns the handle of the existing I/O completion port if successful; it does not create a new I/O completion port.</span></span>

<span data-ttu-id="3dbec-122">Se esse parâmetro for **nulo**, a função criará uma nova porta de conclusão de e/s e, se o parâmetro *fileHandle* for válido, o associará à nova porta de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="3dbec-122">If this parameter is **NULL**, the function creates a new I/O completion port and, if the *FileHandle* parameter is valid, associates it with the new I/O completion port.</span></span> <span data-ttu-id="3dbec-123">Caso contrário, não ocorrerá nenhuma associação de identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-123">Otherwise no file handle association occurs.</span></span> <span data-ttu-id="3dbec-124">A função retornará o identificador para a nova porta de conclusão de e/s se for bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3dbec-124">The function returns the handle to the new I/O completion port if successful.</span></span>

</dd> <dt>

<span data-ttu-id="3dbec-125">*CompletionKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3dbec-125">*CompletionKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbec-126">A chave de conclusão por identificador definida pelo usuário que é incluída em cada pacote de conclusão de e/s para o identificador de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="3dbec-126">The per-handle user-defined completion key that is included in every I/O completion packet for the specified file handle.</span></span> <span data-ttu-id="3dbec-127">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="3dbec-127">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="3dbec-128">*NumberOfConcurrentThreads* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3dbec-128">*NumberOfConcurrentThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dbec-129">O número máximo de threads que o sistema operacional pode permitir para processar simultaneamente os pacotes de conclusão de e/s para a porta de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="3dbec-129">The maximum number of threads that the operating system can allow to concurrently process I/O completion packets for the I/O completion port.</span></span> <span data-ttu-id="3dbec-130">Esse parâmetro será ignorado se o parâmetro *ExistingCompletionPort* não for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3dbec-130">This parameter is ignored if the *ExistingCompletionPort* parameter is not **NULL**.</span></span>

<span data-ttu-id="3dbec-131">Se esse parâmetro for zero, o sistema permitirá o máximo de threads em execução simultaneamente, pois há processadores no sistema.</span><span class="sxs-lookup"><span data-stu-id="3dbec-131">If this parameter is zero, the system allows as many concurrently running threads as there are processors in the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dbec-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3dbec-132">Return value</span></span>

<span data-ttu-id="3dbec-133">Se a função for realizada com sucesso, o valor de retorno será o identificador para uma porta de conclusão de e/s:</span><span class="sxs-lookup"><span data-stu-id="3dbec-133">If the function succeeds, the return value is the handle to an I/O completion port:</span></span>

-   <span data-ttu-id="3dbec-134">Se o parâmetro *ExistingCompletionPort* era **nulo**, o valor de retorno será um novo identificador.</span><span class="sxs-lookup"><span data-stu-id="3dbec-134">If the *ExistingCompletionPort* parameter was **NULL**, the return value is a new handle.</span></span>

-   <span data-ttu-id="3dbec-135">Se o parâmetro *ExistingCompletionPort* era um identificador de porta de conclusão de e/s válido, o valor de retorno é o mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="3dbec-135">If the *ExistingCompletionPort* parameter was a valid I/O completion port handle, the return value is that same handle.</span></span>

-   <span data-ttu-id="3dbec-136">Se o parâmetro *fileHandle* era um identificador válido, esse identificador de arquivo agora está associado à porta de conclusão de e/s retornada.</span><span class="sxs-lookup"><span data-stu-id="3dbec-136">If the *FileHandle* parameter was a valid handle, that file handle is now associated with the returned I/O completion port.</span></span>

<span data-ttu-id="3dbec-137">Se a função falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3dbec-137">If the function fails, the return value is **NULL**.</span></span> <span data-ttu-id="3dbec-138">Para obter informações de erro estendidas, chame a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="3dbec-138">To get extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

## <a name="remarks"></a><span data-ttu-id="3dbec-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dbec-139">Remarks</span></span>

<span data-ttu-id="3dbec-140">O sistema de e/s pode ser instruído a enviar pacotes de notificação de conclusão de e/s para portas de conclusão de e/s, onde eles são enfileirados.</span><span class="sxs-lookup"><span data-stu-id="3dbec-140">The I/O system can be instructed to send I/O completion notification packets to I/O completion ports, where they are queued.</span></span> <span data-ttu-id="3dbec-141">A função **CreateIoCompletionPort** fornece essa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="3dbec-141">The **CreateIoCompletionPort** function provides this functionality.</span></span>

<span data-ttu-id="3dbec-142">Uma porta de conclusão de e/s e seu identificador estão associados ao processo que a criou e não podem ser compartilhadas entre os processos.</span><span class="sxs-lookup"><span data-stu-id="3dbec-142">An I/O completion port and its handle are associated with the process that created it and is not sharable between processes.</span></span> <span data-ttu-id="3dbec-143">No entanto, um único identificador é compartilhável entre threads no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-143">However, a single handle is sharable between threads in the same process.</span></span>

<span data-ttu-id="3dbec-144">**CreateIoCompletionPort** pode ser usado em três modos distintos:</span><span class="sxs-lookup"><span data-stu-id="3dbec-144">**CreateIoCompletionPort** can be used in three distinct modes:</span></span>

-   <span data-ttu-id="3dbec-145">Crie apenas uma porta de conclusão de e/s sem associá-la a um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-145">Create only an I/O completion port without associating it with a file handle.</span></span>
-   <span data-ttu-id="3dbec-146">Associe uma porta de conclusão de e/s existente a um identificador de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3dbec-146">Associate an existing I/O completion port with a file handle.</span></span>
-   <span data-ttu-id="3dbec-147">Execute a criação e a associação em uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="3dbec-147">Perform both creation and association in a single call.</span></span>

<span data-ttu-id="3dbec-148">Para criar uma porta de conclusão de e/s sem associá-la, defina o parâmetro *fileHandle* como **\_ \_ valor de identificador inválido**, o parâmetro *ExistingCompletionPort* como **NULL** e o parâmetro *CompletionKey* como zero (que é ignorado nesse caso).</span><span class="sxs-lookup"><span data-stu-id="3dbec-148">To create an I/O completion port without associating it, set the *FileHandle* parameter to **INVALID\_HANDLE\_VALUE**, the *ExistingCompletionPort* parameter to **NULL**, and the *CompletionKey* parameter to zero (which is ignored in this case).</span></span> <span data-ttu-id="3dbec-149">Defina o parâmetro *NumberOfConcurrentThreads* para o valor de simultaneidade desejado para a nova porta de conclusão de e/s ou zero para o padrão (o número de processadores no sistema).</span><span class="sxs-lookup"><span data-stu-id="3dbec-149">Set the *NumberOfConcurrentThreads* parameter to the desired concurrency value for the new I/O completion port, or zero for the default (the number of processors in the system).</span></span>

<span data-ttu-id="3dbec-150">O identificador passado no parâmetro *fileHandle* pode ser qualquer identificador que ofereça suporte a e/s sobreposta.</span><span class="sxs-lookup"><span data-stu-id="3dbec-150">The handle passed in the *FileHandle* parameter can be any handle that supports overlapped I/O.</span></span> <span data-ttu-id="3dbec-151">Normalmente, trata-se de um identificador aberto pela função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando o **sinalizador \_ \_ sobreposto do sinalizador de arquivo** (por exemplo, arquivos, slots de email e Pipes).</span><span class="sxs-lookup"><span data-stu-id="3dbec-151">Most commonly, this is a handle opened by the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function using the **FILE\_FLAG\_OVERLAPPED** flag (for example, files, mail slots, and pipes).</span></span> <span data-ttu-id="3dbec-152">Os objetos criados por outras funções, como [**soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket) , também podem ser associados a uma porta de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="3dbec-152">Objects created by other functions such as [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) can also be associated with an I/O completion port.</span></span> <span data-ttu-id="3dbec-153">Para obter um exemplo usando soquetes, consulte [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span><span class="sxs-lookup"><span data-stu-id="3dbec-153">For an example using sockets, see [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex).</span></span> <span data-ttu-id="3dbec-154">Um identificador pode ser associado a apenas uma porta de conclusão de e/s e, depois que a associação é feita, o identificador permanece associado a essa porta de conclusão de e/s até que seja fechado.</span><span class="sxs-lookup"><span data-stu-id="3dbec-154">A handle can be associated with only one I/O completion port, and after the association is made, the handle remains associated with that I/O completion port until it is closed.</span></span>

<span data-ttu-id="3dbec-155">Para obter mais informações sobre a teoria, uso e funções associadas da porta de conclusão de e/s, consulte [portas de conclusão de e/s](i-o-completion-ports.md).</span><span class="sxs-lookup"><span data-stu-id="3dbec-155">For more information on I/O completion port theory, usage, and associated functions, see [I/O Completion Ports](i-o-completion-ports.md).</span></span>

<span data-ttu-id="3dbec-156">Vários identificadores de arquivo podem ser associados a uma única porta de conclusão de e/s chamando **CreateIoCompletionPort** várias vezes com o mesmo identificador de porta de conclusão de e/s no parâmetro *ExistingCompletionPort* e um identificador de arquivo diferente no parâmetro *fileHandle* a cada vez.</span><span class="sxs-lookup"><span data-stu-id="3dbec-156">Multiple file handles can be associated with a single I/O completion port by calling **CreateIoCompletionPort** multiple times with the same I/O completion port handle in the *ExistingCompletionPort* parameter and a different file handle in the *FileHandle* parameter each time.</span></span>

<span data-ttu-id="3dbec-157">Use o parâmetro *CompletionKey* para ajudar o aplicativo a controlar quais operações de e/s foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="3dbec-157">Use the *CompletionKey* parameter to help your application track which I/O operations have completed.</span></span> <span data-ttu-id="3dbec-158">Esse valor não é usado pelo **CreateIoCompletionPort** para controle funcional; em vez disso, ele é anexado ao identificador de arquivo especificado no parâmetro *fileHandle* no momento da associação com uma porta de conclusão de e/s.</span><span class="sxs-lookup"><span data-stu-id="3dbec-158">This value is not used by **CreateIoCompletionPort** for functional control; rather, it is attached to the file handle specified in the *FileHandle* parameter at the time of association with an I/O completion port.</span></span> <span data-ttu-id="3dbec-159">Essa chave de conclusão deve ser exclusiva para cada identificador de arquivo e acompanha o identificador de arquivo em todo o processo de enfileiramento de conclusão interno.</span><span class="sxs-lookup"><span data-stu-id="3dbec-159">This completion key should be unique for each file handle, and it accompanies the file handle throughout the internal completion queuing process.</span></span> <span data-ttu-id="3dbec-160">Ele é retornado na chamada de função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) quando um pacote de conclusão chega.</span><span class="sxs-lookup"><span data-stu-id="3dbec-160">It is returned in the [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function call when a completion packet arrives.</span></span> <span data-ttu-id="3dbec-161">O parâmetro *CompletionKey* também é usado pela função [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) para enfileirar seus próprios pacotes de conclusão de finalidade especial.</span><span class="sxs-lookup"><span data-stu-id="3dbec-161">The *CompletionKey* parameter is also used by the [**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) function to queue your own special-purpose completion packets.</span></span>

<span data-ttu-id="3dbec-162">Depois que uma instância de um identificador aberto está associada a uma porta de conclusão de e/s, ela não pode ser usada na função [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) porque essas funções têm seus próprios mecanismos de e/s assíncronos.</span><span class="sxs-lookup"><span data-stu-id="3dbec-162">After an instance of an open handle is associated with an I/O completion port, it cannot be used in the [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) or [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) function because these functions have their own asynchronous I/O mechanisms.</span></span>

<span data-ttu-id="3dbec-163">É melhor não compartilhar um identificador de arquivo associado a uma porta de conclusão de e/s usando a herança de identificador ou uma chamada para a função [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) .</span><span class="sxs-lookup"><span data-stu-id="3dbec-163">It is best not to share a file handle associated with an I/O completion port by using either handle inheritance or a call to the [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) function.</span></span> <span data-ttu-id="3dbec-164">As operações executadas com esses identificadores duplicados geram notificações de conclusão.</span><span class="sxs-lookup"><span data-stu-id="3dbec-164">Operations performed with such duplicate handles generate completion notifications.</span></span> <span data-ttu-id="3dbec-165">É recomendável considerar atentamente.</span><span class="sxs-lookup"><span data-stu-id="3dbec-165">Careful consideration is advised.</span></span>

<span data-ttu-id="3dbec-166">O identificador de porta de conclusão de e/s e todos os identificadores de arquivo associados a essa porta de conclusão de e/s específica são conhecidos como *referências à porta de conclusão de e/s*.</span><span class="sxs-lookup"><span data-stu-id="3dbec-166">The I/O completion port handle and every file handle associated with that particular I/O completion port are known as *references to the I/O completion port*.</span></span> <span data-ttu-id="3dbec-167">A porta de conclusão de e/s é liberada quando não há mais referências a ela.</span><span class="sxs-lookup"><span data-stu-id="3dbec-167">The I/O completion port is released when there are no more references to it.</span></span> <span data-ttu-id="3dbec-168">Portanto, todos esses identificadores devem ser fechados corretamente para liberar a porta de conclusão de e/s e seus recursos de sistema associados.</span><span class="sxs-lookup"><span data-stu-id="3dbec-168">Therefore, all of these handles must be properly closed to release the I/O completion port and its associated system resources.</span></span> <span data-ttu-id="3dbec-169">Depois que essas condições forem satisfeitas, feche o identificador da porta de conclusão de e/s chamando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="3dbec-169">After these conditions are satisfied, close the I/O completion port handle by calling the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="3dbec-170">No Windows 8 e no Windows Server 2012, essa função é suportada pelas seguintes tecnologias.</span><span class="sxs-lookup"><span data-stu-id="3dbec-170">In Windows 8 and Windows Server 2012, this function is supported by the following technologies.</span></span>



| <span data-ttu-id="3dbec-171">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="3dbec-171">Technology</span></span>                                           | <span data-ttu-id="3dbec-172">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3dbec-172">Supported</span></span>      |
|------------------------------------------------------|----------------|
| <span data-ttu-id="3dbec-173">Protocolo SMB (Server Message Block) 3,0</span><span class="sxs-lookup"><span data-stu-id="3dbec-173">Server Message Block (SMB) 3.0 protocol</span></span><br/>   | <span data-ttu-id="3dbec-174">Yes</span><span class="sxs-lookup"><span data-stu-id="3dbec-174">Yes</span></span><br/> |
| <span data-ttu-id="3dbec-175">Failover transparente SMB 3,0 (TFO)</span><span class="sxs-lookup"><span data-stu-id="3dbec-175">SMB 3.0 Transparent Failover (TFO)</span></span><br/>        | <span data-ttu-id="3dbec-176">Yes</span><span class="sxs-lookup"><span data-stu-id="3dbec-176">Yes</span></span><br/> |
| <span data-ttu-id="3dbec-177">SMB 3,0 com compartilhamentos de arquivos de escalabilidade horizontal (SO)</span><span class="sxs-lookup"><span data-stu-id="3dbec-177">SMB 3.0 with Scale-out File Shares (SO)</span></span><br/>   | <span data-ttu-id="3dbec-178">Yes</span><span class="sxs-lookup"><span data-stu-id="3dbec-178">Yes</span></span><br/> |
| <span data-ttu-id="3dbec-179">Sistema de arquivos Volume Compartilhado Clusterizado (CsvFS)</span><span class="sxs-lookup"><span data-stu-id="3dbec-179">Cluster Shared Volume File System (CsvFS)</span></span><br/> | <span data-ttu-id="3dbec-180">Yes</span><span class="sxs-lookup"><span data-stu-id="3dbec-180">Yes</span></span><br/> |
| <span data-ttu-id="3dbec-181">ReFS (Sistema de Arquivos Resiliente)</span><span class="sxs-lookup"><span data-stu-id="3dbec-181">Resilient File System (ReFS)</span></span><br/>              | <span data-ttu-id="3dbec-182">Yes</span><span class="sxs-lookup"><span data-stu-id="3dbec-182">Yes</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3dbec-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dbec-183">Requirements</span></span>



| <span data-ttu-id="3dbec-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dbec-184">Requirement</span></span> | <span data-ttu-id="3dbec-185">Valor</span><span class="sxs-lookup"><span data-stu-id="3dbec-185">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dbec-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dbec-186">Minimum supported client</span></span><br/> | <span data-ttu-id="3dbec-187">Aplicativos de \[ aplicativos \| UWP do Windows XP desktop\]</span><span class="sxs-lookup"><span data-stu-id="3dbec-187">Windows XP \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="3dbec-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3dbec-188">Minimum supported server</span></span><br/> | <span data-ttu-id="3dbec-189">Aplicativos do Windows Server 2003 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3dbec-189">Windows Server 2003 \[desktop apps \| UWP apps\]</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="3dbec-190">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3dbec-190">Header</span></span><br/>                   | <dl> <span data-ttu-id="3dbec-191"><dt>IoAPI. h (incluir Windows. h); </dt> <dt>Winbase. h no Windows server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3dbec-191"><dt>IoAPI.h (include Windows.h); </dt> <dt>WinBase.h on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3dbec-192">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3dbec-192">Library</span></span><br/>                  | <dl> <span data-ttu-id="3dbec-193"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dbec-193"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                  |
| <span data-ttu-id="3dbec-194">DLL</span><span class="sxs-lookup"><span data-stu-id="3dbec-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dbec-195"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dbec-195"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a><span data-ttu-id="3dbec-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dbec-196">See also</span></span>

<dl> <dt>

<span data-ttu-id="3dbec-197">**Tópicos de visão geral**</span><span class="sxs-lookup"><span data-stu-id="3dbec-197">**Overview Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="3dbec-198">Funções de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="3dbec-198">File Management Functions</span></span>](file-management-functions.md)
</dt> <dt>

[<span data-ttu-id="3dbec-199">Portas de conclusão de e/s</span><span class="sxs-lookup"><span data-stu-id="3dbec-199">I/O Completion Ports</span></span>](i-o-completion-ports.md)
</dt> <dt>

[<span data-ttu-id="3dbec-200">Usando os cabeçalhos do Windows</span><span class="sxs-lookup"><span data-stu-id="3dbec-200">Using the Windows Headers</span></span>](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[<span data-ttu-id="3dbec-201">Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="3dbec-201">Windows Sockets 2</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

<span data-ttu-id="3dbec-202">**Funções**</span><span class="sxs-lookup"><span data-stu-id="3dbec-202">**Functions**</span></span>
</dt> <dt>

[<span data-ttu-id="3dbec-203">**AcceptEx**</span><span class="sxs-lookup"><span data-stu-id="3dbec-203">**AcceptEx**</span></span>](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[<span data-ttu-id="3dbec-204">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="3dbec-204">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="3dbec-205">**DuplicateHandle**</span><span class="sxs-lookup"><span data-stu-id="3dbec-205">**DuplicateHandle**</span></span>](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[<span data-ttu-id="3dbec-206">**GetQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="3dbec-206">**GetQueuedCompletionStatus**</span></span>](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[<span data-ttu-id="3dbec-207">**GetQueuedCompletionStatusEx**</span><span class="sxs-lookup"><span data-stu-id="3dbec-207">**GetQueuedCompletionStatusEx**</span></span>](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[<span data-ttu-id="3dbec-208">**PostQueuedCompletionStatus**</span><span class="sxs-lookup"><span data-stu-id="3dbec-208">**PostQueuedCompletionStatus**</span></span>](postqueuedcompletionstatus.md)
</dt> <dt>

[<span data-ttu-id="3dbec-209">**ReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="3dbec-209">**ReadFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[<span data-ttu-id="3dbec-210">**WriteFileEx**</span><span class="sxs-lookup"><span data-stu-id="3dbec-210">**WriteFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

