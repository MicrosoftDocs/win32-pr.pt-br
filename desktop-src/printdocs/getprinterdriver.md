---
description: A função GetPrinterDriver recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, o GetPrinterDriver o instalará.
ms.assetid: 93f859b4-1005-4359-8029-9536d6eeb7e7
title: Função GetPrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver
- GetPrinterDriverA
- GetPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a67a77a8167bf207231d2f3f6f063ed7636e201f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773070"
---
# <a name="getprinterdriver-function"></a><span data-ttu-id="4e56a-104">Função GetPrinterDriver</span><span class="sxs-lookup"><span data-stu-id="4e56a-104">GetPrinterDriver function</span></span>

<span data-ttu-id="4e56a-105">A função **GetPrinterDriver** recupera dados de driver para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="4e56a-105">The **GetPrinterDriver** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="4e56a-106">Se o driver não estiver instalado no computador local, o **GetPrinterDriver** o instalará.</span><span class="sxs-lookup"><span data-stu-id="4e56a-106">If the driver is not installed on the local computer, **GetPrinterDriver** installs it.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e56a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e56a-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="4e56a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e56a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e56a-109">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-110">Um identificador para a impressora para a qual os dados do driver devem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="4e56a-110">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="4e56a-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="4e56a-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="4e56a-112">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-112">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-113">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="4e56a-113">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="4e56a-114">Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.</span><span class="sxs-lookup"><span data-stu-id="4e56a-114">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="4e56a-115">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-115">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-116">A estrutura de driver de impressora retornada no buffer *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="4e56a-116">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="4e56a-117">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4e56a-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4e56a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="4e56a-118">Value</span></span>                                                                                                | <span data-ttu-id="4e56a-119">Significado</span><span class="sxs-lookup"><span data-stu-id="4e56a-119">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="4e56a-120"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-120"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-121">**Informações do DRIVER \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4e56a-121">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="4e56a-122"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-122"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-123">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4e56a-123">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="4e56a-124"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-124"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-125">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4e56a-125">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="4e56a-126"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-126"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-127">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4e56a-127">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="4e56a-128"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-128"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-129">**Informações do DRIVER \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="4e56a-129">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="4e56a-130"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-130"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-131">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="4e56a-131">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="4e56a-132"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-132"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="4e56a-133">**Informações do DRIVER \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="4e56a-133">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="4e56a-134">*pDriverInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-134">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-135">Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre o driver, conforme especificado pelo nível.</span><span class="sxs-lookup"><span data-stu-id="4e56a-135">A pointer to a buffer that receives a structure containing information about the driver, as specified by Level.</span></span> <span data-ttu-id="4e56a-136">O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="4e56a-136">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="4e56a-137">Para determinar o tamanho do buffer necessário, chame **GetPrinterDriver** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="4e56a-137">To determine the required buffer size, call **GetPrinterDriver** with *cbBuf* set to zero.</span></span> <span data-ttu-id="4e56a-138">**GetPrinterDriver** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="4e56a-138">**GetPrinterDriver** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="4e56a-139">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-140">O tamanho, em bytes, da matriz na qual *pDriverInfo* aponta.</span><span class="sxs-lookup"><span data-stu-id="4e56a-140">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="4e56a-141">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e56a-142">Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="4e56a-142">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e56a-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e56a-143">Return value</span></span>

<span data-ttu-id="4e56a-144">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="4e56a-144">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4e56a-145">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="4e56a-145">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="4e56a-146">Para um driver não existente, a função retorna um driver de impressora de erro \_ desconhecido \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="4e56a-146">For a non-existent driver, the function returns ERROR\_UNKNOWN\_PRINTER\_DRIVER.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e56a-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e56a-147">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e56a-148">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="4e56a-148">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4e56a-149">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4e56a-149">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4e56a-150">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="4e56a-150">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4e56a-151">As [**estruturas \_ informações \_ do driver 2**](driver-info-2.md), informações do driver [**\_ \_ 3**](driver-info-3.md), [**informações do driver \_ \_ 4**](driver-info-4.md), [**informações do driver \_ \_ 5**](driver-info-5.md)e [**informações do driver \_ \_ 6**](driver-info-6.md) contêm o nome do arquivo ou o caminho completo e o nome do arquivo do driver de impressora no membro **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="4e56a-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), and [**DRIVER\_INFO\_6**](driver-info-6.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="4e56a-152">Um aplicativo pode usar o caminho e o nome do arquivo para carregar um driver de impressora chamando a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e fornecendo o caminho e o nome do arquivo como o único argumento.</span><span class="sxs-lookup"><span data-stu-id="4e56a-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e56a-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e56a-153">Requirements</span></span>



| <span data-ttu-id="4e56a-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e56a-154">Requirement</span></span> | <span data-ttu-id="4e56a-155">Valor</span><span class="sxs-lookup"><span data-stu-id="4e56a-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e56a-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e56a-156">Minimum supported client</span></span><br/> | <span data-ttu-id="4e56a-157">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-157">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e56a-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4e56a-158">Minimum supported server</span></span><br/> | <span data-ttu-id="4e56a-159">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4e56a-159">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e56a-160">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4e56a-160">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e56a-161"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-161"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4e56a-162">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e56a-162">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e56a-163"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-163"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4e56a-164">DLL</span><span class="sxs-lookup"><span data-stu-id="4e56a-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e56a-165"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="4e56a-165"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="4e56a-166">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4e56a-166">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4e56a-167">**GetPrinterDriverW** (Unicode) e **GetPrinterDriverA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4e56a-167">**GetPrinterDriverW** (Unicode) and **GetPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="4e56a-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e56a-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e56a-169">Impressão</span><span class="sxs-lookup"><span data-stu-id="4e56a-169">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4e56a-170">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="4e56a-170">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4e56a-171">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="4e56a-171">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="4e56a-172">**Informações do DRIVER \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="4e56a-172">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="4e56a-173">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="4e56a-173">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="4e56a-174">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="4e56a-174">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="4e56a-175">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="4e56a-175">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="4e56a-176">**Informações do DRIVER \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="4e56a-176">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="4e56a-177">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="4e56a-177">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="4e56a-178">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="4e56a-178">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="4e56a-179">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="4e56a-179">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

