---
description: A função GetPrinterDataEx recupera dados de configuração para a impressora ou o servidor de impressão especificado.
ms.assetid: 5d9183a7-97cc-46de-848e-e37ce51396eb
title: Função GetPrinterDataEx (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDataEx
- GetPrinterDataExA
- GetPrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: bdadf2e1259445ca5285e5b12bc906140a137cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663209"
---
# <a name="getprinterdataex-function"></a><span data-ttu-id="20fe2-103">Função GetPrinterDataEx</span><span class="sxs-lookup"><span data-stu-id="20fe2-103">GetPrinterDataEx function</span></span>

<span data-ttu-id="20fe2-104">A função **GetPrinterDataEx** recupera dados de configuração para a impressora ou o servidor de impressão especificado.</span><span class="sxs-lookup"><span data-stu-id="20fe2-104">The **GetPrinterDataEx** function retrieves configuration data for the specified printer or print server.</span></span> <span data-ttu-id="20fe2-105">**GetPrinterDataEx** pode recuperar valores armazenados pela função [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="20fe2-105">**GetPrinterDataEx** can retrieve values that the [**SetPrinterData**](setprinterdata.md) function stored.</span></span> <span data-ttu-id="20fe2-106">Além disso, o **GetPrinterDataEx** pode recuperar valores que a função [**SetPrinterDataEx**](setprinterdataex.md) armazenada sob uma chave especificada.</span><span class="sxs-lookup"><span data-stu-id="20fe2-106">In addition, **GetPrinterDataEx** can retrieve values that the [**SetPrinterDataEx**](setprinterdataex.md) function stored under a specified key.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fe2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20fe2-107">Syntax</span></span>


```C++
DWORD GetPrinterDataEx(
  _In_  HANDLE  hPrinter,
  _In_  LPCTSTR pKeyName,
  _In_  LPCTSTR pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="20fe2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20fe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20fe2-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-110">Um identificador para a impressora ou o servidor de impressão para o qual a função recupera dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="20fe2-110">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="20fe2-111">Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="20fe2-111">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="20fe2-112">*pKeyName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-112">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a chave que contém o valor a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="20fe2-113">A pointer to a null-terminated string that specifies the key containing the value to be retrieved.</span></span> <span data-ttu-id="20fe2-114">Use o caractere de barra invertida ( \\ ) como um delimitador para especificar um caminho que tenha uma ou mais subchaves.</span><span class="sxs-lookup"><span data-stu-id="20fe2-114">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="20fe2-115">Se *hPrinter* for um identificador para uma impressora e *pKeyName* for **nulo** ou uma cadeia de caracteres vazia, **GetPrinterDataEx** retornará um **\_ \_ parâmetro inválido de erro**.</span><span class="sxs-lookup"><span data-stu-id="20fe2-115">If *hPrinter* is a handle to a printer and *pKeyName* is **NULL** or an empty string, **GetPrinterDataEx** returns **ERROR\_INVALID\_PARAMETER**.</span></span>

<span data-ttu-id="20fe2-116">Se *hPrinter* for um identificador para um servidor de impressão, *pKeyName* será ignorado.</span><span class="sxs-lookup"><span data-stu-id="20fe2-116">If *hPrinter* is a handle to a print server, *pKeyName* is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="20fe2-117">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-117">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-118">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="20fe2-118">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="20fe2-119">Para impressoras, essa cadeia de caracteres especifica o nome de um valor na chave *pKeyName* .</span><span class="sxs-lookup"><span data-stu-id="20fe2-119">For printers, this string specifies the name of a value under the *pKeyName* key.</span></span>

<span data-ttu-id="20fe2-120">Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="20fe2-120">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="20fe2-121">*pType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-121">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-122">Um ponteiro para uma variável que recebe o tipo de dados armazenados no valor.</span><span class="sxs-lookup"><span data-stu-id="20fe2-122">A pointer to a variable that receives the type of data stored in the value.</span></span> <span data-ttu-id="20fe2-123">A função retorna o tipo especificado na chamada [**SetPrinterDataEx**](setprinterdataex.md) quando os dados foram armazenados.</span><span class="sxs-lookup"><span data-stu-id="20fe2-123">The function returns the type specified in the [**SetPrinterDataEx**](setprinterdataex.md) call when the data was stored.</span></span> <span data-ttu-id="20fe2-124">Esse parâmetro poderá ser **nulo** se você não precisar das informações.</span><span class="sxs-lookup"><span data-stu-id="20fe2-124">This parameter can be **NULL** if you don't need the information.</span></span> <span data-ttu-id="20fe2-125">**GetPrinterDataEx** passa *pType* como o parâmetro *lpdwType* de uma chamada de função [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) .</span><span class="sxs-lookup"><span data-stu-id="20fe2-125">**GetPrinterDataEx** passes *pType* on as the *lpdwType* parameter of a [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) function call.</span></span>

</dd> <dt>

<span data-ttu-id="20fe2-126">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-126">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-127">Um ponteiro para um buffer que recebe os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="20fe2-127">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="20fe2-128">*nSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-128">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-129">O tamanho, em bytes, do buffer apontado por *pData*.</span><span class="sxs-lookup"><span data-stu-id="20fe2-129">The size, in bytes, of the buffer pointed to by *pData*.</span></span>

</dd> <dt>

<span data-ttu-id="20fe2-130">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-130">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20fe2-131">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="20fe2-131">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="20fe2-132">Se o tamanho do buffer especificado por *nSize* for muito pequeno, a função retornará um **erro com \_ mais \_ dados** e *pcbNeeded* indicará o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="20fe2-132">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20fe2-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20fe2-133">Return value</span></span>

<span data-ttu-id="20fe2-134">Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.</span><span class="sxs-lookup"><span data-stu-id="20fe2-134">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span>

<span data-ttu-id="20fe2-135">Se a função falhar, o valor de retorno será um valor de erro.</span><span class="sxs-lookup"><span data-stu-id="20fe2-135">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20fe2-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="20fe2-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20fe2-137">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="20fe2-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="20fe2-138">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="20fe2-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="20fe2-139">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="20fe2-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="20fe2-140">**GetPrinterDataEx** recupera os dados de configuração de impressora que foram definidos pelas funções [**SetPrinterDataEx**](setprinterdataex.md) e [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="20fe2-140">**GetPrinterDataEx** retrieves printer-configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) and [**SetPrinterData**](setprinterdata.md) functions.</span></span>

<span data-ttu-id="20fe2-141">Chamar **GetPrinterDataEx** com o parâmetro *pKeyName* definido como "PrinterDriverData" é equivalente a chamar a função [**GetPrinterData**](getprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="20fe2-141">Calling **GetPrinterDataEx** with the *pKeyName* parameter set to "PrinterDriverData" is equivalent to calling the [**GetPrinterData**](getprinterdata.md) function.</span></span>

<span data-ttu-id="20fe2-142">Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="20fe2-142">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="20fe2-143">Valor</span><span class="sxs-lookup"><span data-stu-id="20fe2-143">Value</span></span>                                                               | <span data-ttu-id="20fe2-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="20fe2-144">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fe2-145">**SPLREG \_ permitir que o \_ usuário \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="20fe2-145">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="20fe2-146">Windows XP com Service Pack 2 (SP2) e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-146">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="20fe2-147">Windows Server 2003 com Service Pack 1 (SP1) e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-147">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="20fe2-148">**arquitetura do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-148">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-149">**aviso de SPLREG \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="20fe2-149">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-150">**SPLREG \_ o \_ diretório de spool padrão \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-150">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-151">**SPLREG \_ \_ nome do computador DNS \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-151">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-152">**SPLREG \_ DS \_ presente**</span><span class="sxs-lookup"><span data-stu-id="20fe2-152">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="20fe2-153">Após o retorno bem-sucedido, *pData* conterá 0x0001 se o computador estiver em um domínio DS; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="20fe2-153">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="20fe2-154">**SPLREG \_ DS \_ presente \_ para o \_ usuário**</span><span class="sxs-lookup"><span data-stu-id="20fe2-154">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="20fe2-155">Após o retorno bem-sucedido, o *pData* conterá 0x0001 se o usuário estiver conectado a um domínio DS; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="20fe2-155">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="20fe2-156">**\_log de eventos do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-156">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-157">**\_versão principal do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-157">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-158">**SPLREG \_ \_ versão secundária**</span><span class="sxs-lookup"><span data-stu-id="20fe2-158">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-159">**\_ \_ pop-up do SPLREG net**</span><span class="sxs-lookup"><span data-stu-id="20fe2-159">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="20fe2-160">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-160">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="20fe2-161">**\_ \_ pop-up do SPLREG net para o \_ \_ computador**</span><span class="sxs-lookup"><span data-stu-id="20fe2-161">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="20fe2-162">Após o retorno bem-sucedido, o *pData* conterá 1 se as notificações de trabalho devem ser enviadas para o computador cliente ou 0 se as notificações de trabalho forem enviadas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="20fe2-162">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="20fe2-163">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-163">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="20fe2-164">**\_versão do so SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-164">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="20fe2-165">Windows XP e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-165">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-166">**SPLREG \_ os \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="20fe2-166">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-167">**\_padrão de \_ prioridade de thread de porta SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-167">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-168">**\_prioridade de \_ thread de porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-168">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-169">**\_grupos de \_ isolamento do driver de impressão SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="20fe2-170">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="20fe2-171">**\_tempo de isolamento do driver de impressão SPLREG \_ antes da \_ \_ \_ \_ reciclagem**</span><span class="sxs-lookup"><span data-stu-id="20fe2-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="20fe2-172">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="20fe2-173">**\_isolamento do driver de impressão SPLREG máximo de \_ \_ \_ \_ objetos antes da \_ \_ reciclagem**</span><span class="sxs-lookup"><span data-stu-id="20fe2-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="20fe2-174">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="20fe2-175">**\_ \_ \_ \_ tempo limite de ociosidade do isolamento do driver de impressão SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-175">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="20fe2-176">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-176">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="20fe2-177">**\_política de \_ execução de isolamento do driver de impressão SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-177">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="20fe2-178">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-178">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="20fe2-179">**\_política de \_ substituição de isolamento do driver de impressão SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-179">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="20fe2-180">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-180">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="20fe2-181">**\_fax remoto do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-181">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="20fe2-182">Após o retorno bem-sucedido, o *pData* conterá 0x0001 se o serviço de fax der suporte a clientes remotos. caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="20fe2-182">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="20fe2-183">**\_ \_ pop-up de repetição do SPLREG**</span><span class="sxs-lookup"><span data-stu-id="20fe2-183">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="20fe2-184">Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="20fe2-184">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="20fe2-185">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-185">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="20fe2-186">**\_prioridade de thread do Agendador SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-186">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-187">**\_padrão de prioridade de thread do Agendador SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-187">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="20fe2-188">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="20fe2-188">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="20fe2-189">Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="20fe2-189">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="20fe2-190">Os valores a seguir de valueName indicam o *comportamento de impressão* do pool quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="20fe2-190">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="20fe2-191">Valor</span><span class="sxs-lookup"><span data-stu-id="20fe2-191">Value</span></span>                                       | <span data-ttu-id="20fe2-192">Comentários</span><span class="sxs-lookup"><span data-stu-id="20fe2-192">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fe2-193">**\_erro de reinicialização \_ de SPLREG \_ no \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="20fe2-193">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="20fe2-194">O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="20fe2-194">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="20fe2-195">Essa configuração é usada com **o \_ trabalho de reinicialização SPLREG \_ \_ no \_ pool \_ habilitado**.</span><span class="sxs-lookup"><span data-stu-id="20fe2-195">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="20fe2-196">**\_trabalho de reinicialização \_ de SPLREG \_ no \_ pool \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="20fe2-196">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="20fe2-197">Um valor diferente de zero em *pData* indica que o **\_ erro SPLREG reiniciar o \_ trabalho \_ no \_ pool \_** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="20fe2-197">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="20fe2-198">O tempo especificado em **SPLREG \_ reiniciar o \_ trabalho \_ no \_ pool \_** é um tempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="20fe2-198">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="20fe2-199">O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:</span><span class="sxs-lookup"><span data-stu-id="20fe2-199">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="20fe2-200">**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**</span><span class="sxs-lookup"><span data-stu-id="20fe2-200">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="20fe2-201">Chame a função [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar esses valores.</span><span class="sxs-lookup"><span data-stu-id="20fe2-201">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="20fe2-202">Configuração do monitor de porta</span><span class="sxs-lookup"><span data-stu-id="20fe2-202">Port monitor setting</span></span>     | <span data-ttu-id="20fe2-203">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="20fe2-203">Data type</span></span>      | <span data-ttu-id="20fe2-204">Significado</span><span class="sxs-lookup"><span data-stu-id="20fe2-204">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fe2-205">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="20fe2-205">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="20fe2-206">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="20fe2-206">**REG\_DWORD**</span></span> | <span data-ttu-id="20fe2-207">Se um valor diferente de zero, permite que o monitor de porta atualize o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="20fe2-207">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="20fe2-208">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="20fe2-208">**StatusUpdateInterval**</span></span> | <span data-ttu-id="20fe2-209">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="20fe2-209">**REG\_DWORD**</span></span> | <span data-ttu-id="20fe2-210">Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="20fe2-210">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="20fe2-211">Se *pKeyName* for uma das chaves de DS (serviço de diretório predefinidas) (Confira [**setprinter**](setprinter.md) *) e o* nome da chave contiver uma vírgula (', '), a parte de namename antes da vírgula será a do valor Value e a *parte de* NAMEname *à direita* da vírgula será a OID da propriedade DS.</span><span class="sxs-lookup"><span data-stu-id="20fe2-211">If *pKeyName* is one of the predefined Directory Service (DS) keys (see [**SetPrinter**](setprinter.md)) and *pValueName* contains a comma (','), then the portion of *pValueName* before the comma is the value name and the portion of *pValueName* to the right of the comma is the DS Property OID.</span></span> <span data-ttu-id="20fe2-212">Uma subchave chamada OID é criada e um novo valor que consiste no nome do valor e no OID é inserido sob a chave de OID.</span><span class="sxs-lookup"><span data-stu-id="20fe2-212">A subkey called OID is created and a new value that consists of the value name and OID is entered under the OID key.</span></span> <span data-ttu-id="20fe2-213">[**SetPrinterDataEx**](setprinterdataex.md) também adiciona o nome de valor e os dados sob a chave DS.</span><span class="sxs-lookup"><span data-stu-id="20fe2-213">[**SetPrinterDataEx**](setprinterdataex.md) also adds the value name and data under the DS key.</span></span>

<span data-ttu-id="20fe2-214">No Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão.</span><span class="sxs-lookup"><span data-stu-id="20fe2-214">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="20fe2-215">A configuração do processamento do lado do cliente para uma impressora pode ser lida com a definição de *pKeyName* como "PrinterDriverData" e o *valores* de configuração na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="20fe2-215">The configuration of client-side rendering for a printer can be read by setting *pKeyName* to "PrinterDriverData" and *pValueName* to the setting value in the following table.</span></span>



| <span data-ttu-id="20fe2-216">Configuração</span><span class="sxs-lookup"><span data-stu-id="20fe2-216">Setting</span></span>                      | <span data-ttu-id="20fe2-217">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="20fe2-217">Data type</span></span>      | <span data-ttu-id="20fe2-218">Descrição</span><span class="sxs-lookup"><span data-stu-id="20fe2-218">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fe2-219">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="20fe2-219">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="20fe2-220">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="20fe2-220">**REG\_DWORD**</span></span> | <span data-ttu-id="20fe2-221">Um valor de 0, ou se esse valor não estiver presente no registro, habilitará a renderização padrão do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="20fe2-221">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="20fe2-222">Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="20fe2-222">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="20fe2-223">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="20fe2-223">**ForceClientSideRendering**</span></span> | <span data-ttu-id="20fe2-224">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="20fe2-224">**REG\_DWORD**</span></span> | <span data-ttu-id="20fe2-225">Um valor de 0 ou, se esse valor não estiver presente no registro, fará com que os trabalhos de impressão sejam renderizados no cliente.</span><span class="sxs-lookup"><span data-stu-id="20fe2-225">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="20fe2-226">Se um trabalho de impressão não puder ser processado no cliente, ele será renderizado no servidor.</span><span class="sxs-lookup"><span data-stu-id="20fe2-226">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="20fe2-227">Se não for possível renderizar um trabalho de impressão no servidor, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="20fe2-227">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="20fe2-228">Um valor de 1 processará trabalhos de impressão no cliente.</span><span class="sxs-lookup"><span data-stu-id="20fe2-228">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="20fe2-229">Se não for possível renderizar um trabalho de impressão no cliente, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="20fe2-229">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="20fe2-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20fe2-230">Requirements</span></span>



| <span data-ttu-id="20fe2-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fe2-231">Requirement</span></span> | <span data-ttu-id="20fe2-232">Valor</span><span class="sxs-lookup"><span data-stu-id="20fe2-232">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fe2-233">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20fe2-233">Minimum supported client</span></span><br/> | <span data-ttu-id="20fe2-234">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-234">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="20fe2-235">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20fe2-235">Minimum supported server</span></span><br/> | <span data-ttu-id="20fe2-236">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="20fe2-236">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="20fe2-237">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="20fe2-237">Header</span></span><br/>                   | <dl> <span data-ttu-id="20fe2-238"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20fe2-238"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="20fe2-239">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20fe2-239">Library</span></span><br/>                  | <dl> <span data-ttu-id="20fe2-240"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20fe2-240"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="20fe2-241">DLL</span><span class="sxs-lookup"><span data-stu-id="20fe2-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20fe2-242"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="20fe2-242"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="20fe2-243">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="20fe2-243">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="20fe2-244">**GetPrinterDataExW** (Unicode) e **GetPrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="20fe2-244">**GetPrinterDataExW** (Unicode) and **GetPrinterDataExA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="20fe2-245">Confira também</span><span class="sxs-lookup"><span data-stu-id="20fe2-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fe2-246">Impressão</span><span class="sxs-lookup"><span data-stu-id="20fe2-246">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="20fe2-247">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="20fe2-247">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="20fe2-248">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="20fe2-248">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="20fe2-249">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="20fe2-249">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

