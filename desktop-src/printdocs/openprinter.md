---
description: A função OpenPrinter recupera um identificador para a impressora ou o servidor de impressão especificado ou outros tipos de identificadores no subsistema de impressão.
ms.assetid: 96763220-d851-46f0-8be8-403f3356edb9
title: Função OpenPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter
- OpenPrinterA
- OpenPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-0.dll
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 02cd6f6b5d56eec525bd00e2feef50f4d5f07734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749933"
---
# <a name="openprinter-function"></a><span data-ttu-id="3c637-103">Função OpenPrinter</span><span class="sxs-lookup"><span data-stu-id="3c637-103">OpenPrinter function</span></span>

<span data-ttu-id="3c637-104">A função **OpenPrinter** recupera um identificador para a impressora ou o servidor de impressão especificado ou outros tipos de identificadores no subsistema de impressão.</span><span class="sxs-lookup"><span data-stu-id="3c637-104">The **OpenPrinter** function retrieves a handle to the specified printer or print server or other types of handles in the print subsystem.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c637-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3c637-105">Syntax</span></span>


```C++
BOOL OpenPrinter(
  _In_  LPTSTR             pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault
);
```



## <a name="parameters"></a><span data-ttu-id="3c637-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c637-107">*pPrinterName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c637-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c637-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome da impressora ou do servidor de impressão, o objeto de impressora, o XcvMonitor ou o XcvPort.</span><span class="sxs-lookup"><span data-stu-id="3c637-108">A pointer to a null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="3c637-109">Para um objeto de impressora, use: PrinterName, trabalho xxxx.</span><span class="sxs-lookup"><span data-stu-id="3c637-109">For a printer object use: PrinterName, Job xxxx.</span></span> <span data-ttu-id="3c637-110">Para um XcvMonitor, use: nomedoservidor, XcvMonitor Monitorname.</span><span class="sxs-lookup"><span data-stu-id="3c637-110">For an XcvMonitor, use: ServerName, XcvMonitor MonitorName.</span></span> <span data-ttu-id="3c637-111">Para um XcvPort, use: nomedoservidor, XcvPort PortName.</span><span class="sxs-lookup"><span data-stu-id="3c637-111">For an XcvPort, use: ServerName, XcvPort PortName.</span></span>

<span data-ttu-id="3c637-112">Se for **NULL**, indicará o servidor de impressora local.</span><span class="sxs-lookup"><span data-stu-id="3c637-112">If **NULL**, it indicates the local printer server.</span></span>

</dd> <dt>

<span data-ttu-id="3c637-113">*phPrinter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3c637-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c637-114">Um ponteiro para uma variável que recebe um identificador (não seguro para thread) para o objeto de impressora aberta ou de servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="3c637-114">A pointer to a variable that receives a handle (not thread safe) to the open printer or print server object.</span></span>

<span data-ttu-id="3c637-115">O parâmetro *phPrinter* pode retornar um identificador Xcv para uso com a função XcvData.</span><span class="sxs-lookup"><span data-stu-id="3c637-115">The *phPrinter* parameter can return an Xcv handle for use with the XcvData function.</span></span> <span data-ttu-id="3c637-116">Para obter mais informações sobre XcvData, consulte o DDK.</span><span class="sxs-lookup"><span data-stu-id="3c637-116">For more information about XcvData, see the DDK.</span></span>

</dd> <dt>

<span data-ttu-id="3c637-117">*pDefault* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3c637-117">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c637-118">Um ponteiro para uma estrutura de [**\_ padrões de impressora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="3c637-118">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="3c637-119">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3c637-119">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c637-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c637-120">Return value</span></span>

<span data-ttu-id="3c637-121">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3c637-121">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3c637-122">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="3c637-122">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c637-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c637-123">Remarks</span></span>

<span data-ttu-id="3c637-124">Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="3c637-124">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="3c637-125">Um identificador obtido para uma impressora remota por uma chamada para **OpenPrinter** para uma impressora remota acessa a impressora por meio de um cache local no serviço spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="3c637-125">A handle obtained for a remote printer by a call to **OpenPrinter** for a remote printer accesses the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="3c637-126">Esse cache não é preciso em tempo real.</span><span class="sxs-lookup"><span data-stu-id="3c637-126">This cache isn't real-time accurate.</span></span> <span data-ttu-id="3c637-127">Para obter dados precisos, substitua a chamada OpenPrinter por [**OpenPrinter2**](openprinter2.md) por POptions. dwFlags definido como \_ opção de impressora \_ sem \_ cache.</span><span class="sxs-lookup"><span data-stu-id="3c637-127">To obtain accurate data, replace the OpenPrinter call with [**OpenPrinter2**](openprinter2.md) with pOptions.dwFlags set to PRINTER\_OPTION\_NO\_CACHE.</span></span> <span data-ttu-id="3c637-128">Observe que apenas OpenPrinter2W é funcional.</span><span class="sxs-lookup"><span data-stu-id="3c637-128">Note that only OpenPrinter2W is functional.</span></span> <span data-ttu-id="3c637-129">A função retorna um identificador de impressora que usa outras chamadas à API de impressão e ignora o cache local.</span><span class="sxs-lookup"><span data-stu-id="3c637-129">The function returns a printer handle that uses other Printing API calls and bypasses the local cache.</span></span> <span data-ttu-id="3c637-130">Esse método é bloqueado enquanto aguarda a comunicação de rede com a impressora remota, portanto, ele pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3c637-130">This method blocks while waiting for network communication with the remote printer, so it might not return immediately.</span></span> <span data-ttu-id="3c637-131">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c637-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3c637-132">Chamar essa função de um thread que gerencia a interação da interface do usuário pode fazer com que o aplicativo pareça sem resposta.</span><span class="sxs-lookup"><span data-stu-id="3c637-132">Calling this function from a thread that manages user interface interaction might make the application appear unresponsive.</span></span>

 

> [!Note]  
> <span data-ttu-id="3c637-133">Um identificador obtido por uma chamada para **OpenPrinter** para uma impressora remota acessará a impressora por meio de um cache local no serviço spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="3c637-133">A handle obtained by a call to **OpenPrinter** for a remote printer will access the printer through a local cache in the print spooler service.</span></span> <span data-ttu-id="3c637-134">Esse cache é, por design, não é preciso em tempo real.</span><span class="sxs-lookup"><span data-stu-id="3c637-134">This cache is, by design, not real time accurate.</span></span> <span data-ttu-id="3c637-135">Se você precisar obter dados precisos, substitua a chamada **OpenPrinter** por [**OpenPrinter2**](openprinter2.md) por *pOptions. dwFlags* definido como [**opção de impressora \_ \_ sem \_ cache**](printer-options.md).</span><span class="sxs-lookup"><span data-stu-id="3c637-135">If you need to obtain accurate data, replace the **OpenPrinter** call with [**OpenPrinter2**](openprinter2.md) with *pOptions.dwFlags* set to [**PRINTER\_OPTION\_NO\_CACHE**](printer-options.md).</span></span> <span data-ttu-id="3c637-136">Observe que apenas **OpenPrinter2W** é funcional.</span><span class="sxs-lookup"><span data-stu-id="3c637-136">Note that only **OpenPrinter2W** is functional.</span></span> <span data-ttu-id="3c637-137">Ao fazer isso, a função retorna um identificador de impressora que faz com que outras chamadas à API de impressão ignorem o cache local.</span><span class="sxs-lookup"><span data-stu-id="3c637-137">Doing so the function returns a printer handle that makes other Printing API calls to bypass the local cache.</span></span> <span data-ttu-id="3c637-138">Observe que essa abordagem será bloqueada enquanto aguarda a comunicação de rede de ida e volta para a impressora remota, para que ela possa não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3c637-138">Note that this approach will block while waiting for the round-trip network communication to the remote printer, so it may not return immediately.</span></span> <span data-ttu-id="3c637-139">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3c637-139">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation - factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3c637-140">Portanto, chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="3c637-140">Therefore calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3c637-141">O identificador apontado por *phPrinter* não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="3c637-141">The handle pointed to by *phPrinter* is not thread safe.</span></span> <span data-ttu-id="3c637-142">Se os chamadores precisarem usá-lo simultaneamente em vários threads, eles deverão fornecer acesso de sincronização personalizado ao identificador da impressora usando as [funções de sincronização](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="3c637-142">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="3c637-143">Para evitar escrever código personalizado, o aplicativo pode abrir um identificador de impressora em cada thread, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="3c637-143">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="3c637-144">O parâmetro *pDefault* permite que você especifique o tipo de dados e os valores do modo de dispositivo que são usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="3c637-144">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="3c637-145">No entanto, você pode substituir esses valores usando a função [**SetJob**](setjob.md) depois que um documento for iniciado.</span><span class="sxs-lookup"><span data-stu-id="3c637-145">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="3c637-146">As configurações [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definidas na estrutura [**\_ padrões da impressora**](printer-defaults.md) do parâmetro *pDefault* não são usadas quando o valor do membro *pDatatype* da estrutura [**info do documento \_ \_ 1**](doc-info-1.md) que foi passada no parâmetro *pDocInfo* da chamada [**StartDocPrinter**](startdocprinter.md) é "RAW".</span><span class="sxs-lookup"><span data-stu-id="3c637-146">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) settings defined in the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure of the *pDefault* parameter are not used when the value of the *pDatatype* member of the [**DOC\_INFO\_1**](doc-info-1.md) structure that was passed in the *pDocInfo* parameter of the [**StartDocPrinter**](startdocprinter.md) call is "RAW".</span></span> <span data-ttu-id="3c637-147">Quando um documento de alto nível (como um arquivo Adobe PDF ou Microsoft Word) ou outros dados de impressora (como PCL, PS ou HPGL) são enviados diretamente para uma impressora com *pDatatype* definido como "RAW", o documento deve descrever totalmente as configurações do trabalho de impressão estilo **DEVMODE** no idioma compreendido pelo hardware.</span><span class="sxs-lookup"><span data-stu-id="3c637-147">When a high-level document (such as an Adobe PDF or Microsoft Word file) or other printer data (such PCL, PS, or HPGL) is sent directly to a printer with *pDatatype* set to "RAW", the document must fully describe the **DEVMODE**-style print job settings in the language understood by the hardware.</span></span>

<span data-ttu-id="3c637-148">Você pode chamar a função **OpenPrinter** para abrir um identificador para um servidor de impressão ou para determinar os direitos de acesso que um cliente tem a um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="3c637-148">You can call the **OpenPrinter** function to open a handle to a print server or to determine the access rights that a client has to a print server.</span></span> <span data-ttu-id="3c637-149">Para fazer isso, especifique o nome do servidor de impressão no parâmetro *pPrinterName* , defina os membros **pDatatype** e **PDevMode** da estrutura [**\_ padrões da impressora**](printer-defaults.md) como **NULL** e defina o membro **desiredAccess** para especificar um valor de máscara de acesso do servidor, como servidor \_ todo \_ acesso.</span><span class="sxs-lookup"><span data-stu-id="3c637-149">To do so, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="3c637-150">Quando você terminar com a alça, passe-a para a função [**ClosePrinter**](closeprinter.md) para fechá-la.</span><span class="sxs-lookup"><span data-stu-id="3c637-150">When you finish with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="3c637-151">Use o membro **desiredAccess** da estrutura [**\_ padrões da impressora**](printer-defaults.md) para especificar os direitos de acesso necessários para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3c637-151">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the access rights that you need to the printer.</span></span> <span data-ttu-id="3c637-152">Os direitos de acesso podem ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="3c637-152">The access rights can be one of the following.</span></span> <span data-ttu-id="3c637-153">(Se *pDefault* for **nulo**, os direitos de acesso serão impressora \_ uso de acesso \_ .)</span><span class="sxs-lookup"><span data-stu-id="3c637-153">(If *pDefault* is **NULL**, then the access rights are PRINTER\_ACCESS\_USE.)</span></span>



| <span data-ttu-id="3c637-154">Valor de acesso desejado</span><span class="sxs-lookup"><span data-stu-id="3c637-154">Desired Access value</span></span>                        | <span data-ttu-id="3c637-155">Significado</span><span class="sxs-lookup"><span data-stu-id="3c637-155">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c637-156">acesso de impressora \_ \_ administrar</span><span class="sxs-lookup"><span data-stu-id="3c637-156">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="3c637-157">Para executar tarefas administrativas, como as fornecidas pelo [**Setprinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="3c637-157">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="3c637-158">\_uso de acesso à impressora \_</span><span class="sxs-lookup"><span data-stu-id="3c637-158">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="3c637-159">Para executar operações básicas de impressão.</span><span class="sxs-lookup"><span data-stu-id="3c637-159">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="3c637-160">\_todos os \_ acessos à impressora</span><span class="sxs-lookup"><span data-stu-id="3c637-160">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="3c637-161">Para executar todas as tarefas administrativas e operações básicas de impressão, exceto para sincronizar (consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="3c637-161">To perform all administrative tasks and basic printing operations except for SYNCHRONIZE (see [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                     |
| <span data-ttu-id="3c637-162">\_Gerenciamento de acesso à impressora \_ \_ limitado</span><span class="sxs-lookup"><span data-stu-id="3c637-162">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="3c637-163">Para executar tarefas administrativas, como as fornecidas por [**Setprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="3c637-163">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="3c637-164">Esse valor está disponível a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="3c637-164">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="3c637-165">valores de segurança genéricos, como gravar \_ DAC</span><span class="sxs-lookup"><span data-stu-id="3c637-165">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="3c637-166">Para permitir direitos de acesso de controle específico.</span><span class="sxs-lookup"><span data-stu-id="3c637-166">To allow specific control access rights.</span></span> <span data-ttu-id="3c637-167">Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="3c637-167">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="3c637-168">Se um usuário não tiver permissão para abrir uma impressora ou um servidor de impressão especificado com o acesso desejado, a chamada **OpenPrinter** falhará com um valor de retorno zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o valor de erro \_ acesso \_ negado.</span><span class="sxs-lookup"><span data-stu-id="3c637-168">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter** call will fail with a return value of zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

## <a name="examples"></a><span data-ttu-id="3c637-169">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3c637-169">Examples</span></span>

<span data-ttu-id="3c637-170">Para obter um programa de exemplo que usa essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="3c637-170">For a sample program that uses this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c637-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c637-171">Requirements</span></span>



| <span data-ttu-id="3c637-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c637-172">Requirement</span></span> | <span data-ttu-id="3c637-173">Valor</span><span class="sxs-lookup"><span data-stu-id="3c637-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c637-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c637-174">Minimum supported client</span></span><br/> | <span data-ttu-id="3c637-175">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c637-175">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c637-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c637-176">Minimum supported server</span></span><br/> | <span data-ttu-id="3c637-177">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3c637-177">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c637-178">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3c637-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c637-179"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c637-179"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3c637-180">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3c637-180">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c637-181"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c637-181"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3c637-182">DLL</span><span class="sxs-lookup"><span data-stu-id="3c637-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c637-183"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3c637-183"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3c637-184">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3c637-184">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3c637-185">**OpenPrinterW** (Unicode) e **OpenPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3c637-185">**OpenPrinterW** (Unicode) and **OpenPrinterA** (ANSI)</span></span><br/>                                         |



## <a name="see-also"></a><span data-ttu-id="3c637-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c637-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c637-187">Impressão</span><span class="sxs-lookup"><span data-stu-id="3c637-187">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3c637-188">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3c637-188">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3c637-189">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="3c637-189">**WritePrinter**</span></span>](writeprinter.md)
</dt> <dt>

[<span data-ttu-id="3c637-190">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="3c637-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="3c637-191">**padrões de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="3c637-191">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="3c637-192">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="3c637-192">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="3c637-193">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="3c637-193">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="3c637-194">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3c637-194">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

