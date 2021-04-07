---
description: A função SetPrinterData define os dados de configuração para um servidor de impressão ou impressora.
ms.assetid: 16072de9-98fb-4ada-8216-180b64cf44c8
title: Função SetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterData
- SetPrinterDataA
- SetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 36af84fe665d68fd7996a0b81fbbf291314cc69e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828205"
---
# <a name="setprinterdata-function"></a><span data-ttu-id="d8c48-103">Função SetPrinterData</span><span class="sxs-lookup"><span data-stu-id="d8c48-103">SetPrinterData function</span></span>

<span data-ttu-id="d8c48-104">A função **SetPrinterData** define os dados de configuração para um servidor de impressão ou impressora.</span><span class="sxs-lookup"><span data-stu-id="d8c48-104">The **SetPrinterData** function sets the configuration data for a printer or print server.</span></span>

<span data-ttu-id="d8c48-105">Para especificar a chave do registro sob a qual armazenar os dados, chame a função [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c48-105">To specify the registry key under which to store the data, call the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span> <span data-ttu-id="d8c48-106">Chamar **SetPrinterData** é equivalente a chamar a função **SetPrinterDataEx** com o parâmetro *pKeyName* definido como "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="d8c48-106">Calling **SetPrinterData** is equivalent to calling the **SetPrinterDataEx** function with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c48-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8c48-107">Syntax</span></span>


```C++
DWORD SetPrinterData(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pValueName,
  _In_ DWORD  Type,
  _In_ LPBYTE pData,
  _In_ DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="d8c48-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8c48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c48-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c48-110">Um identificador para a impressora ou o servidor de impressão para o qual a função define os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="d8c48-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="d8c48-111">Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="d8c48-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d8c48-112">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-112">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c48-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="d8c48-113">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="d8c48-114">Para impressoras, essa cadeia de caracteres é o nome de um valor de registro na chave "PrinterDriverData" da impressora no registro.</span><span class="sxs-lookup"><span data-stu-id="d8c48-114">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="d8c48-115">Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8c48-115">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d8c48-116">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c48-117">Um código que indica o tipo de dados para o qual o parâmetro *pData* aponta.</span><span class="sxs-lookup"><span data-stu-id="d8c48-117">A code that indicates the type of data that the *pData* parameter points to.</span></span> <span data-ttu-id="d8c48-118">Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="d8c48-118">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

</dd> <dt>

<span data-ttu-id="d8c48-119">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-119">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c48-120">Um ponteiro para uma matriz de bytes que contém os dados de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="d8c48-120">A pointer to an array of bytes that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="d8c48-121">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-121">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c48-122">O tamanho, em bytes, da matriz.</span><span class="sxs-lookup"><span data-stu-id="d8c48-122">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c48-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8c48-123">Return value</span></span>

<span data-ttu-id="d8c48-124">Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.</span><span class="sxs-lookup"><span data-stu-id="d8c48-124">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="d8c48-125">Se a função falhar, o valor de retorno será um valor de erro.</span><span class="sxs-lookup"><span data-stu-id="d8c48-125">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c48-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8c48-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d8c48-127">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d8c48-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d8c48-128">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d8c48-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d8c48-129">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="d8c48-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d8c48-130">Para recuperar os dados de configuração existentes de uma impressora, chame a função [**GetPrinterDataEx**](getprinterdataex.md) ou [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c48-130">To retrieve existing configuration data for a printer, call the [**GetPrinterDataEx**](getprinterdataex.md) or [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="d8c48-131">Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8c48-131">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="d8c48-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d8c48-132">Value</span></span>                                                               | <span data-ttu-id="d8c48-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8c48-133">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c48-134">**SPLREG \_ permitir que o \_ usuário \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="d8c48-134">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="d8c48-135">Windows XP com Service Pack 2 (SP2) e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-135">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="d8c48-136">Windows Server 2003 com Service Pack 1 (SP1) e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-136">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="d8c48-137">**aviso de SPLREG \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="d8c48-137">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-138">**SPLREG \_ o \_ diretório de spool padrão \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-138">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-139">**\_log de eventos do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-139">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-140">**\_ \_ pop-up do SPLREG net**</span><span class="sxs-lookup"><span data-stu-id="d8c48-140">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="d8c48-141">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-141">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="d8c48-142">**\_padrão de \_ prioridade de thread de porta SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-142">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-143">**\_prioridade de \_ thread de porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-143">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-144">**\_grupos de \_ isolamento do driver de impressão SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-144">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="d8c48-145">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-145">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="d8c48-146">**\_tempo de isolamento do driver de impressão SPLREG \_ antes da \_ \_ \_ \_ reciclagem**</span><span class="sxs-lookup"><span data-stu-id="d8c48-146">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="d8c48-147">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-147">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="d8c48-148">**\_isolamento do driver de impressão SPLREG máximo de \_ \_ \_ \_ objetos antes da \_ \_ reciclagem**</span><span class="sxs-lookup"><span data-stu-id="d8c48-148">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="d8c48-149">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-149">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="d8c48-150">**\_ \_ \_ \_ tempo limite de ociosidade do isolamento do driver de impressão SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-150">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="d8c48-151">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-151">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="d8c48-152">**\_política de \_ execução de isolamento do driver de impressão SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-152">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="d8c48-153">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-153">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="d8c48-154">**\_política de \_ substituição de isolamento do driver de impressão SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-154">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="d8c48-155">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-155">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="d8c48-156">**\_ \_ pop-up de repetição do SPLREG**</span><span class="sxs-lookup"><span data-stu-id="d8c48-156">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="d8c48-157">Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="d8c48-157">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="d8c48-158">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-158">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="d8c48-159">**\_prioridade de thread do Agendador SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-159">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-160">**\_padrão de prioridade de thread do Agendador SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-160">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="d8c48-161">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="d8c48-161">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="d8c48-162">Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="d8c48-162">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="d8c48-163">Os valores a seguir de valueName determinam o *comportamento de impressão* do pool quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="d8c48-163">The following values of *pValueName* determine the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="d8c48-164">Valor</span><span class="sxs-lookup"><span data-stu-id="d8c48-164">Value</span></span>                                       | <span data-ttu-id="d8c48-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8c48-165">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c48-166">**\_erro de reinicialização \_ de SPLREG \_ no \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="d8c48-166">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="d8c48-167">O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="d8c48-167">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="d8c48-168">Essa configuração é usada com **o \_ trabalho de reinicialização SPLREG \_ \_ no \_ pool \_ habilitado**.</span><span class="sxs-lookup"><span data-stu-id="d8c48-168">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="d8c48-169">**\_trabalho de reinicialização \_ de SPLREG \_ no \_ pool \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="d8c48-169">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="d8c48-170">Um valor diferente de zero em *pData* indica que o **\_ erro SPLREG reiniciar o \_ trabalho \_ no \_ pool \_** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="d8c48-170">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="d8c48-171">O tempo especificado em **SPLREG \_ reiniciar o \_ trabalho \_ no \_ pool \_** é um tempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="d8c48-171">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="d8c48-172">O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:</span><span class="sxs-lookup"><span data-stu-id="d8c48-172">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="d8c48-173">**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**</span><span class="sxs-lookup"><span data-stu-id="d8c48-173">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="d8c48-174">Chame a função [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para definir esses valores.</span><span class="sxs-lookup"><span data-stu-id="d8c48-174">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="d8c48-175">Configuração do monitor de porta</span><span class="sxs-lookup"><span data-stu-id="d8c48-175">Port monitor setting</span></span>     | <span data-ttu-id="d8c48-176">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d8c48-176">Data type</span></span>      | <span data-ttu-id="d8c48-177">Significado</span><span class="sxs-lookup"><span data-stu-id="d8c48-177">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c48-178">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="d8c48-178">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="d8c48-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8c48-179">**REG\_DWORD**</span></span> | <span data-ttu-id="d8c48-180">Se um valor diferente de zero, permite que o monitor de porta atualize o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="d8c48-180">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="d8c48-181">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="d8c48-181">**StatusUpdateInterval**</span></span> | <span data-ttu-id="d8c48-182">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8c48-182">**REG\_DWORD**</span></span> | <span data-ttu-id="d8c48-183">Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="d8c48-183">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="d8c48-184">No Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão.</span><span class="sxs-lookup"><span data-stu-id="d8c48-184">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="d8c48-185">A renderização do lado do cliente de trabalhos de impressão pode ser configurada para cada impressora definindo os valores a *seguir em valores* de valor.</span><span class="sxs-lookup"><span data-stu-id="d8c48-185">Client-side rendering of a print jobs can be configured for each printer by setting the following values in *pValueName*.</span></span>



| <span data-ttu-id="d8c48-186">Configuração</span><span class="sxs-lookup"><span data-stu-id="d8c48-186">Setting</span></span>                      | <span data-ttu-id="d8c48-187">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d8c48-187">Data type</span></span>      | <span data-ttu-id="d8c48-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8c48-188">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c48-189">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="d8c48-189">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="d8c48-190">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8c48-190">**REG\_DWORD**</span></span> | <span data-ttu-id="d8c48-191">Um valor de 0, ou se esse valor não estiver presente no registro, habilitará a renderização padrão do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="d8c48-191">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="d8c48-192">Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="d8c48-192">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                      |
| <span data-ttu-id="d8c48-193">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="d8c48-193">**ForceClientSideRendering**</span></span> | <span data-ttu-id="d8c48-194">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d8c48-194">**REG\_DWORD**</span></span> | <span data-ttu-id="d8c48-195">Um valor de 0 ou, se esse valor não estiver presente no registro, fará com que os trabalhos de impressão sejam renderizados no cliente.</span><span class="sxs-lookup"><span data-stu-id="d8c48-195">A value of 0, or if this value is not present in the registry, causes the print jobs to be rendered on the client.</span></span> <span data-ttu-id="d8c48-196">Se um trabalho de impressão não puder ser processado no cliente, ele será renderizado no servidor.</span><span class="sxs-lookup"><span data-stu-id="d8c48-196">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="d8c48-197">Se não for possível renderizar um trabalho de impressão no servidor, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="d8c48-197">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="d8c48-198">Um valor de 1 processará trabalhos de impressão no cliente.</span><span class="sxs-lookup"><span data-stu-id="d8c48-198">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="d8c48-199">Se não for possível renderizar um trabalho de impressão no cliente, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="d8c48-199">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8c48-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8c48-200">Requirements</span></span>



| <span data-ttu-id="d8c48-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8c48-201">Requirement</span></span> | <span data-ttu-id="d8c48-202">Valor</span><span class="sxs-lookup"><span data-stu-id="d8c48-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c48-203">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8c48-203">Minimum supported client</span></span><br/> | <span data-ttu-id="d8c48-204">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d8c48-205">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8c48-205">Minimum supported server</span></span><br/> | <span data-ttu-id="d8c48-206">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d8c48-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8c48-207">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d8c48-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8c48-208"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c48-208"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d8c48-209">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8c48-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8c48-210"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8c48-210"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d8c48-211">DLL</span><span class="sxs-lookup"><span data-stu-id="d8c48-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8c48-212"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d8c48-212"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d8c48-213">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="d8c48-213">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d8c48-214">**SetPrinterDataW** (Unicode) e **SetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d8c48-214">**SetPrinterDataW** (Unicode) and **SetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="d8c48-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8c48-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c48-216">Impressão</span><span class="sxs-lookup"><span data-stu-id="d8c48-216">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d8c48-217">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="d8c48-217">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d8c48-218">**Getprinter**</span><span class="sxs-lookup"><span data-stu-id="d8c48-218">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="d8c48-219">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="d8c48-219">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> <dt>

[<span data-ttu-id="d8c48-220">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="d8c48-220">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="d8c48-221">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d8c48-221">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d8c48-222">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="d8c48-222">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

