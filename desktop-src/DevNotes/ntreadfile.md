---
description: Lê dados de um arquivo aberto.
ms.assetid: 7EA2FE38-20DA-43E1-A764-66A81725D1EA
title: Função NtReadFile (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtReadFile
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: be1a73c6451012dfd97d7d4c55c23f0842cf1551
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500831"
---
# <a name="ntreadfile-function"></a><span data-ttu-id="59e0c-103">Função NtReadFile</span><span class="sxs-lookup"><span data-stu-id="59e0c-103">NtReadFile function</span></span>

<span data-ttu-id="59e0c-104">Lê dados de um arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="59e0c-104">Reads data from an open file.</span></span>

<span data-ttu-id="59e0c-105">Essa função é o modo de usuário equivalente à função [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) documentada no WDK (Kit de driver do Windows).</span><span class="sxs-lookup"><span data-stu-id="59e0c-105">This function is the user-mode equivalent to the [**ZwReadFile**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntreadfile) function documented in the Windows Driver Kit (WDK).</span></span>

## <a name="syntax"></a><span data-ttu-id="59e0c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59e0c-106">Syntax</span></span>


```C++
NTSTATUS NtReadFile(
  _In_     HANDLE           FileHandle,
  _In_opt_ HANDLE           Event,
  _In_opt_ PIO_APC_ROUTINE  ApcRoutine,
  _In_opt_ PVOID            ApcContext,
  _Out_    PIO_STATUS_BLOCK IoStatusBlock,
  _Out_    PVOID            Buffer,
  _In_     ULONG            Length,
  _In_opt_ PLARGE_INTEGER   ByteOffset,
  _In_opt_ PULONG           Key
);
```



## <a name="parameters"></a><span data-ttu-id="59e0c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59e0c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59e0c-108">*Identificador de fileHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-108">*FileHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-109">Identificador para o objeto de arquivo.</span><span class="sxs-lookup"><span data-stu-id="59e0c-109">Handle to the file object.</span></span> <span data-ttu-id="59e0c-110">Esse identificador é criado por uma chamada bem-sucedida para [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) ou [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span><span class="sxs-lookup"><span data-stu-id="59e0c-110">This handle is created by a successful call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) or [**NtOpenFile**](/windows/desktop/api/Winternl/nf-winternl-ntopenfile).</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-111">*Evento* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-111">*Event* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-112">Opcionalmente, um identificador para um objeto de evento a ser definido para o estado sinalizado após a operação de leitura ser concluída.</span><span class="sxs-lookup"><span data-stu-id="59e0c-112">Optionally, a handle to an event object to set to the signaled state after the read operation completes.</span></span> <span data-ttu-id="59e0c-113">Os drivers intermediários e de dispositivo devem definir esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-113">Device and intermediate drivers should set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-114">*ApcRoutine* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-114">*ApcRoutine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-115">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="59e0c-115">This parameter is reserved.</span></span> <span data-ttu-id="59e0c-116">Os drivers intermediários e de dispositivo devem definir esse ponteiro como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-116">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-117">*ApcContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-117">*ApcContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-118">Esse parâmetro é reservado.</span><span class="sxs-lookup"><span data-stu-id="59e0c-118">This parameter is reserved.</span></span> <span data-ttu-id="59e0c-119">Os drivers intermediários e de dispositivo devem definir esse ponteiro como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-119">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-120">*IoStatusBlock* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-120">*IoStatusBlock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-121">Ponteiro para uma estrutura de [**\_ \_ bloco de status de e/s**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) que recebe o status final de conclusão e informações sobre a operação de leitura solicitada.</span><span class="sxs-lookup"><span data-stu-id="59e0c-121">Pointer to an [**IO\_STATUS\_BLOCK**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_io_status_block) structure that receives the final completion status and information about the requested read operation.</span></span> <span data-ttu-id="59e0c-122">O membro de **informações** recebe o número de bytes realmente lidos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="59e0c-122">The **Information** member receives the number of bytes actually read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-123">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-123">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-124">Ponteiro para um buffer alocado pelo chamador que recebe os dados lidos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="59e0c-124">Pointer to a caller-allocated buffer that receives the data read from the file.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-125">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-125">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-126">O tamanho, em bytes, do buffer apontado pelo *buffer*.</span><span class="sxs-lookup"><span data-stu-id="59e0c-126">The size, in bytes, of the buffer pointed to by *Buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-127">*ByteOffset* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-127">*ByteOffset* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-128">Ponteiro para uma variável que especifica o deslocamento de byte inicial no arquivo em que a operação de leitura será iniciada.</span><span class="sxs-lookup"><span data-stu-id="59e0c-128">Pointer to a variable that specifies the starting byte offset in the file where the read operation will begin.</span></span> <span data-ttu-id="59e0c-129">Se for feita uma tentativa de leitura além do final do arquivo, **NtReadFile** retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="59e0c-129">If an attempt is made to read beyond the end of the file, **NtReadFile** returns an error.</span></span>

<span data-ttu-id="59e0c-130">Se a chamada para [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) definir o alerta de e/s SÍNCRONA do arquivo de sinalizadores de *criaçãooptions* \_ ou o \_ \_ arquivo \_ de es síncrona de arquivos não \_ \_ alerta, o Gerenciador de e/s manterá a posição atual do arquivo.</span><span class="sxs-lookup"><span data-stu-id="59e0c-130">If the call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set either of the *CreateOptions* flags FILE\_SYNCHRONOUS\_IO\_ALERT or FILE\_SYNCHRONOUS\_IO\_NONALERT, the I/O Manager maintains the current file position.</span></span> <span data-ttu-id="59e0c-131">Nesse caso, o chamador de **NtReadFile** pode especificar que o deslocamento da posição atual do arquivo seja usado em vez de um valor *ByteOffset* explícito.</span><span class="sxs-lookup"><span data-stu-id="59e0c-131">If so, the caller of **NtReadFile** can specify that the current file position offset be used instead of an explicit *ByteOffset* value.</span></span> <span data-ttu-id="59e0c-132">Essa especificação pode ser feita usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="59e0c-132">This specification can be made by using one of the following methods:</span></span>

-   <span data-ttu-id="59e0c-133">Especifique um ponteiro para um **valor \_ inteiro grande** com o membro **HighPart** definido como-1 e o membro **LowPart** definido como o arquivo de valor definido pelo sistema use a posição do \_ ponteiro do \_ arquivo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="59e0c-133">Specify a pointer to a **LARGE\_INTEGER** value with the **HighPart** member set to -1 and the **LowPart** member set to the system-defined value FILE\_USE\_FILE\_POINTER\_POSITION.</span></span>

-   <span data-ttu-id="59e0c-134">Passe um ponteiro **NULL** para *ByteOffset*.</span><span class="sxs-lookup"><span data-stu-id="59e0c-134">Pass a **NULL** pointer for *ByteOffset*.</span></span>

<span data-ttu-id="59e0c-135">O **NtReadFile** atualiza a posição atual do arquivo adicionando o número de bytes lidos quando concluir a operação de leitura, se estiver usando a posição atual do arquivo mantida pelo Gerenciador de e/s.</span><span class="sxs-lookup"><span data-stu-id="59e0c-135">**NtReadFile** updates the current file position by adding the number of bytes read when it completes the read operation, if it is using the current file position maintained by the I/O Manager.</span></span>

<span data-ttu-id="59e0c-136">Mesmo quando o Gerenciador de e/s está mantendo a posição atual do arquivo, o chamador pode redefinir essa posição passando um valor *ByteOffset* explícito para **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-136">Even when the I/O Manager is maintaining the current file position, the caller can reset this position by passing an explicit *ByteOffset* value to **NtReadFile**.</span></span> <span data-ttu-id="59e0c-137">Fazer isso altera automaticamente a posição do arquivo atual para esse valor de *ByteOffset* , executa a operação de leitura e, em seguida, atualiza a posição de acordo com o número de bytes realmente lidos.</span><span class="sxs-lookup"><span data-stu-id="59e0c-137">Doing this automatically changes the current file position to that *ByteOffset* value, performs the read operation, and then updates the position according to the number of bytes actually read.</span></span> <span data-ttu-id="59e0c-138">Essa técnica fornece o serviço de busca e leitura atômica do chamador.</span><span class="sxs-lookup"><span data-stu-id="59e0c-138">This technique gives the caller atomic seek-and-read service.</span></span>

</dd> <dt>

<span data-ttu-id="59e0c-139">*Chave* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-139">*Key* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="59e0c-140">Os drivers intermediários e de dispositivo devem definir esse ponteiro como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-140">Device and intermediate drivers should set this pointer to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59e0c-141">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59e0c-141">Return value</span></span>

<span data-ttu-id="59e0c-142">**NtReadFile** retorna o status \_ Success ou o código de erro NTSTATUS apropriado.</span><span class="sxs-lookup"><span data-stu-id="59e0c-142">**NtReadFile** returns either STATUS\_SUCCESS or the appropriate NTSTATUS error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="59e0c-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="59e0c-143">Remarks</span></span>

<span data-ttu-id="59e0c-144">Os chamadores de **NtReadFile** devem já ter chamado [**NTCREATEFILE**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) com o arquivo de leitura de \_ \_ dados ou o valor de leitura genérico \_ definido no parâmetro *desiredAccess* .</span><span class="sxs-lookup"><span data-stu-id="59e0c-144">Callers of **NtReadFile** must have already called [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) with the FILE\_READ\_DATA or GENERIC\_READ value set in the *DesiredAccess* parameter.</span></span>

<span data-ttu-id="59e0c-145">Se a chamada anterior para [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) definir o sinalizador do arquivo \_ sem \_ \_ buffer intermediário no parâmetro *CreateOptions* como **NtCreateFile**, os parâmetros *Length* e *ByteOffset* para **NtReadFile** devem ser múltiplos do tamanho do setor.</span><span class="sxs-lookup"><span data-stu-id="59e0c-145">If the preceding call to [**NtCreateFile**](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile) set the FILE\_NO\_INTERMEDIATE\_BUFFERING flag in the *CreateOptions* parameter to **NtCreateFile**, the *Length* and *ByteOffset* parameters to **NtReadFile** must be multiples of the sector size.</span></span> <span data-ttu-id="59e0c-146">Para obter mais informações, consulte **NtCreateFile**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-146">For more information, see **NtCreateFile**.</span></span>

<span data-ttu-id="59e0c-147">**NtReadFile** começa a ler da *ByteOffset* especificada ou da posição do arquivo atual para o *buffer* fornecido.</span><span class="sxs-lookup"><span data-stu-id="59e0c-147">**NtReadFile** begins reading from the given *ByteOffset* or the current file position into the given *Buffer*.</span></span> <span data-ttu-id="59e0c-148">Ele encerra a operação de leitura em uma das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="59e0c-148">It terminates the read operation under one of the following conditions:</span></span>

-   <span data-ttu-id="59e0c-149">O buffer está cheio porque o número de bytes especificado pelo parâmetro de *comprimento* foi lido.</span><span class="sxs-lookup"><span data-stu-id="59e0c-149">The buffer is full because the number of bytes specified by the *Length* parameter has been read.</span></span> <span data-ttu-id="59e0c-150">Portanto, não é possível colocar mais dados no buffer sem um estouro.</span><span class="sxs-lookup"><span data-stu-id="59e0c-150">Therefore, no more data can be placed into the buffer without an overflow.</span></span>

-   <span data-ttu-id="59e0c-151">O fim do arquivo é atingido durante a operação de leitura, portanto, não há mais dados no arquivo a serem transferidos para o buffer.</span><span class="sxs-lookup"><span data-stu-id="59e0c-151">The end of file is reached during the read operation, so there is no more data in the file to be transferred into the buffer.</span></span>

<span data-ttu-id="59e0c-152">Se o chamador abrir o arquivo com o sinalizador SYNCHRONIZE definido em *desiredAccess*, o thread de chamada poderá sincronizar com a conclusão da operação de leitura aguardando o identificador do arquivo, *fileHandle*.</span><span class="sxs-lookup"><span data-stu-id="59e0c-152">If the caller opened the file with the SYNCHRONIZE flag set in *DesiredAccess*, the calling thread can synchronize to the completion of the read operation by waiting on the file handle, *FileHandle*.</span></span> <span data-ttu-id="59e0c-153">O identificador é sinalizado cada vez que uma operação de e/s emitida no identificador é concluída.</span><span class="sxs-lookup"><span data-stu-id="59e0c-153">The handle is signaled each time that an I/O operation that was issued on the handle completes.</span></span> <span data-ttu-id="59e0c-154">No entanto, o chamador não deve aguardar um identificador que foi aberto para acesso a arquivos síncronos (alerta de e/s de arquivo \_ síncrono de \_ es \_ \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="59e0c-154">However, the caller must not wait on a handle that was opened for synchronous file access (FILE\_SYNCHRONOUS\_IO\_NONALERT or FILE\_SYNCHRONOUS\_IO\_ALERT).</span></span> <span data-ttu-id="59e0c-155">Nesse caso, **NtReadFile** aguarda em nome do chamador e não retorna até que a operação de leitura seja concluída.</span><span class="sxs-lookup"><span data-stu-id="59e0c-155">In this case, **NtReadFile** waits on behalf of the caller and does not return until the read operation is complete.</span></span> <span data-ttu-id="59e0c-156">O chamador pode aguardar com segurança o identificador do arquivo somente se todas as três condições a seguir forem atendidas:</span><span class="sxs-lookup"><span data-stu-id="59e0c-156">The caller can safely wait on the file handle only if all three of the following conditions are met:</span></span>

-   <span data-ttu-id="59e0c-157">O identificador foi aberto para acesso assíncrono (ou seja, nenhum \_ sinalizador de \_ e/s SÍNCRONA de arquivo \_  foi especificado).</span><span class="sxs-lookup"><span data-stu-id="59e0c-157">The handle was opened for asynchronous access (that is, neither FILE\_SYNCHRONOUS\_IO\_*XXX* flag was specified).</span></span>

-   <span data-ttu-id="59e0c-158">O identificador está sendo usado apenas para uma operação de e/s por vez.</span><span class="sxs-lookup"><span data-stu-id="59e0c-158">The handle is being used for only one I/O operation at a time.</span></span>

-   <span data-ttu-id="59e0c-159">**NtReadFile** retornou o status \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="59e0c-159">**NtReadFile** returned STATUS\_PENDING.</span></span>

<span data-ttu-id="59e0c-160">Um driver deve chamar **NtReadFile** no contexto do processo do sistema se qualquer uma das seguintes condições existir:</span><span class="sxs-lookup"><span data-stu-id="59e0c-160">A driver should call **NtReadFile** in the context of the system process if any of the following conditions exist:</span></span>

-   <span data-ttu-id="59e0c-161">O driver criou o identificador de arquivo que ele passa para **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-161">The driver created the file handle that it passes to **NtReadFile**.</span></span>

-   <span data-ttu-id="59e0c-162">O **NtReadFile** notificará o driver de conclusão de e/s por meio de um evento criado pelo driver.</span><span class="sxs-lookup"><span data-stu-id="59e0c-162">**NtReadFile** will notify the driver of I/O completion by means of an event that the driver created.</span></span>

-   <span data-ttu-id="59e0c-163">O **NtReadFile** notificará o driver de conclusão de e/s por meio de uma rotina de retorno de chamada da APC que o driver passa para **NtReadFile**.</span><span class="sxs-lookup"><span data-stu-id="59e0c-163">**NtReadFile** will notify the driver of I/O completion by means of an APC callback routine that the driver passes to **NtReadFile**.</span></span>

<span data-ttu-id="59e0c-164">Os identificadores de arquivo e de evento são válidos somente no contexto do processo em que os identificadores são criados.</span><span class="sxs-lookup"><span data-stu-id="59e0c-164">File and event handles are valid only in the process context where the handles are created.</span></span> <span data-ttu-id="59e0c-165">Portanto, para evitar brechas de segurança, o driver deve criar qualquer identificador de arquivo ou evento que ele passe para **NtReadFile** no contexto do processo do sistema, em vez do contexto do processo em que o driver está.</span><span class="sxs-lookup"><span data-stu-id="59e0c-165">Therefore, to avoid security holes, the driver should create any file or event handle that it passes to **NtReadFile** in the context of the system process rather than the context of the process that the driver is in.</span></span>

<span data-ttu-id="59e0c-166">Da mesma forma, **NtReadFile** deve ser chamado no contexto do processo do sistema, caso ele notifique o driver de conclusão de e/s por meio de uma APC, porque o APCs sempre é acionado no contexto do thread que emite a solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="59e0c-166">Likewise, **NtReadFile** should be called in the context of the system process if it notifies the driver of I/O completion by means of an APC, because APCs are always fired in the context of the thread that issues the I/O request.</span></span> <span data-ttu-id="59e0c-167">Se o driver chamar **NtReadFile** no contexto de um processo diferente do sistema um, a APC poderá ser atrasada indefinidamente ou pode não ser acionada.</span><span class="sxs-lookup"><span data-stu-id="59e0c-167">If the driver calls **NtReadFile** in the context of a process other than the system one, the APC could be delayed indefinitely, or it might not fire at all.</span></span>

<span data-ttu-id="59e0c-168">Para obter mais informações sobre como trabalhar com arquivos, consulte [usando arquivos em um driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span><span class="sxs-lookup"><span data-stu-id="59e0c-168">For more information about working with files, see [Using Files in a Driver](/windows-hardware/drivers/kernel/using-files-in-a-driver).</span></span>

<span data-ttu-id="59e0c-169">Os chamadores de **NtReadFile** devem estar em execução em IRQL = \_ nível passivo e com o [kernel APCs especial habilitado](/windows-hardware/drivers/kernel/disabling-apcs).</span><span class="sxs-lookup"><span data-stu-id="59e0c-169">Callers of **NtReadFile** must be running at IRQL = PASSIVE\_LEVEL and [with special kernel APCs enabled](/windows-hardware/drivers/kernel/disabling-apcs).</span></span>

## <a name="requirements"></a><span data-ttu-id="59e0c-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59e0c-170">Requirements</span></span>



| <span data-ttu-id="59e0c-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e0c-171">Requirement</span></span> | <span data-ttu-id="59e0c-172">Valor</span><span class="sxs-lookup"><span data-stu-id="59e0c-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59e0c-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59e0c-173">Minimum supported client</span></span><br/> | <span data-ttu-id="59e0c-174">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="59e0c-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59e0c-175">Minimum supported server</span></span><br/> | <span data-ttu-id="59e0c-176">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="59e0c-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="59e0c-177">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="59e0c-177">Target platform</span></span><br/>          | <dl> <span data-ttu-id="59e0c-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="59e0c-178"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="59e0c-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59e0c-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="59e0c-180"><dt>WDM. h (incluindo WDM. h, Ntddk. h ou Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59e0c-180"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="59e0c-181">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59e0c-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="59e0c-182"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59e0c-182"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="59e0c-183">DLL</span><span class="sxs-lookup"><span data-stu-id="59e0c-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59e0c-184"><dt>Ntdll.dll (modo de usuário)</dt></span><span class="sxs-lookup"><span data-stu-id="59e0c-184"><dt>Ntdll.dll (user mode)</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="59e0c-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="59e0c-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59e0c-186">**KeInitializeEvent**</span><span class="sxs-lookup"><span data-stu-id="59e0c-186">**KeInitializeEvent**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-keinitializeevent)
</dt> <dt>

[<span data-ttu-id="59e0c-187">**NtCreateFile**</span><span class="sxs-lookup"><span data-stu-id="59e0c-187">**NtCreateFile**</span></span>](/windows/desktop/api/Winternl/nf-winternl-ntcreatefile)
</dt> <dt>

[<span data-ttu-id="59e0c-188">**NtQueryInformationFile**</span><span class="sxs-lookup"><span data-stu-id="59e0c-188">**NtQueryInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntqueryinformationfile)
</dt> <dt>

[<span data-ttu-id="59e0c-189">**NtSetInformationFile**</span><span class="sxs-lookup"><span data-stu-id="59e0c-189">**NtSetInformationFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntsetinformationfile)
</dt> <dt>

[<span data-ttu-id="59e0c-190">**NtWriteFile**</span><span class="sxs-lookup"><span data-stu-id="59e0c-190">**NtWriteFile**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-ntwritefile)
</dt> </dl>

 

 
