---
description: A função AddPrinter adiciona uma impressora à lista de impressoras com suporte para um servidor especificado.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Função AddPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169354"
---
# <a name="addprinter-function"></a><span data-ttu-id="0374f-103">Função AddPrinter</span><span class="sxs-lookup"><span data-stu-id="0374f-103">AddPrinter function</span></span>

<span data-ttu-id="0374f-104">A função **AddPrinter** adiciona uma impressora à lista de impressoras com suporte para um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="0374f-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0374f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0374f-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="0374f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0374f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0374f-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0374f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0374f-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual a impressora deve ser instalada.</span><span class="sxs-lookup"><span data-stu-id="0374f-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="0374f-109">Se essa cadeia de caracteres for **nula**, a impressora será instalada localmente.</span><span class="sxs-lookup"><span data-stu-id="0374f-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="0374f-110">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="0374f-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0374f-111">A versão da estrutura à qual o *pPrinter* aponta.</span><span class="sxs-lookup"><span data-stu-id="0374f-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="0374f-112">Esse valor deve ser 2.</span><span class="sxs-lookup"><span data-stu-id="0374f-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="0374f-113">*pPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0374f-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0374f-114">Um ponteiro para uma estrutura de [**informações da impressora \_ \_ 2**](printer-info-2.md) que contém informações sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="0374f-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="0374f-115">Você deve especificar valores não **nulos** para os membros **pPrinterName**, **pPortName**, **pDriverName** e **pPrintProcessor** dessa estrutura antes de chamar **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="0374f-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0374f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0374f-116">Return value</span></span>

<span data-ttu-id="0374f-117">Se a função for realizada com sucesso, o valor de retorno será um identificador (não seguro para thread) para um novo objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="0374f-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="0374f-118">Quando você terminar com o identificador, passe-o para a função [**ClosePrinter**](closeprinter.md) para fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="0374f-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="0374f-119">Se a função falhar, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="0374f-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0374f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0374f-120">Remarks</span></span>

<span data-ttu-id="0374f-121">Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="0374f-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="0374f-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0374f-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0374f-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0374f-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0374f-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="0374f-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="0374f-125">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="0374f-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="0374f-126">O identificador retornado não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0374f-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="0374f-127">Se os chamadores precisarem usá-lo simultaneamente em vários threads, eles deverão fornecer acesso de sincronização personalizado ao identificador da impressora usando as [funções de sincronização](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="0374f-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="0374f-128">Para evitar escrever código personalizado, o aplicativo pode abrir um identificador de impressora em cada thread, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="0374f-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="0374f-129">A seguir estão os membros da estrutura [**\_ info \_ 2 da impressora**](printer-info-2.md) que podem ser definidos antes que a função **AddPrinter** seja chamada:</span><span class="sxs-lookup"><span data-stu-id="0374f-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="0374f-130">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="0374f-130">**Attributes**</span></span>
-   <span data-ttu-id="0374f-131">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="0374f-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="0374f-132">**Defaultanteriority**</span><span class="sxs-lookup"><span data-stu-id="0374f-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="0374f-133">**Prioridade**</span><span class="sxs-lookup"><span data-stu-id="0374f-133">**Priority**</span></span>
-   <span data-ttu-id="0374f-134">**pComment**</span><span class="sxs-lookup"><span data-stu-id="0374f-134">**pComment**</span></span>
-   <span data-ttu-id="0374f-135">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0374f-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="0374f-136">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="0374f-136">**pDatatype**</span></span>
-   <span data-ttu-id="0374f-137">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="0374f-137">**pSepFile**</span></span>
-   <span data-ttu-id="0374f-138">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="0374f-138">**pDevMode**</span></span>
-   <span data-ttu-id="0374f-139">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="0374f-139">**pShareName**</span></span>
-   <span data-ttu-id="0374f-140">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="0374f-140">**pLocation**</span></span>
-   <span data-ttu-id="0374f-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="0374f-141">**StartTime**</span></span>
-   <span data-ttu-id="0374f-142">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="0374f-142">**pParameters**</span></span>
-   <span data-ttu-id="0374f-143">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="0374f-143">**UntilTime**</span></span>

<span data-ttu-id="0374f-144">Os membros **status**, **cJobs** e **AveragePPM** da estrutura [**informações da \_ impressora \_ 2**](printer-info-2.md) são reservados para uso pela função [**getprinter**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="0374f-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="0374f-145">Eles não devem ser definidos antes de chamar **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="0374f-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="0374f-146">Se **pSecurityDescriptor** for **NULL**, o sistema atribuirá um descritor de segurança padrão à impressora.</span><span class="sxs-lookup"><span data-stu-id="0374f-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="0374f-147">O descritor de segurança padrão tem as seguintes permissões.</span><span class="sxs-lookup"><span data-stu-id="0374f-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="0374f-148">Valor</span><span class="sxs-lookup"><span data-stu-id="0374f-148">Value</span></span>                          | <span data-ttu-id="0374f-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="0374f-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0374f-150">Administradores e Usuários Avançados</span><span class="sxs-lookup"><span data-stu-id="0374f-150">Administrators and Power Users</span></span> | <span data-ttu-id="0374f-151">Controle total na fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="0374f-151">Full control on the print queue.</span></span> <span data-ttu-id="0374f-152">Isso significa que os membros desses grupos podem imprimir, gerenciar a fila (pode excluir a fila, alterar qualquer configuração da fila, incluindo o descritor de segurança) e gerenciar os trabalhos de impressão de todos os usuários (excluir, pausar, retomar e reiniciar trabalhos). Observe que os usuários avançados não existem antes do Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="0374f-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="0374f-153">Criador/Proprietário</span><span class="sxs-lookup"><span data-stu-id="0374f-153">Creator/Owner</span></span>                  | <span data-ttu-id="0374f-154">Pode gerenciar trabalhos próprios.</span><span class="sxs-lookup"><span data-stu-id="0374f-154">Can manage own jobs.</span></span> <span data-ttu-id="0374f-155">Isso significa que o usuário que envia trabalhos pode gerenciar (excluir, pausar, retomar, reiniciar) seus próprios trabalhos.</span><span class="sxs-lookup"><span data-stu-id="0374f-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="0374f-156">Todos</span><span class="sxs-lookup"><span data-stu-id="0374f-156">Everyone</span></span>                       | <span data-ttu-id="0374f-157">Execute e controle de leitura padrão.</span><span class="sxs-lookup"><span data-stu-id="0374f-157">Execute and standard read control.</span></span> <span data-ttu-id="0374f-158">Isso significa que os membros do grupo Everyone podem imprimir e ler as propriedades da fila de impressão.</span><span class="sxs-lookup"><span data-stu-id="0374f-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="0374f-159">Depois que um aplicativo cria um objeto de impressora com a função **AddPrinter** , ele deve usar a função [**printerproperties**](printerproperties.md) para especificar as configurações corretas para o driver de impressora associado ao objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="0374f-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="0374f-160">A função **AddPrinter** retornará um erro se um objeto de impressora com o mesmo nome já existir, a menos que esse objeto esteja marcado como exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="0374f-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="0374f-161">Nesse caso, a impressora existente não é excluída, e os parâmetros de criação **Addimprimíer** são usados para alterar as configurações de impressora existentes (como se o aplicativo tivesse usado a função [**setprintr**](setprinter.md) ).</span><span class="sxs-lookup"><span data-stu-id="0374f-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="0374f-162">Use a função [**EnumPrintProcessors**](enumprintprocessors.md) para enumerar o conjunto de processadores de impressão instalados em um servidor.</span><span class="sxs-lookup"><span data-stu-id="0374f-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="0374f-163">Use a função [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) para enumerar o conjunto de tipos de dados que um processador de impressão suporta.</span><span class="sxs-lookup"><span data-stu-id="0374f-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="0374f-164">Use a função [**EnumPorts**](enumports.md) para enumerar o conjunto de portas disponíveis.</span><span class="sxs-lookup"><span data-stu-id="0374f-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="0374f-165">Use a função [**EnumPrinterDrivers**](enumprinterdrivers.md) para enumerar os drivers de impressora instalados.</span><span class="sxs-lookup"><span data-stu-id="0374f-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="0374f-166">O chamador da função **AddPrinter** deve ter acesso \_ ao servidor \_ administrar o acesso ao servidor no qual a impressora será criada.</span><span class="sxs-lookup"><span data-stu-id="0374f-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="0374f-167">O identificador retornado pela função terá toda a permissão de acesso à impressora \_ \_ e poderá ser usado para executar operações administrativas na impressora.</span><span class="sxs-lookup"><span data-stu-id="0374f-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="0374f-168">Se a função **DrvPrinterEvent** for passada, o sinalizador de evento de impressora \_ \_ \_ sem sinalizador de interface do \_ usuário não deverá usar uma chamada de interface do usuário durante o **DrvPrinterEvent**.</span><span class="sxs-lookup"><span data-stu-id="0374f-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="0374f-169">Para fazer trabalhos relacionados à interface do usuário, o instalador deve usar a entrada **VendorSetup** no arquivo. inf da impressora ou, para dispositivos plug and Play, o instalador pode usar um coinstalador específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0374f-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="0374f-170">Para obter mais informações sobre o **VendorSetup**, consulte o Microsoft Windows Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="0374f-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="0374f-171">O firewall de conexão com a Internet (ICF) bloqueia as portas de impressora por padrão, mas uma exceção para o compartilhamento de arquivos e impressoras é habilitada quando você executa o **AddPrinter**.</span><span class="sxs-lookup"><span data-stu-id="0374f-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0374f-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0374f-172">Requirements</span></span>



| <span data-ttu-id="0374f-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="0374f-173">Requirement</span></span> | <span data-ttu-id="0374f-174">Valor</span><span class="sxs-lookup"><span data-stu-id="0374f-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0374f-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0374f-175">Minimum supported client</span></span><br/> | <span data-ttu-id="0374f-176">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0374f-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0374f-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0374f-177">Minimum supported server</span></span><br/> | <span data-ttu-id="0374f-178">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0374f-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0374f-179">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0374f-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="0374f-180"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0374f-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0374f-181">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0374f-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="0374f-182"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0374f-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0374f-183">DLL</span><span class="sxs-lookup"><span data-stu-id="0374f-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0374f-184"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0374f-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0374f-185">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0374f-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0374f-186">**AddPrinterW** (Unicode) e **addprintera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0374f-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="0374f-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="0374f-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0374f-188">Impressão</span><span class="sxs-lookup"><span data-stu-id="0374f-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0374f-189">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="0374f-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0374f-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="0374f-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="0374f-191">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="0374f-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="0374f-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="0374f-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="0374f-193">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="0374f-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="0374f-194">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="0374f-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="0374f-195">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="0374f-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="0374f-196">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="0374f-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="0374f-197">**Informações da impressora \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="0374f-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="0374f-198">**Impressoras**</span><span class="sxs-lookup"><span data-stu-id="0374f-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="0374f-199">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="0374f-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

