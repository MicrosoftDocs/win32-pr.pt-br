---
description: A função SetPrinterDataEx define os dados de configuração para um servidor de impressão ou impressora. A função armazena os dados de configuração na chave do registro de impressoras.
ms.assetid: b7faadfc-1c81-4ddf-8fe5-68f4cc0376f1
title: Função SetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPrinterDataEx
- SetPrinterDataExA
- SetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 9f384c9c9d6f0d956264b45ec8b52043ad20e897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171327"
---
# <a name="setprinterdataex-function"></a><span data-ttu-id="f46e4-104">Função SetPrinterDataEx</span><span class="sxs-lookup"><span data-stu-id="f46e4-104">SetPrinterDataEx function</span></span>

<span data-ttu-id="f46e4-105">A função **SetPrinterDataEx** define os dados de configuração para um servidor de impressão ou impressora.</span><span class="sxs-lookup"><span data-stu-id="f46e4-105">The **SetPrinterDataEx** function sets the configuration data for a printer or print server.</span></span> <span data-ttu-id="f46e4-106">A função armazena os dados de configuração na chave do registro da impressora.</span><span class="sxs-lookup"><span data-stu-id="f46e4-106">The function stores the configuration data under the printer's registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="f46e4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f46e4-107">Syntax</span></span>


```C++
DWORD SetPrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName,
  _In_ DWORD   Type,
  _In_ LPBYTE  pData,
  _In_ DWORD   cbData
);
```



## <a name="parameters"></a><span data-ttu-id="f46e4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f46e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f46e4-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46e4-110">Um identificador para a impressora ou o servidor de impressão para o qual a função define os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="f46e4-110">A handle to the printer or print server for which the function sets configuration data.</span></span> <span data-ttu-id="f46e4-111">Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="f46e4-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f46e4-112">*pKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46e4-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém o valor a ser definido.</span><span class="sxs-lookup"><span data-stu-id="f46e4-113">A pointer to a null-terminated string that specifies the key containing the value to set.</span></span> <span data-ttu-id="f46e4-114">Se a chave ou subchaves especificadas não existirem, a função as criará.</span><span class="sxs-lookup"><span data-stu-id="f46e4-114">If the specified key or subkeys do not exist, the function creates them.</span></span>

<span data-ttu-id="f46e4-115">Para armazenar os dados de configuração que podem ser publicados no serviço de diretório (DS), especifique uma das seguintes chaves de registro predefinidas.</span><span class="sxs-lookup"><span data-stu-id="f46e4-115">To store configuration data that can be published in the directory service (DS), specify one of the following predefined registry keys.</span></span>



| <span data-ttu-id="f46e4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f46e4-116">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="f46e4-117">Significado</span><span class="sxs-lookup"><span data-stu-id="f46e4-117">Meaning</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="SPLDS_DRIVER_KEY"></span><span id="splds_driver_key"></span><dl> <span data-ttu-id="f46e4-118"><dt>**SPLDS_DRIVER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="f46e4-118"><dt>**SPLDS_DRIVER_KEY**</dt></span></span> </dl>    | <span data-ttu-id="f46e4-119">Os drivers de impressora usam essa chave para armazenar as propriedades do driver.</span><span class="sxs-lookup"><span data-stu-id="f46e4-119">Printer drivers use this key to store driver properties.</span></span><br/>                             |
| <span id="SPLDS_SPOOLER_KEY"></span><span id="splds_spooler_key"></span><dl> <span data-ttu-id="f46e4-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="f46e4-120"><dt>**SPLDS_SPOOLER_KEY**</dt></span></span> </dl> | <span data-ttu-id="f46e4-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f46e4-121">Reserved.</span></span> <span data-ttu-id="f46e4-122">Usado somente pelo spooler de impressão para armazenar propriedades internas do spooler.</span><span class="sxs-lookup"><span data-stu-id="f46e4-122">Used only by the print spooler to store internal spooler properties.</span></span><br/>       |
| <span id="SPLDS_USER_KEY"></span><span id="splds_user_key"></span><dl> <span data-ttu-id="f46e4-123"><dt>**SPLDS_USER_KEY**</dt></span><span class="sxs-lookup"><span data-stu-id="f46e4-123"><dt>**SPLDS_USER_KEY**</dt></span></span> </dl>          | <span data-ttu-id="f46e4-124">Os aplicativos usam essa chave para armazenar propriedades de impressora, como números de ativos de impressora.</span><span class="sxs-lookup"><span data-stu-id="f46e4-124">Applications use this key to store printer properties such as printer asset numbers.</span></span><br/> |



 

<span data-ttu-id="f46e4-125">Os valores armazenados na chave de SPLDS_USER_KEY serão publicados no serviço de diretório somente se houver uma propriedade correspondente no esquema.</span><span class="sxs-lookup"><span data-stu-id="f46e4-125">Values that are stored under the SPLDS_USER_KEY key are published in the directory service only if there is a corresponding property in the schema.</span></span> <span data-ttu-id="f46e4-126">Um administrador de domínio deve criar a propriedade se ela ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="f46e4-126">A domain administrator must create the property if it doesn't already exist.</span></span> <span data-ttu-id="f46e4-127">Para publicar uma propriedade definida pelo usuário depois de usar **SetPrinterDataEx** para adicionar ou alterar um valor, chame [**setprinter**](setprinter.md) com *Level* = 7 e com o membro **dwAction** de [**PRINTER_INFO_7**](printer-info-7.md) definido como **DSPRINT_UPDATE**.</span><span class="sxs-lookup"><span data-stu-id="f46e4-127">To publish a user-defined property after you use **SetPrinterDataEx** to add or change a value, call [**SetPrinter**](setprinter.md) with *Level* = 7 and with the **dwAction** member of [**PRINTER_INFO_7**](printer-info-7.md) set to **DSPRINT_UPDATE**.</span></span>

<span data-ttu-id="f46e4-128">Você pode especificar outras chaves para armazenar dados de configuração não DS.</span><span class="sxs-lookup"><span data-stu-id="f46e4-128">You can specify other keys to store non-DS configuration data.</span></span> <span data-ttu-id="f46e4-129">Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho que tenha uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="f46e4-129">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="f46e4-130">Se *hPrinter* for um identificador para uma impressora e *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **SetPrinterDataEx** retornará **ERROR_INVALID_PARAMETER**.</span><span class="sxs-lookup"><span data-stu-id="f46e4-130">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **SetPrinterDataEx** returns **ERROR_INVALID_PARAMETER**.</span></span>

<span data-ttu-id="f46e4-131">Se *hPrinter* for um identificador para um servidor de impressão, *pKeyName* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="f46e4-131">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

<span data-ttu-id="f46e4-132">Não use **SPLDS_SPOOLER_KEY**.</span><span class="sxs-lookup"><span data-stu-id="f46e4-132">Do not use **SPLDS_SPOOLER_KEY**.</span></span> <span data-ttu-id="f46e4-133">Para alterar as propriedades da impressora do spooler, use [**Setprinter**](setprinter.md) com o *nível* = 2.</span><span class="sxs-lookup"><span data-stu-id="f46e4-133">To change the spooler printer properties, use [**SetPrinter**](setprinter.md) with *Level* = 2.</span></span>

</dd> <dt>

<span data-ttu-id="f46e4-134">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-134">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46e4-135">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="f46e4-135">A pointer to a null-terminated string that identifies the data to set.</span></span>

<span data-ttu-id="f46e4-136">Para impressoras, essa cadeia de caracteres especifica o nome de um valor na chave *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="f46e4-136">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="f46e4-137">Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="f46e4-137">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="f46e4-138">*Tipo* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-138">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46e4-139">Um código que indica o tipo de dados apontado pelo parâmetro *pData* .</span><span class="sxs-lookup"><span data-stu-id="f46e4-139">A code indicating the type of data pointed to by the *pData* parameter.</span></span> <span data-ttu-id="f46e4-140">Para obter uma lista dos possíveis códigos de tipo, consulte [tipos de valor do registro](/windows/desktop/SysInfo/registry-value-types).</span><span class="sxs-lookup"><span data-stu-id="f46e4-140">For a list of the possible type codes, see [Registry Value Types](/windows/desktop/SysInfo/registry-value-types).</span></span>

<span data-ttu-id="f46e4-141">Se *pKeyName* especificar uma das chaves de serviço de diretório predefinidas, o *tipo* deverá ser **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD** ou **REG_BINARY**.</span><span class="sxs-lookup"><span data-stu-id="f46e4-141">If *pKeyName* specifies one of the predefined directory service keys, *Type* must be **REG_SZ**, **REG_MULTI_SZ**, **REG_DWORD**, or **REG_BINARY**.</span></span> <span data-ttu-id="f46e4-142">Se **REG_BINARY** for usado, *cbData* deverá ser igual a 1 e o serviço de diretório tratará os dados como um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="f46e4-142">If **REG_BINARY** is used, *cbData* must be equal to 1, and the directory service treats the data as a Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="f46e4-143">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46e4-144">Um ponteiro para um buffer que contém os dados de configuração da impressora.</span><span class="sxs-lookup"><span data-stu-id="f46e4-144">A pointer to a buffer that contains the printer configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="f46e4-145">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-145">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f46e4-146">O tamanho, em bytes, da matriz.</span><span class="sxs-lookup"><span data-stu-id="f46e4-146">The size, in bytes, of the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f46e4-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f46e4-147">Return value</span></span>

<span data-ttu-id="f46e4-148">Se a função for realizada com sucesso, o valor de retorno será **ERROR_SUCCESS**.</span><span class="sxs-lookup"><span data-stu-id="f46e4-148">If the function succeeds, the return value is **ERROR_SUCCESS**.</span></span>

<span data-ttu-id="f46e4-149">Se a função falhar, o valor de retorno será um valor de erro.</span><span class="sxs-lookup"><span data-stu-id="f46e4-149">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f46e4-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="f46e4-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f46e4-151">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f46e4-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f46e4-152">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f46e4-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f46e4-153">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="f46e4-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f46e4-154">Para recuperar dados de configuração existentes para uma impressora ou spooler de impressão, chame a função [**GetPrinterDataEx**](getprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="f46e4-154">To retrieve existing configuration data for a printer or print spooler, call the [**GetPrinterDataEx**](getprinterdataex.md) function.</span></span>

<span data-ttu-id="f46e4-155">Chamar **SetPrinterDataEx** com o parâmetro *pKeyName* definido como "PrinterDriverData" é equivalente a chamar a função [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f46e4-155">Calling **SetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="f46e4-156">Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="f46e4-156">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="f46e4-157">Valor</span><span class="sxs-lookup"><span data-stu-id="f46e4-157">Value</span></span>                                                               | <span data-ttu-id="f46e4-158">Comentários</span><span class="sxs-lookup"><span data-stu-id="f46e4-158">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46e4-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="f46e4-159">**SPLREG_ALLOW_USER_MANAGEFORMS**</span></span>                                | <span data-ttu-id="f46e4-160">Windows XP com Service Pack 2 (SP2) e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-160">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="f46e4-161">Windows Server 2003 com Service Pack 1 (SP1) e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-161">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="f46e4-162">**SPLREG_BEEP_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="f46e4-162">**SPLREG_BEEP_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span><span class="sxs-lookup"><span data-stu-id="f46e4-163">**SPLREG_DEFAULT_SPOOL_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-164">**SPLREG_EVENT_LOG**</span><span class="sxs-lookup"><span data-stu-id="f46e4-164">**SPLREG_EVENT_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-165">**SPLREG_NET_POPUP**</span><span class="sxs-lookup"><span data-stu-id="f46e4-165">**SPLREG_NET_POPUP**</span></span>                                              | <span data-ttu-id="f46e4-166">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-166">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="f46e4-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f46e4-167">**SPLREG_PORT_THREAD_PRIORITY_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-168">**SPLREG_PORT_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="f46e4-168">**SPLREG_PORT_THREAD_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span><span class="sxs-lookup"><span data-stu-id="f46e4-169">**SPLREG_PRINT_DRIVER_ISOLATION_GROUPS**</span></span>                        | <span data-ttu-id="f46e4-170">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f46e4-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="f46e4-171">**SPLREG_PRINT_DRIVER_ISOLATION_TIME_BEFORE_RECYCLE**</span></span>         | <span data-ttu-id="f46e4-172">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f46e4-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span><span class="sxs-lookup"><span data-stu-id="f46e4-173">**SPLREG_PRINT_DRIVER_ISOLATION_MAX_OBJECTS_BEFORE_RECYCLE**</span></span> | <span data-ttu-id="f46e4-174">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f46e4-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span><span class="sxs-lookup"><span data-stu-id="f46e4-175">**SPLREG_PRINT_DRIVER_ISOLATION_IDLE_TIMEOUT**</span></span>                 | <span data-ttu-id="f46e4-176">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f46e4-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span><span class="sxs-lookup"><span data-stu-id="f46e4-177">**SPLREG_PRINT_DRIVER_ISOLATION_EXECUTION_POLICY**</span></span>             | <span data-ttu-id="f46e4-178">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f46e4-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span><span class="sxs-lookup"><span data-stu-id="f46e4-179">**SPLREG_PRINT_DRIVER_ISOLATION_OVERRIDE_POLICY**</span></span>              | <span data-ttu-id="f46e4-180">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="f46e4-181">**SPLREG_RETRY_POPUP**</span><span class="sxs-lookup"><span data-stu-id="f46e4-181">**SPLREG_RETRY_POPUP**</span></span>                                            | <span data-ttu-id="f46e4-182">Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="f46e4-182">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="f46e4-183">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-183">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="f46e4-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="f46e4-184">**SPLREG_SCHEDULER_THREAD_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f46e4-185">**SPLREG_SCHEDULER_THREAD_PRIORITY_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="f46e4-186">**SPLREG_WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="f46e4-186">**SPLREG_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="f46e4-187">Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="f46e4-187">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="f46e4-188">A passagem de um dos valores predefinidos a *seguir, como o valor de* valueName, define o comportamento de impressão do pool quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="f46e4-188">Passing one of the following predefined values as *pValueName* sets the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="f46e4-189">Valor</span><span class="sxs-lookup"><span data-stu-id="f46e4-189">Value</span></span>                                       | <span data-ttu-id="f46e4-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="f46e4-190">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46e4-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span><span class="sxs-lookup"><span data-stu-id="f46e4-191">**SPLREG_RESTART_JOB_ON_POOL_ERROR**</span></span>   | <span data-ttu-id="f46e4-192">O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="f46e4-192">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="f46e4-193">Essa configuração é usada com **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span><span class="sxs-lookup"><span data-stu-id="f46e4-193">This setting is used with **SPLREG_RESTART_JOB_ON_POOL_ENABLED**.</span></span><br/> |
| <span data-ttu-id="f46e4-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="f46e4-194">**SPLREG_RESTART_JOB_ON_POOL_ENABLED**</span></span> | <span data-ttu-id="f46e4-195">Um valor diferente de zero em *pData* indica que **SPLREG_RESTART_JOB_ON_POOL_ERROR** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f46e4-195">A nonzero value in *pData* indicates that **SPLREG_RESTART_JOB_ON_POOL_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="f46e4-196">O tempo especificado em **SPLREG_RESTART_JOB_ON_POOL_ERROR** é um tempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="f46e4-196">The time specified in **SPLREG_RESTART_JOB_ON_POOL_ERROR** is a minimum time.</span></span> <span data-ttu-id="f46e4-197">O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:</span><span class="sxs-lookup"><span data-stu-id="f46e4-197">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="f46e4-198">**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**</span><span class="sxs-lookup"><span data-stu-id="f46e4-198">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="f46e4-199">Chame a função [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) para definir esses valores.</span><span class="sxs-lookup"><span data-stu-id="f46e4-199">Call the [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) function to set these values.</span></span>



| <span data-ttu-id="f46e4-200">Configuração do monitor de porta</span><span class="sxs-lookup"><span data-stu-id="f46e4-200">Port monitor setting</span></span>     | <span data-ttu-id="f46e4-201">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f46e4-201">Data type</span></span>      | <span data-ttu-id="f46e4-202">Significado</span><span class="sxs-lookup"><span data-stu-id="f46e4-202">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46e4-203">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="f46e4-203">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="f46e4-204">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="f46e4-204">**REG_DWORD**</span></span> | <span data-ttu-id="f46e4-205">Se um valor diferente de zero, permite que o monitor de porta atualize o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="f46e4-205">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="f46e4-206">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="f46e4-206">**StatusUpdateInterval**</span></span> | <span data-ttu-id="f46e4-207">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="f46e4-207">**REG_DWORD**</span></span> | <span data-ttu-id="f46e4-208">Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="f46e4-208">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="f46e4-209">Para garantir que o spooler redirecione trabalhos para a próxima impressora disponível no pool (quando o trabalho de impressão não é impresso dentro do tempo definido), o monitor de porta deve dar suporte a SNMP e as portas de rede no pool devem ser configuradas como "status SNMP habilitado".</span><span class="sxs-lookup"><span data-stu-id="f46e4-209">To ensure that the spooler redirects jobs to the next available printer in the pool (when the print job is not printed within the set time), the port monitor must support SNMP and the network ports in the pool must be configured as "SNMP status enabled."</span></span> <span data-ttu-id="f46e4-210">O monitor de porta que dá suporte a SNMP é o monitor de porta TCP/IP padrão.</span><span class="sxs-lookup"><span data-stu-id="f46e4-210">The port monitor that supports SNMP is Standard TCP/IP port monitor.</span></span>

<span data-ttu-id="f46e4-211">No Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão.</span><span class="sxs-lookup"><span data-stu-id="f46e4-211">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="f46e4-212">O processamento do lado do cliente de trabalhos de impressão pode ser configurado definindo *pKeyName* como "PrinterDriverData" e *valores* de configuração na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f46e4-212">Client-side rendering of print jobs can be configured by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="f46e4-213">Configuração</span><span class="sxs-lookup"><span data-stu-id="f46e4-213">Setting</span></span>                      | <span data-ttu-id="f46e4-214">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f46e4-214">Data type</span></span>      | <span data-ttu-id="f46e4-215">Descrição</span><span class="sxs-lookup"><span data-stu-id="f46e4-215">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46e4-216">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="f46e4-216">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="f46e4-217">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="f46e4-217">**REG_DWORD**</span></span> | <span data-ttu-id="f46e4-218">Um valor de 0, ou se esse valor não estiver presente no registro, habilitará a renderização padrão do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="f46e4-218">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="f46e4-219">Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="f46e4-219">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="f46e4-220">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="f46e4-220">**ForceClientSideRendering**</span></span> | <span data-ttu-id="f46e4-221">**REG_DWORD**</span><span class="sxs-lookup"><span data-stu-id="f46e4-221">**REG_DWORD**</span></span> | <span data-ttu-id="f46e4-222">Um valor de 0 ou, se esse valor não estiver presente no registro, fará com que os trabalhos de impressão sejam renderizados no cliente.</span><span class="sxs-lookup"><span data-stu-id="f46e4-222">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="f46e4-223">Se um trabalho de impressão não puder ser processado no cliente, ele será renderizado no servidor.</span><span class="sxs-lookup"><span data-stu-id="f46e4-223">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="f46e4-224">Se não for possível renderizar um trabalho de impressão no servidor, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="f46e4-224">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="f46e4-225">Um valor de 1 processará trabalhos de impressão no cliente.</span><span class="sxs-lookup"><span data-stu-id="f46e4-225">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="f46e4-226">Se não for possível renderizar um trabalho de impressão no cliente, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="f46e4-226">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f46e4-227">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f46e4-227">Requirements</span></span>



| <span data-ttu-id="f46e4-228">Requisito</span><span class="sxs-lookup"><span data-stu-id="f46e4-228">Requirement</span></span> | <span data-ttu-id="f46e4-229">Valor</span><span class="sxs-lookup"><span data-stu-id="f46e4-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f46e4-230">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f46e4-230">Minimum supported client</span></span><br/> | <span data-ttu-id="f46e4-231">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-231">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f46e4-232">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f46e4-232">Minimum supported server</span></span><br/> | <span data-ttu-id="f46e4-233">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f46e4-233">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f46e4-234">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f46e4-234">Header</span></span><br/>                   | <dl> <span data-ttu-id="f46e4-235"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f46e4-235"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f46e4-236">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f46e4-236">Library</span></span><br/>                  | <dl> <span data-ttu-id="f46e4-237"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f46e4-237"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f46e4-238">DLL</span><span class="sxs-lookup"><span data-stu-id="f46e4-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f46e4-239"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f46e4-239"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f46e4-240">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f46e4-240">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f46e4-241">**SetPrinterDataExW** (Unicode) e **SetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f46e4-241">**SetPrinterDataExW** (Unicode) and **SetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="f46e4-242">Confira também</span><span class="sxs-lookup"><span data-stu-id="f46e4-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46e4-243">Impressão</span><span class="sxs-lookup"><span data-stu-id="f46e4-243">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f46e4-244">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f46e4-244">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f46e4-245">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="f46e4-245">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="f46e4-246">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f46e4-246">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="f46e4-247">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="f46e4-247">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f46e4-248">**PRINTER_INFO_7**</span><span class="sxs-lookup"><span data-stu-id="f46e4-248">**PRINTER_INFO_7**</span></span>](printer-info-7.md)
</dt> </dl>

 

