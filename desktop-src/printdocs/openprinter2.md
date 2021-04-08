---
description: Recupera um identificador para a impressora especificada, o servidor de impressão ou outros tipos de identificadores no subsistema de impressão, enquanto define algumas das opções de impressora.
ms.assetid: e2370ae4-4475-4ccc-a6f9-3d33d1370054
title: Função OpenPrinter2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OpenPrinter2
- OpenPrinter2A
- OpenPrinter2W
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 46788d7ad810ef623cd77793a72ab6c046b73590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828764"
---
# <a name="openprinter2-function"></a><span data-ttu-id="4d06c-103">Função OpenPrinter2</span><span class="sxs-lookup"><span data-stu-id="4d06c-103">OpenPrinter2 function</span></span>

<span data-ttu-id="4d06c-104">Recupera um identificador para a impressora especificada, o servidor de impressão ou outros tipos de identificadores no subsistema de impressão, enquanto define algumas das opções de impressora.</span><span class="sxs-lookup"><span data-stu-id="4d06c-104">Retrieves a handle to the specified printer, print server, or other types of handles in the print subsystem, while setting some of the printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d06c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d06c-105">Syntax</span></span>


```C++
BOOL OpenPrinter2(
  _In_  LPCTSTR            pPrinterName,
  _Out_ LPHANDLE           phPrinter,
  _In_  LPPRINTER_DEFAULTS pDefault,
  _In_  PPRINTER_OPTIONS   pOptions
);
```



## <a name="parameters"></a><span data-ttu-id="4d06c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d06c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d06c-107">*pPrinterName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d06c-107">*pPrinterName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d06c-108">Um ponteiro para uma cadeia de caracteres constante terminada em nulo que especifica o nome da impressora ou do servidor de impressão, o objeto de impressora, o XcvMonitor ou o XcvPort.</span><span class="sxs-lookup"><span data-stu-id="4d06c-108">A pointer to a constant null-terminated string that specifies the name of the printer or print server, the printer object, the XcvMonitor, or the XcvPort.</span></span>

<span data-ttu-id="4d06c-109">Para um objeto de impressora, use: PrinterName, trabalho xxxx.</span><span class="sxs-lookup"><span data-stu-id="4d06c-109">For a printer object, use: PrinterName,Job xxxx.</span></span> <span data-ttu-id="4d06c-110">Para um XcvMonitor, use: nomedoservidor, XcvMonitor Monitorname.</span><span class="sxs-lookup"><span data-stu-id="4d06c-110">For an XcvMonitor, use: ServerName,XcvMonitor MonitorName.</span></span> <span data-ttu-id="4d06c-111">Para um XcvPort, use: nomedoservidor, XcvPort PortName.</span><span class="sxs-lookup"><span data-stu-id="4d06c-111">For an XcvPort, use: ServerName,XcvPort PortName.</span></span>

<span data-ttu-id="4d06c-112">**Windows Vista:** Se for **NULL**, indicará o servidor de impressão local.</span><span class="sxs-lookup"><span data-stu-id="4d06c-112">**Windows Vista:** If **NULL**, it indicates the local print server.</span></span>

</dd> <dt>

<span data-ttu-id="4d06c-113">*phPrinter* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4d06c-113">*phPrinter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d06c-114">Um ponteiro para uma variável que recebe um identificador para o objeto de impressora aberta ou de servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="4d06c-114">A pointer to a variable that receives a handle to the open printer or print server object.</span></span>

</dd> <dt>

<span data-ttu-id="4d06c-115">*pDefault* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d06c-115">*pDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d06c-116">Um ponteiro para uma estrutura de [**\_ padrões de impressora**](printer-defaults.md) .</span><span class="sxs-lookup"><span data-stu-id="4d06c-116">A pointer to a [**PRINTER\_DEFAULTS**](printer-defaults.md) structure.</span></span> <span data-ttu-id="4d06c-117">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4d06c-117">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4d06c-118">*pOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4d06c-118">*pOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d06c-119">Um ponteiro para uma estrutura de [**\_ Opções de impressora**](printer-options.md) .</span><span class="sxs-lookup"><span data-stu-id="4d06c-119">A pointer to a [**PRINTER\_OPTIONS**](printer-options.md) structure.</span></span> <span data-ttu-id="4d06c-120">Esse valor pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4d06c-120">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d06c-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d06c-121">Return value</span></span>

<span data-ttu-id="4d06c-122">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4d06c-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4d06c-123">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="4d06c-123">If the function fails, the return value is zero.</span></span> <span data-ttu-id="4d06c-124">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="4d06c-124">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="4d06c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d06c-125">Remarks</span></span>

<span data-ttu-id="4d06c-126">Não chame esse método em [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="4d06c-126">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="4d06c-127">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="4d06c-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4d06c-128">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4d06c-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4d06c-129">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="4d06c-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4d06c-130">A versão ANSI dessa função não foi implementada e \_ não \_ há suporte para o erro.</span><span class="sxs-lookup"><span data-stu-id="4d06c-130">The ANSI version of this function is not implemented and returns ERROR\_NOT\_SUPPORTED.</span></span>

<span data-ttu-id="4d06c-131">O parâmetro *pDefault* permite que você especifique o tipo de dados e os valores do modo de dispositivo que são usados para imprimir documentos enviados pela função [**StartDocPrinter**](startdocprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="4d06c-131">The *pDefault* parameter enables you to specify the data type and device mode values that are used for printing documents submitted by the [**StartDocPrinter**](startdocprinter.md) function.</span></span> <span data-ttu-id="4d06c-132">No entanto, você pode substituir esses valores usando a função [**SetJob**](setjob.md) depois que um documento for iniciado.</span><span class="sxs-lookup"><span data-stu-id="4d06c-132">However, you can override these values by using the [**SetJob**](setjob.md) function after a document has been started.</span></span>

<span data-ttu-id="4d06c-133">Você pode chamar a função **OpenPrinter2** para abrir um identificador para um servidor de impressão ou para determinar os direitos de acesso do cliente a um servidor de impressão.</span><span class="sxs-lookup"><span data-stu-id="4d06c-133">You can call the **OpenPrinter2** function to open a handle to a print server or to determine client access rights to a print server.</span></span> <span data-ttu-id="4d06c-134">Para fazer isso, especifique o nome do servidor de impressão no parâmetro *pPrinterName* , defina os membros **pDatatype** e **PDevMode** da estrutura [**\_ padrões da impressora**](printer-defaults.md) como **NULL** e defina o membro **desiredAccess** para especificar um valor de máscara de acesso do servidor, como servidor \_ todo \_ acesso.</span><span class="sxs-lookup"><span data-stu-id="4d06c-134">To do this, specify the name of the print server in the *pPrinterName* parameter, set the **pDatatype** and **pDevMode** members of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to **NULL**, and set the **DesiredAccess** member to specify a server access mask value such as SERVER\_ALL\_ACCESS.</span></span> <span data-ttu-id="4d06c-135">Quando você terminar com o identificador, passe-o para a função [**ClosePrinter**](closeprinter.md) para fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="4d06c-135">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="4d06c-136">Use o membro **desiredAccess** da estrutura [**\_ padrões da impressora**](printer-defaults.md) para especificar os direitos de acesso necessários.</span><span class="sxs-lookup"><span data-stu-id="4d06c-136">Use the **DesiredAccess** member of the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure to specify the necessary access rights.</span></span> <span data-ttu-id="4d06c-137">Os direitos de acesso podem ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="4d06c-137">The access rights can be one of the following.</span></span>



| <span data-ttu-id="4d06c-138">Valor de acesso desejado</span><span class="sxs-lookup"><span data-stu-id="4d06c-138">Desired Access value</span></span>                        | <span data-ttu-id="4d06c-139">Significado</span><span class="sxs-lookup"><span data-stu-id="4d06c-139">Meaning</span></span>                                                                                                                                                                                      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d06c-140">acesso de impressora \_ \_ administrar</span><span class="sxs-lookup"><span data-stu-id="4d06c-140">PRINTER\_ACCESS\_ADMINISTER</span></span>                 | <span data-ttu-id="4d06c-141">Para executar tarefas administrativas, como as fornecidas pelo [**Setprinter**](setprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4d06c-141">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md).</span></span>                                                                                                 |
| <span data-ttu-id="4d06c-142">\_uso de acesso à impressora \_</span><span class="sxs-lookup"><span data-stu-id="4d06c-142">PRINTER\_ACCESS\_USE</span></span>                        | <span data-ttu-id="4d06c-143">Para executar operações básicas de impressão.</span><span class="sxs-lookup"><span data-stu-id="4d06c-143">To perform basic printing operations.</span></span>                                                                                                                                                        |
| <span data-ttu-id="4d06c-144">\_todos os \_ acessos à impressora</span><span class="sxs-lookup"><span data-stu-id="4d06c-144">PRINTER\_ALL\_ACCESS</span></span>                        | <span data-ttu-id="4d06c-145">Para executar todas as tarefas administrativas e operações básicas de impressão, exceto sincronizar.</span><span class="sxs-lookup"><span data-stu-id="4d06c-145">To perform all administrative tasks and basic printing operations except SYNCHRONIZE.</span></span> <span data-ttu-id="4d06c-146">Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="4d06c-146">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                         |
| <span data-ttu-id="4d06c-147">\_Gerenciamento de acesso à impressora \_ \_ limitado</span><span class="sxs-lookup"><span data-stu-id="4d06c-147">PRINTER\_ACCESS\_MANAGE\_LIMITED</span></span>            | <span data-ttu-id="4d06c-148">Para executar tarefas administrativas, como as fornecidas por [**Setprinter**](setprinter.md) e [**SetPrinterData**](setprinterdata.md).</span><span class="sxs-lookup"><span data-stu-id="4d06c-148">To perform administrative tasks, such as those provided by [**SetPrinter**](setprinter.md) and [**SetPrinterData**](setprinterdata.md).</span></span> <span data-ttu-id="4d06c-149">Esse valor está disponível a partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="4d06c-149">This value is available starting from Windows 8.1.</span></span> |
| <span data-ttu-id="4d06c-150">valores de segurança genéricos, como gravar \_ DAC</span><span class="sxs-lookup"><span data-stu-id="4d06c-150">generic security values, such as WRITE\_DAC</span></span> | <span data-ttu-id="4d06c-151">Para permitir direitos de acesso de controle específico.</span><span class="sxs-lookup"><span data-stu-id="4d06c-151">To allow specific control access rights.</span></span> <span data-ttu-id="4d06c-152">Consulte [direitos de acesso padrão](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="4d06c-152">See [Standard Access Rights](/windows/desktop/SecAuthZ/standard-access-rights).</span></span>                                                                                      |



 

<span data-ttu-id="4d06c-153">Se um usuário não tiver permissão para abrir uma impressora ou servidor de impressão especificado com o acesso desejado, a chamada **OpenPrinter2** falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o valor erro \_ acesso \_ negado.</span><span class="sxs-lookup"><span data-stu-id="4d06c-153">If a user does not have permission to open a specified printer or print server with the desired access, the **OpenPrinter2** call will fail, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the value ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="4d06c-154">Quando *pPrinterName* é uma impressora local, o **OpenPrinter2** ignora todos os valores do **dwFlags** que a estrutura [**de \_ Opções de impressora**](printer-options.md) apontou para usar o *pOptions*, exceto a opção de impressora do \_ \_ cliente \_ mudar.</span><span class="sxs-lookup"><span data-stu-id="4d06c-154">When *pPrinterName* is a local printer, then **OpenPrinter2** ignores all values of the **dwFlags** that the [**PRINTER\_OPTIONS**](printer-options.md) structure pointed to using *pOptions*, except PRINTER\_OPTION\_CLIENT\_CHANGE.</span></span> <span data-ttu-id="4d06c-155">Se o último for passado, **OpenPrinter2** retornará um erro de \_ acesso \_ negado.</span><span class="sxs-lookup"><span data-stu-id="4d06c-155">If the latter is passed, then **OpenPrinter2** will return ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="4d06c-156">Da mesma forma, ao abrir uma impressora local, o **OpenPrinter2** não oferece nenhuma vantagem sobre [**OpenPrinter**](openprinter.md).</span><span class="sxs-lookup"><span data-stu-id="4d06c-156">Accordingly, when opening a local printer, **OpenPrinter2** provides no advantage over [**OpenPrinter**](openprinter.md).</span></span>

<span data-ttu-id="4d06c-157">**Windows Vista:** Os dados de impressora retornados por **OpenPrinter2** são recuperados de um cache local, a menos que a **opção de impressora sem sinalizador de \_ \_ \_ cache** esteja definida no campo **dwFlags** da estrutura de [**\_ Opções de impressora**](printer-options.md) referenciada por *pOptions*.</span><span class="sxs-lookup"><span data-stu-id="4d06c-157">**Windows Vista:** The printer data returned by **OpenPrinter2** is retrieved from a local cache unless the **PRINTER\_OPTION\_NO\_CACHE** flag is set in the **dwFlags** field of the [**PRINTER\_OPTIONS**](printer-options.md) structure referenced by *pOptions*.</span></span>

## <a name="examples"></a><span data-ttu-id="4d06c-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d06c-158">Examples</span></span>

<span data-ttu-id="4d06c-159">Neste exemplo, **OpenPrinter2** falha quando o \_ acesso à impressora \_ Gerenciar \_ limitado é passado para a estrutura de [**\_ padrões de impressora**](printer-defaults.md) e o usuário não tem a permissão apropriada.</span><span class="sxs-lookup"><span data-stu-id="4d06c-159">In this example, **OpenPrinter2** fails when PRINTER\_ACCESS\_MANAGE\_LIMITED is passed to the [**PRINTER\_DEFAULTS**](printer-defaults.md) structure, and the user does not have the appropriate permission.</span></span>


```C++
// Specify the limited management permission.
PRINTER_DEFAULTS defaults = {};
defaults.DesiredAccess = PRINTER_ACCESS_MANAGE_LIMITED;

// Open a printer to which the user has no administrative rights.
HANDLE printer = nullptr;
assert(!OpenPrinter2(L QueueWithNoAdminRights , // Queue name
                     &printer,                  // Printer handle
                     &defaults,                 // Printer defaults
                     nullptr));                 // Printer options

assert(GetLastError() == ERROR_ACCESS_DENIED);

if (printer)
{
    ClosePrinter(printer);
}
```



<span data-ttu-id="4d06c-160">Para um programa de exemplo que mostra como usar essa função, consulte [como imprimir usando a API de impressão GDI](how-to--print-using-the-gdi-print-api.md).</span><span class="sxs-lookup"><span data-stu-id="4d06c-160">For a sample program that shows how to use this function, see [How To: Print Using the GDI Print API](how-to--print-using-the-gdi-print-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d06c-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d06c-161">Requirements</span></span>



| <span data-ttu-id="4d06c-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d06c-162">Requirement</span></span> | <span data-ttu-id="4d06c-163">Valor</span><span class="sxs-lookup"><span data-stu-id="4d06c-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d06c-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d06c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="4d06c-165">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d06c-165">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4d06c-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d06c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="4d06c-167">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d06c-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4d06c-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d06c-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d06c-169"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d06c-169"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4d06c-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4d06c-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d06c-171"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d06c-171"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4d06c-172">DLL</span><span class="sxs-lookup"><span data-stu-id="4d06c-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d06c-173"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d06c-173"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="4d06c-174">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4d06c-174">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4d06c-175">**OpenPrinter2W** (Unicode) e **OpenPrinter2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4d06c-175">**OpenPrinter2W** (Unicode) and **OpenPrinter2A** (ANSI)</span></span><br/>                                       |



## <a name="see-also"></a><span data-ttu-id="4d06c-176">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d06c-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d06c-177">Impressão</span><span class="sxs-lookup"><span data-stu-id="4d06c-177">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4d06c-178">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="4d06c-178">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4d06c-179">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="4d06c-179">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="4d06c-180">**padrões de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="4d06c-180">**PRINTER\_DEFAULTS**</span></span>](printer-defaults.md)
</dt> <dt>

[<span data-ttu-id="4d06c-181">**opções de impressora \_**</span><span class="sxs-lookup"><span data-stu-id="4d06c-181">**PRINTER\_OPTIONS**</span></span>](printer-options.md)
</dt> <dt>

[<span data-ttu-id="4d06c-182">**SetJob**</span><span class="sxs-lookup"><span data-stu-id="4d06c-182">**SetJob**</span></span>](setjob.md)
</dt> <dt>

[<span data-ttu-id="4d06c-183">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="4d06c-183">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="4d06c-184">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="4d06c-184">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="4d06c-185">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4d06c-185">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

