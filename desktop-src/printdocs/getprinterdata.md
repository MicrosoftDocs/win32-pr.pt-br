---
description: A função GetPrinterData recupera dados de configuração para a impressora ou o servidor de impressão especificado.
ms.assetid: b5a44b27-a4aa-4e58-9a64-05be87d12ab5
title: Função GetPrinterData (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterData
- GetPrinterDataA
- GetPrinterDataW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: cb18936d6d3c1d82f4a52a874883cdcdfaae4815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764489"
---
# <a name="getprinterdata-function"></a><span data-ttu-id="6eaec-103">Função GetPrinterData</span><span class="sxs-lookup"><span data-stu-id="6eaec-103">GetPrinterData function</span></span>

<span data-ttu-id="6eaec-104">A função **GetPrinterData** recupera dados de configuração para a impressora ou o servidor de impressão especificado.</span><span class="sxs-lookup"><span data-stu-id="6eaec-104">The **GetPrinterData** function retrieves configuration data for the specified printer or print server.</span></span>

<span data-ttu-id="6eaec-105">No Windows 2000 e versões posteriores do Windows, chamar **GetPrinterData** é equivalente a chamar [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) com o parâmetro *pKeyName* definido como "PrinterDriverData".</span><span class="sxs-lookup"><span data-stu-id="6eaec-105">In Windows 2000 and later versions of Windows, calling **GetPrinterData** is equivalent to calling [**GetPrinterDataEx**](/windows/desktop/printdocs/getprinterdataex) with the *pKeyName* parameter set to "PrinterDriverData".</span></span>

## <a name="syntax"></a><span data-ttu-id="6eaec-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6eaec-106">Syntax</span></span>


```C++
DWORD GetPrinterData(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pValueName,
  _Out_ LPDWORD pType,
  _Out_ LPBYTE  pData,
  _In_  DWORD   nSize,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="6eaec-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6eaec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eaec-108">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-108">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaec-109">Um identificador para a impressora ou o servidor de impressão para o qual a função recupera dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="6eaec-109">A handle to the printer or print server for which the function retrieves configuration data.</span></span> <span data-ttu-id="6eaec-110">Use a função [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md)ou [**AddPrinter**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="6eaec-110">Use the [**OpenPrinter**](openprinter.md), [**OpenPrinter2**](openprinter2.md), or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6eaec-111">*valores principais* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-111">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaec-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que identifica os dados a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="6eaec-112">A pointer to a null-terminated string that identifies the data to retrieve.</span></span>

<span data-ttu-id="6eaec-113">Para impressoras, essa cadeia de caracteres é o nome de um valor de registro na chave "PrinterDriverData" da impressora no registro.</span><span class="sxs-lookup"><span data-stu-id="6eaec-113">For printers, this string is the name of a registry value under the printer's "PrinterDriverData" key in the registry.</span></span>

<span data-ttu-id="6eaec-114">Para servidores de impressão, essa cadeia é uma das cadeias de caracteres predefinidas listadas na seção comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="6eaec-114">For print servers, this string is one of the predefined strings listed in the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="6eaec-115">*pType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-115">*pType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaec-116">Um ponteiro para uma variável que recebe um valor que indica o tipo de dados recuperados em *pData*.</span><span class="sxs-lookup"><span data-stu-id="6eaec-116">A pointer to a variable that receives a value that indicates the type of data retrieved in *pData*.</span></span> <span data-ttu-id="6eaec-117">A função retorna o tipo especificado na chamada [**SetPrinterData**](setprinterdata.md) ou [**SetPrinterDataEx**](setprinterdataex.md) que armazenou os dados.</span><span class="sxs-lookup"><span data-stu-id="6eaec-117">The function returns the type specified in the [**SetPrinterData**](setprinterdata.md) or [**SetPrinterDataEx**](setprinterdataex.md) call that stored the data.</span></span> <span data-ttu-id="6eaec-118">Defina esse parâmetro como **NULL** se você não precisar do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6eaec-118">Set this parameter to **NULL** if you don't need the data type.</span></span>

</dd> <dt>

<span data-ttu-id="6eaec-119">*pData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-119">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaec-120">Um ponteiro para um buffer que recebe os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="6eaec-120">A pointer to a buffer that receives the configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="6eaec-121">*nSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-121">*nSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaec-122">O tamanho, em bytes, do buffer para o qual *pData* aponta.</span><span class="sxs-lookup"><span data-stu-id="6eaec-122">The size, in bytes, of the buffer that *pData* points to.</span></span>

</dd> <dt>

<span data-ttu-id="6eaec-123">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eaec-124">Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="6eaec-124">A pointer to a variable that receives the size, in bytes, of the configuration data.</span></span> <span data-ttu-id="6eaec-125">Se o tamanho do buffer especificado por *nSize* for muito pequeno, a função retornará um **erro com \_ mais \_ dados** e *pcbNeeded* indicará o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="6eaec-125">If the buffer size specified by *nSize* is too small, the function returns **ERROR\_MORE\_DATA**, and *pcbNeeded* indicates the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eaec-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6eaec-126">Return value</span></span>

<span data-ttu-id="6eaec-127">Se a função for bem-sucedida, o valor de retorno **será \_ êxito no erro**.</span><span class="sxs-lookup"><span data-stu-id="6eaec-127">If the function succeeds, the return value is **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="6eaec-128">Se a função falhar, o valor de retorno será um valor de erro.</span><span class="sxs-lookup"><span data-stu-id="6eaec-128">If the function fails, the return value is an error value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eaec-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eaec-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6eaec-130">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6eaec-130">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6eaec-131">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6eaec-131">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6eaec-132">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="6eaec-132">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="6eaec-133">**GetPrinterData** recupera os dados de configuração da impressora que foram definidos pela função [**SetPrinterDataEx**](setprinterdataex.md) ou [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6eaec-133">**GetPrinterData** retrieves printer configuration data that was set by the [**SetPrinterDataEx**](setprinterdataex.md) or [**SetPrinterData**](setprinterdata.md) function.</span></span>

<span data-ttu-id="6eaec-134">**GetPrinterData** pode disparar uma chamada do Windows para [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), que pode gravar no registro.</span><span class="sxs-lookup"><span data-stu-id="6eaec-134">**GetPrinterData** might trigger a Windows call to [**GetPrinterDataFromPort**](/previous-versions//ff550506(v=vs.85)), which might write to the registry.</span></span> <span data-ttu-id="6eaec-135">Se tiver, podem ocorrer efeitos colaterais, como disparar uma atualização ou atualizar a ID de evento 20 no cliente, se a impressora for compartilhada em uma rede.</span><span class="sxs-lookup"><span data-stu-id="6eaec-135">If it does, side effects can occur, such as triggering an update or upgrade printer event ID 20 in the client, if the printer is shared in a network.</span></span>

<span data-ttu-id="6eaec-136">Se *hPrinter* for um identificador para um *servidor de impressão, o* especifiquename poderá especificar um dos valores predefinidos a seguir.</span><span class="sxs-lookup"><span data-stu-id="6eaec-136">If *hPrinter* is a handle to a print server, *pValueName* can specify one of the following predefined values.</span></span>



| <span data-ttu-id="6eaec-137">Valor</span><span class="sxs-lookup"><span data-stu-id="6eaec-137">Value</span></span>                                                               | <span data-ttu-id="6eaec-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eaec-138">Comments</span></span>                                                                                                                                                                                                                        |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaec-139">**SPLREG \_ permitir que o \_ usuário \_ MANAGEFORMS**</span><span class="sxs-lookup"><span data-stu-id="6eaec-139">**SPLREG\_ALLOW\_USER\_MANAGEFORMS**</span></span>                                | <span data-ttu-id="6eaec-140">Windows XP com Service Pack 2 (SP2) e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-140">Windows XP with Service Pack 2 (SP2) and later</span></span><br/> <span data-ttu-id="6eaec-141">Windows Server 2003 com Service Pack 1 (SP1) e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-141">Windows Server 2003 with Service Pack 1 (SP1) and later</span></span><br/>                                                                                                    |
| <span data-ttu-id="6eaec-142">**arquitetura do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-142">**SPLREG\_ARCHITECTURE**</span></span>                                            |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-143">**aviso de SPLREG \_ \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="6eaec-143">**SPLREG\_BEEP\_ENABLED**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-144">**SPLREG \_ o \_ diretório de spool padrão \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-144">**SPLREG\_DEFAULT\_SPOOL\_DIRECTORY**</span></span>                               |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-145">**SPLREG \_ \_ nome do computador DNS \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-145">**SPLREG\_DNS\_MACHINE\_NAME**</span></span>                                      |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-146">**SPLREG \_ DS \_ presente**</span><span class="sxs-lookup"><span data-stu-id="6eaec-146">**SPLREG\_DS\_PRESENT**</span></span>                                             | <span data-ttu-id="6eaec-147">Após o retorno bem-sucedido, *pData* conterá 0x0001 se o computador estiver em um domínio DS; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="6eaec-147">On successful return, *pData* contains 0x0001 if the machine is on a DS domain, 0 otherwise.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="6eaec-148">**SPLREG \_ DS \_ presente \_ para o \_ usuário**</span><span class="sxs-lookup"><span data-stu-id="6eaec-148">**SPLREG\_DS\_PRESENT\_FOR\_USER**</span></span>                                  | <span data-ttu-id="6eaec-149">Após o retorno bem-sucedido, o *pData* conterá 0x0001 se o usuário estiver conectado a um domínio DS; caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="6eaec-149">On successful return, *pData* contains 0x0001 if the user is logged onto a DS domain, 0 otherwise.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="6eaec-150">**\_log de eventos do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-150">**SPLREG\_EVENT\_LOG**</span></span>                                              |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-151">**\_versão principal do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-151">**SPLREG\_MAJOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-152">**SPLREG \_ \_ versão secundária**</span><span class="sxs-lookup"><span data-stu-id="6eaec-152">**SPLREG\_MINOR\_VERSION**</span></span>                                          |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-153">**\_ \_ pop-up do SPLREG net**</span><span class="sxs-lookup"><span data-stu-id="6eaec-153">**SPLREG\_NET\_POPUP**</span></span>                                              | <span data-ttu-id="6eaec-154">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-154">Not supported in Windows Server 2003 and later</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="6eaec-155">**\_ \_ pop-up do SPLREG net para o \_ \_ computador**</span><span class="sxs-lookup"><span data-stu-id="6eaec-155">**SPLREG\_NET\_POPUP\_TO\_COMPUTER**</span></span>                                | <span data-ttu-id="6eaec-156">Após o retorno bem-sucedido, o *pData* conterá 1 se as notificações de trabalho devem ser enviadas para o computador cliente ou 0 se as notificações de trabalho forem enviadas ao usuário.</span><span class="sxs-lookup"><span data-stu-id="6eaec-156">On successful return, *pData* contains 1 if job notifications should be sent to the client computer, or 0 if job notifications are to be sent to the user.</span></span><br/> <span data-ttu-id="6eaec-157">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-157">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="6eaec-158">**\_versão do so SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-158">**SPLREG\_OS\_VERSION**</span></span>                                             | <span data-ttu-id="6eaec-159">Windows XP e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-159">Windows XP and later</span></span><br/>                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-160">**SPLREG \_ os \_ VERSIONEX**</span><span class="sxs-lookup"><span data-stu-id="6eaec-160">**SPLREG\_OS\_VERSIONEX**</span></span>                                           |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-161">**\_padrão de \_ prioridade de thread de porta SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-161">**SPLREG\_PORT\_THREAD\_PRIORITY\_DEFAULT**</span></span>                         |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-162">**\_prioridade de \_ thread de porta SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-162">**SPLREG\_PORT\_THREAD\_PRIORITY**</span></span>                                  |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-163">**\_grupos de \_ isolamento do driver de impressão SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-163">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_GROUPS**</span></span>                        | <span data-ttu-id="6eaec-164">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-164">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6eaec-165">**\_tempo de isolamento do driver de impressão SPLREG \_ antes da \_ \_ \_ \_ reciclagem**</span><span class="sxs-lookup"><span data-stu-id="6eaec-165">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_TIME\_BEFORE\_RECYCLE**</span></span>         | <span data-ttu-id="6eaec-166">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-166">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6eaec-167">**\_isolamento do driver de impressão SPLREG máximo de \_ \_ \_ \_ objetos antes da \_ \_ reciclagem**</span><span class="sxs-lookup"><span data-stu-id="6eaec-167">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_MAX\_OBJECTS\_BEFORE\_RECYCLE**</span></span> | <span data-ttu-id="6eaec-168">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-168">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6eaec-169">**\_ \_ \_ \_ tempo limite de ociosidade do isolamento do driver de impressão SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-169">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_IDLE\_TIMEOUT**</span></span>                 | <span data-ttu-id="6eaec-170">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-170">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6eaec-171">**\_política de \_ execução de isolamento do driver de impressão SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-171">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_EXECUTION\_POLICY**</span></span>             | <span data-ttu-id="6eaec-172">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-172">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6eaec-173">**\_política de \_ substituição de isolamento do driver de impressão SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-173">**SPLREG\_PRINT\_DRIVER\_ISOLATION\_OVERRIDE\_POLICY**</span></span>              | <span data-ttu-id="6eaec-174">Windows 7 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-174">Windows 7 and later</span></span><br/>                                                                                                                                                                                                  |
| <span data-ttu-id="6eaec-175">**\_fax remoto do SPLREG \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-175">**SPLREG\_REMOTE\_FAX**</span></span>                                             | <span data-ttu-id="6eaec-176">Após o retorno bem-sucedido, o *pData* conterá 0x0001 se o serviço de fax der suporte a clientes remotos. caso contrário, 0.</span><span class="sxs-lookup"><span data-stu-id="6eaec-176">On successful return, *pData* contains 0x0001 if the FAX service supports remote clients, 0 otherwise.</span></span><br/>                                                                                                               |
| <span data-ttu-id="6eaec-177">**\_ \_ pop-up de repetição do SPLREG**</span><span class="sxs-lookup"><span data-stu-id="6eaec-177">**SPLREG\_RETRY\_POPUP**</span></span>                                            | <span data-ttu-id="6eaec-178">Após o retorno bem-sucedido, o *pData* conterá 1 se o servidor estiver definido para repetir janelas pop-up para todos os trabalhos ou 0 se o servidor não tentar novamente janelas pop-up para todos os trabalhos.</span><span class="sxs-lookup"><span data-stu-id="6eaec-178">On successful return, *pData* contains 1 if server is set to retry pop-up windows for all jobs, or 0 if server does not retry pop-up windows for all jobs.</span></span><br/> <span data-ttu-id="6eaec-179">Sem suporte no Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-179">Not supported in Windows Server 2003 and later</span></span><br/> |
| <span data-ttu-id="6eaec-180">**\_prioridade de thread do Agendador SPLREG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-180">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY**</span></span>                             |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-181">**\_padrão de prioridade de thread do Agendador SPLREG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-181">**SPLREG\_SCHEDULER\_THREAD\_PRIORITY\_DEFAULT**</span></span>                    |                                                                                                                                                                                                                                 |
| <span data-ttu-id="6eaec-182">**SPLREG \_ WEBSHAREMGMT**</span><span class="sxs-lookup"><span data-stu-id="6eaec-182">**SPLREG\_WEBSHAREMGMT**</span></span>                                            | <span data-ttu-id="6eaec-183">Windows Server 2003 e posterior</span><span class="sxs-lookup"><span data-stu-id="6eaec-183">Windows Server 2003 and later</span></span><br/>                                                                                                                                                                                        |



 

<span data-ttu-id="6eaec-184">Os valores a seguir de valueName indicam o *comportamento de impressão* do pool quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="6eaec-184">The following values of *pValueName* indicate the pool printing behavior when an error occurs.</span></span>



| <span data-ttu-id="6eaec-185">Valor</span><span class="sxs-lookup"><span data-stu-id="6eaec-185">Value</span></span>                                       | <span data-ttu-id="6eaec-186">Comentários</span><span class="sxs-lookup"><span data-stu-id="6eaec-186">Comments</span></span>                                                                                                                                                                                              |
|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaec-187">**\_erro de reinicialização \_ de SPLREG \_ no \_ pool \_**</span><span class="sxs-lookup"><span data-stu-id="6eaec-187">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR**</span></span>   | <span data-ttu-id="6eaec-188">O valor de *pData* indica o tempo, em segundos, quando um trabalho é reiniciado em outra porta após a ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="6eaec-188">The value of *pData* indicates the time, in seconds, when a job is restarted on another port after an error occurs.</span></span> <span data-ttu-id="6eaec-189">Essa configuração é usada com **o \_ trabalho de reinicialização SPLREG \_ \_ no \_ pool \_ habilitado**.</span><span class="sxs-lookup"><span data-stu-id="6eaec-189">This setting is used with **SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**.</span></span><br/> |
| <span data-ttu-id="6eaec-190">**\_trabalho de reinicialização \_ de SPLREG \_ no \_ pool \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="6eaec-190">**SPLREG\_RESTART\_JOB\_ON\_POOL\_ENABLED**</span></span> | <span data-ttu-id="6eaec-191">Um valor diferente de zero em *pData* indica que o **\_ erro SPLREG reiniciar o \_ trabalho \_ no \_ pool \_** está habilitado.</span><span class="sxs-lookup"><span data-stu-id="6eaec-191">A nonzero value in *pData* indicates that **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is enabled.</span></span><br/>                                                                                            |



 

<span data-ttu-id="6eaec-192">O tempo especificado em **SPLREG \_ reiniciar o \_ trabalho \_ no \_ pool \_** é um tempo mínimo.</span><span class="sxs-lookup"><span data-stu-id="6eaec-192">The time specified in **SPLREG\_RESTART\_JOB\_ON\_POOL\_ERROR** is a minimum time.</span></span> <span data-ttu-id="6eaec-193">O tempo real pode ser maior, dependendo das seguintes configurações do monitor de porta, que são valores de registro nessa chave do registro:</span><span class="sxs-lookup"><span data-stu-id="6eaec-193">The actual time can be longer, depending on the following port monitor settings, which are registry values under this registry key:</span></span>

<span data-ttu-id="6eaec-194">**HKLM \\ sistema \\ CurrentControlSet \\ controle \\ Imprimir \\ monitores \\ <  > \\ portas monitor**</span><span class="sxs-lookup"><span data-stu-id="6eaec-194">**HKLM\\SYSTEM\\CurrentControlSet\\Control\\Print\\Monitors\\<*MonitorName*>\\Ports**</span></span>

<span data-ttu-id="6eaec-195">Chame a função [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) para consultar esses valores.</span><span class="sxs-lookup"><span data-stu-id="6eaec-195">Call the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to query these values.</span></span>



| <span data-ttu-id="6eaec-196">Configuração do monitor de porta</span><span class="sxs-lookup"><span data-stu-id="6eaec-196">Port monitor setting</span></span>     | <span data-ttu-id="6eaec-197">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6eaec-197">Data type</span></span>      | <span data-ttu-id="6eaec-198">Significado</span><span class="sxs-lookup"><span data-stu-id="6eaec-198">Meaning</span></span>                                                                                                        |
|--------------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaec-199">**StatusUpdateEnabled**</span><span class="sxs-lookup"><span data-stu-id="6eaec-199">**StatusUpdateEnabled**</span></span>  | <span data-ttu-id="6eaec-200">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6eaec-200">**REG\_DWORD**</span></span> | <span data-ttu-id="6eaec-201">Se um valor diferente de zero, permite que o monitor de porta atualize o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="6eaec-201">If a nonzero value, enables the port monitor to update the spooler with the port status.</span></span><br/>            |
| <span data-ttu-id="6eaec-202">**StatusUpdateInterval**</span><span class="sxs-lookup"><span data-stu-id="6eaec-202">**StatusUpdateInterval**</span></span> | <span data-ttu-id="6eaec-203">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6eaec-203">**REG\_DWORD**</span></span> | <span data-ttu-id="6eaec-204">Especifica o intervalo, em minutos, quando o monitor de porta atualiza o spooler com o status da porta.</span><span class="sxs-lookup"><span data-stu-id="6eaec-204">Specifies the interval, in minutes, when the port monitor updates the spooler with the port status.</span></span><br/> |



 

<span data-ttu-id="6eaec-205">No Windows 7 e versões posteriores do Windows, os trabalhos de impressão enviados a um servidor de impressão são renderizados no cliente por padrão.</span><span class="sxs-lookup"><span data-stu-id="6eaec-205">In Windows 7 and later versions of Windows, print jobs that are sent to a print server are rendered on the client by default.</span></span> <span data-ttu-id="6eaec-206">Os valores a seguir configuram o processamento do lado do cliente de trabalhos de impressão e podem ser lidos se você definir os valores a seguir em *valores* de valor.</span><span class="sxs-lookup"><span data-stu-id="6eaec-206">The following values configure client-side rendering of a print jobs and can be read if you set the following values in *pValueName*.</span></span>



| <span data-ttu-id="6eaec-207">Configuração</span><span class="sxs-lookup"><span data-stu-id="6eaec-207">Setting</span></span>                      | <span data-ttu-id="6eaec-208">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6eaec-208">Data type</span></span>      | <span data-ttu-id="6eaec-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="6eaec-209">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaec-210">**EMFDespoolingSetting**</span><span class="sxs-lookup"><span data-stu-id="6eaec-210">**EMFDespoolingSetting**</span></span>     | <span data-ttu-id="6eaec-211">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6eaec-211">**REG\_DWORD**</span></span> | <span data-ttu-id="6eaec-212">Um valor de 0, ou se esse valor não estiver presente no registro, habilitará a renderização padrão do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="6eaec-212">A value of 0, or if this value is not present in the registry, enables the default client-side rendering of print jobs.</span></span><br/> <span data-ttu-id="6eaec-213">Um valor de 1 desabilita a renderização do lado do cliente de trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="6eaec-213">A value of 1 disables client-side rendering of print jobs.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="6eaec-214">**ForceClientSideRendering**</span><span class="sxs-lookup"><span data-stu-id="6eaec-214">**ForceClientSideRendering**</span></span> | <span data-ttu-id="6eaec-215">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6eaec-215">**REG\_DWORD**</span></span> | <span data-ttu-id="6eaec-216">Um valor de 0 ou, se esse valor não estiver presente no registro, fará com que os trabalhos de impressão sejam renderizados no cliente.</span><span class="sxs-lookup"><span data-stu-id="6eaec-216">A value of 0, or if this value is not present in the registry, will cause the print jobs to be rendered on the client.</span></span> <span data-ttu-id="6eaec-217">Se um trabalho de impressão não puder ser processado no cliente, ele será renderizado no servidor.</span><span class="sxs-lookup"><span data-stu-id="6eaec-217">If a print job cannot be rendered on the client, it will be rendered on the server.</span></span> <span data-ttu-id="6eaec-218">Se não for possível renderizar um trabalho de impressão no servidor, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="6eaec-218">If a print job cannot be rendered on the server, it will fail.</span></span><br/> <span data-ttu-id="6eaec-219">Um valor de 1 processará trabalhos de impressão no cliente.</span><span class="sxs-lookup"><span data-stu-id="6eaec-219">A value of 1 will render print jobs on the client.</span></span> <span data-ttu-id="6eaec-220">Se não for possível renderizar um trabalho de impressão no cliente, ele falhará.</span><span class="sxs-lookup"><span data-stu-id="6eaec-220">If a print job cannot be rendered on the client, it will fail.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6eaec-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eaec-221">Requirements</span></span>



| <span data-ttu-id="6eaec-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eaec-222">Requirement</span></span> | <span data-ttu-id="6eaec-223">Valor</span><span class="sxs-lookup"><span data-stu-id="6eaec-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaec-224">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6eaec-224">Minimum supported client</span></span><br/> | <span data-ttu-id="6eaec-225">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6eaec-226">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6eaec-226">Minimum supported server</span></span><br/> | <span data-ttu-id="6eaec-227">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6eaec-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6eaec-228">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6eaec-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eaec-229"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6eaec-229"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6eaec-230">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6eaec-230">Library</span></span><br/>                  | <dl> <span data-ttu-id="6eaec-231"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eaec-231"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6eaec-232">DLL</span><span class="sxs-lookup"><span data-stu-id="6eaec-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eaec-233"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6eaec-233"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6eaec-234">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6eaec-234">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6eaec-235">**GetPrinterDataW** (Unicode) e **GetPrinterDataA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6eaec-235">**GetPrinterDataW** (Unicode) and **GetPrinterDataA** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="6eaec-236">Confira também</span><span class="sxs-lookup"><span data-stu-id="6eaec-236">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eaec-237">Impressão</span><span class="sxs-lookup"><span data-stu-id="6eaec-237">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6eaec-238">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="6eaec-238">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6eaec-239">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6eaec-239">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="6eaec-240">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6eaec-240">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="6eaec-241">**Setprinter**</span><span class="sxs-lookup"><span data-stu-id="6eaec-241">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="6eaec-242">**SetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="6eaec-242">**SetPrinterData**</span></span>](setprinterdata.md)
</dt> <dt>

[<span data-ttu-id="6eaec-243">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6eaec-243">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="6eaec-244">**Caps do multiprocessador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6eaec-244">**PRINTPROCESSOR\_CAPS\_1**</span></span>](printprocessor-caps-1.md)
</dt> </dl>

 

