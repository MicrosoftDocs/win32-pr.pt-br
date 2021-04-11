---
description: A função GetPrinterDriver2 recupera dados de driver para a impressora especificada. Se o driver não estiver instalado no computador local, o GetPrinterDriver2 o instalará e exibirá qualquer interface do usuário na janela especificada.
ms.assetid: 0d482d28-7668-4734-ba71-5b355c18ddec
title: Função GetPrinterDriver2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriver2
- GetPrinterDriver2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b0a9d2bfe7827a2c0e3db9fff9e8249b73bf5102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171714"
---
# <a name="getprinterdriver2-function"></a><span data-ttu-id="b6b62-104">Função GetPrinterDriver2</span><span class="sxs-lookup"><span data-stu-id="b6b62-104">GetPrinterDriver2 function</span></span>

<span data-ttu-id="b6b62-105">A função **GetPrinterDriver2** recupera dados de driver para a impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="b6b62-105">The **GetPrinterDriver2** function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="b6b62-106">Se o driver não estiver instalado no computador local, o **GetPrinterDriver2** o instalará e exibirá qualquer interface do usuário na janela especificada.</span><span class="sxs-lookup"><span data-stu-id="b6b62-106">If the driver is not installed on the local computer, **GetPrinterDriver2** installs it and displays any user interface to the specified window.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6b62-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b6b62-107">Syntax</span></span>


```C++
BOOL GetPrinterDriver2(
  _In_opt_ HWND    hWnd,
  _In_     HANDLE  hPrinter,
  _In_opt_ LPTSTR  pEnvironment,
  _In_     DWORD   Level,
  _Out_    LPBYTE  pDriverInfo,
  _In_     DWORD   cbBuf,
  _Out_    LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="b6b62-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6b62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6b62-109">*HWND* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-109">*hWnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-110">Um identificador da janela que será usado como a janela pai de qualquer interface do usuário, como uma caixa de diálogo, que o driver exibe durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="b6b62-110">A handle of the window that will be used as the parent window of any user interface, such as a dialog box, that the driver displays during installation.</span></span> <span data-ttu-id="b6b62-111">Se o valor desse parâmetro for **nulo**, a interface do usuário do driver ainda será exibida para o usuário durante a instalação, mas não terá uma janela pai.</span><span class="sxs-lookup"><span data-stu-id="b6b62-111">If the value of this parameter is **NULL**, the driver's user interface will still be displayed to the user during installation, but it will not have a parent window.</span></span>

</dd> <dt>

<span data-ttu-id="b6b62-112">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-112">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-113">Um identificador para a impressora para a qual os dados do driver devem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="b6b62-113">A handle to the printer for which the driver data should be retrieved.</span></span> <span data-ttu-id="b6b62-114">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="b6b62-114">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b6b62-115">*pEnvironment* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-115">*pEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-116">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="b6b62-116">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="b6b62-117">Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.</span><span class="sxs-lookup"><span data-stu-id="b6b62-117">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="b6b62-118">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-118">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-119">A estrutura de driver de impressora retornada no buffer *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="b6b62-119">The printer driver structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="b6b62-120">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6b62-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b6b62-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b6b62-121">Value</span></span>                                                                                                | <span data-ttu-id="b6b62-122">Significado</span><span class="sxs-lookup"><span data-stu-id="b6b62-122">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="b6b62-123"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-123"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-124">**Informações do DRIVER \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b6b62-124">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="b6b62-125"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-125"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-126">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b6b62-126">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="b6b62-127"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-127"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-128">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="b6b62-128">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="b6b62-129"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-129"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-130">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="b6b62-130">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="b6b62-131"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-131"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-132">**Informações do DRIVER \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="b6b62-132">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="b6b62-133"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-133"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-134">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="b6b62-134">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="b6b62-135"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-135"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="b6b62-136">**Informações do DRIVER \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="b6b62-136">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="b6b62-137">*pDriverInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-137">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-138">Um ponteiro para um buffer que recebe uma estrutura que contém informações sobre o driver, conforme especificado pelo *nível*.</span><span class="sxs-lookup"><span data-stu-id="b6b62-138">A pointer to a buffer that receives a structure containing information about the driver, as specified by *Level*.</span></span> <span data-ttu-id="b6b62-139">O buffer deve ser grande o suficiente para armazenar as cadeias de caracteres apontadas pelos membros da estrutura.</span><span class="sxs-lookup"><span data-stu-id="b6b62-139">The buffer must be large enough to store the strings pointed to by the structure members.</span></span>

<span data-ttu-id="b6b62-140">Para determinar o tamanho do buffer necessário, chame **GetPrinterDriver2** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="b6b62-140">To determine the required buffer size, call **GetPrinterDriver2** with *cbBuf* set to zero.</span></span> <span data-ttu-id="b6b62-141">**GetPrinterDriver2** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **um \_ \_ buffer insuficiente de erro** e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="b6b62-141">**GetPrinterDriver2** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_INSUFFICIENT\_BUFFER**, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="b6b62-142">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-142">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-143">O tamanho, em bytes, da matriz na qual *pDriverInfo* aponta.</span><span class="sxs-lookup"><span data-stu-id="b6b62-143">The size, in bytes, of the array at which *pDriverInfo* points.</span></span>

</dd> <dt>

<span data-ttu-id="b6b62-144">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-144">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6b62-145">Um ponteiro para um valor que recebe o número de bytes copiados se a função for bem sucedido ou o número de bytes necessários se *cbBuf* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="b6b62-145">A pointer to a value that receives the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6b62-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b6b62-146">Return value</span></span>

<span data-ttu-id="b6b62-147">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="b6b62-147">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b6b62-148">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="b6b62-148">If the function fails, the return value is zero.</span></span> <span data-ttu-id="b6b62-149">Para obter o status de retorno, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="b6b62-149">To get the return status, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="b6b62-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6b62-150">Remarks</span></span>

<span data-ttu-id="b6b62-151">As [**estruturas \_ informações \_ do driver 2**](driver-info-2.md), informações do driver [**\_ \_ 3**](driver-info-3.md), [**informações do driver \_ \_ 4**](driver-info-4.md), [**informações do driver \_ \_ 5**](driver-info-5.md), [**\_ informações sobre o driver \_ 6**](driver-info-6.md)e [**\_ informações sobre o driver \_ 8**](driver-info-8.md) contêm o nome do arquivo ou o caminho completo e o nome do arquivo do driver de impressora no membro **pDriverPath** .</span><span class="sxs-lookup"><span data-stu-id="b6b62-151">The [**DRIVER\_INFO\_2**](driver-info-2.md), [**DRIVER\_INFO\_3**](driver-info-3.md), [**DRIVER\_INFO\_4**](driver-info-4.md), [**DRIVER\_INFO\_5**](driver-info-5.md), [**DRIVER\_INFO\_6**](driver-info-6.md), and [**DRIVER\_INFO\_8**](driver-info-8.md) structures contain the file name or the full path and file name of the printer driver in the **pDriverPath** member.</span></span> <span data-ttu-id="b6b62-152">Um aplicativo pode usar o caminho e o nome do arquivo para carregar um driver de impressora chamando a função [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e fornecendo o caminho e o nome do arquivo como o único argumento.</span><span class="sxs-lookup"><span data-stu-id="b6b62-152">An application can use the path and file name to load a printer driver by calling the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function and supplying the path and file name as the single argument.</span></span>

<span data-ttu-id="b6b62-153">Não há suporte para a versão ANSI dessa função, **GetPrinterDriver2A** e **\_ não \_ há suporte para** retorno de erro.</span><span class="sxs-lookup"><span data-stu-id="b6b62-153">The ANSI version of this function, **GetPrinterDriver2A** is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6b62-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6b62-154">Requirements</span></span>



| <span data-ttu-id="b6b62-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6b62-155">Requirement</span></span> | <span data-ttu-id="b6b62-156">Valor</span><span class="sxs-lookup"><span data-stu-id="b6b62-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b62-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6b62-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b6b62-158">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="b6b62-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6b62-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b6b62-160">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6b62-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b6b62-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6b62-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6b62-162"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b6b62-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b6b62-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="b6b62-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b6b62-165">DLL</span><span class="sxs-lookup"><span data-stu-id="b6b62-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6b62-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b6b62-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b6b62-167">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b6b62-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6b62-168">**GetPrinterDriver2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="b6b62-168">**GetPrinterDriver2W** (Unicode)</span></span><br/>                                                               |



## <a name="see-also"></a><span data-ttu-id="b6b62-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6b62-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6b62-170">Impressão</span><span class="sxs-lookup"><span data-stu-id="b6b62-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b6b62-171">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="b6b62-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b6b62-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="b6b62-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="b6b62-173">**Informações do DRIVER \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b6b62-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="b6b62-174">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b6b62-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="b6b62-175">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="b6b62-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="b6b62-176">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="b6b62-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="b6b62-177">**Informações do DRIVER \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="b6b62-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="b6b62-178">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="b6b62-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="b6b62-179">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="b6b62-179">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="b6b62-180">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="b6b62-180">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="b6b62-181">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b6b62-181">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

