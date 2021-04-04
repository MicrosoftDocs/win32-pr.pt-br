---
description: A função EnumPrinterDrivers enumera os drivers de impressora instalados em um servidor de impressora especificado.
ms.assetid: fa3d8cf4-70bc-4362-833e-e4217ed5d43b
title: Função EnumPrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrinterDrivers
- EnumPrinterDriversA
- EnumPrinterDriversW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: c5175daf0a59ac4231baa1a32772863a0017c45d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662120"
---
# <a name="enumprinterdrivers-function"></a><span data-ttu-id="3aecc-103">Função EnumPrinterDrivers</span><span class="sxs-lookup"><span data-stu-id="3aecc-103">EnumPrinterDrivers function</span></span>

<span data-ttu-id="3aecc-104">A função **EnumPrinterDrivers** enumera os drivers de impressora instalados em um servidor de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="3aecc-104">The **EnumPrinterDrivers** function enumerates the printer drivers installed on a specified printer server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aecc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3aecc-105">Syntax</span></span>


```C++
BOOL EnumPrinterDrivers(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="3aecc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3aecc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aecc-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual os drivers de impressora são enumerados.</span><span class="sxs-lookup"><span data-stu-id="3aecc-108">A pointer to a null-terminated string that specifies the name of the server on which the printer drivers are enumerated.</span></span>

<span data-ttu-id="3aecc-109">Se *pname* for **NULL**, a função enumerará os drivers de impressora local.</span><span class="sxs-lookup"><span data-stu-id="3aecc-109">If *pName* is **NULL**, the function enumerates the local printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="3aecc-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64, Windows x64 ou Windows NT R4000).</span><span class="sxs-lookup"><span data-stu-id="3aecc-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, Windows x64, or Windows NT R4000).</span></span> <span data-ttu-id="3aecc-112">Se esse parâmetro for **nulo**, a função usará o ambiente atual do chamador/cliente (não do destino/servidor).</span><span class="sxs-lookup"><span data-stu-id="3aecc-112">If this parameter is **NULL**, the function uses the current environment of the caller/client (not of the destination/server).</span></span>

<span data-ttu-id="3aecc-113">Se a cadeia de caracteres *pEnvironment* especificar "All", o **EnumPrinterDrivers** enumera drivers de impressora para todas as plataformas instaladas no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="3aecc-113">If the *pEnvironment* string specifies "all", **EnumPrinterDrivers** enumerates printer drivers for all platforms installed on the specified server.</span></span>

</dd> <dt>

<span data-ttu-id="3aecc-114">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-114">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-115">O tipo de estrutura de informações retornado no buffer *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="3aecc-115">The type of information structure returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="3aecc-116">Pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="3aecc-116">It can be one of the following.</span></span>



| <span data-ttu-id="3aecc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3aecc-117">Value</span></span>                                                                                                | <span data-ttu-id="3aecc-118">Significado</span><span class="sxs-lookup"><span data-stu-id="3aecc-118">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="3aecc-119"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-119"><dt>**1**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-120">**Informações do DRIVER \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3aecc-120">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)<br/> |
| <span id="2"></span><dl> <span data-ttu-id="3aecc-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-122">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3aecc-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="3aecc-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-124">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="3aecc-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="3aecc-125"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-126">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="3aecc-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="5"></span><dl> <span data-ttu-id="3aecc-127"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-127"><dt>**5**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-128">**Informações do DRIVER \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="3aecc-128">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="3aecc-129"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-129"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-130">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="3aecc-130">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="3aecc-131"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-131"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="3aecc-132">**Informações do DRIVER \_ \_ 8**</span><span class="sxs-lookup"><span data-stu-id="3aecc-132">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

</dd> <dt>

<span data-ttu-id="3aecc-133">*pDriverInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-133">*pDriverInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-134">Um ponteiro para um buffer que recebe uma matriz de estruturas de informações de DRIVER \_ \_ \* , conforme especificado pelo *nível*.</span><span class="sxs-lookup"><span data-stu-id="3aecc-134">A pointer to a buffer that receives an array of DRIVER\_INFO\_\* structures, as specified by *Level*.</span></span> <span data-ttu-id="3aecc-135">Cada estrutura contém dados que descrevem um driver de impressora disponível.</span><span class="sxs-lookup"><span data-stu-id="3aecc-135">Each structure contains data that describes an available printer driver.</span></span> <span data-ttu-id="3aecc-136">O buffer deve ser grande o suficiente para receber a matriz de estruturas e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.</span><span class="sxs-lookup"><span data-stu-id="3aecc-136">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="3aecc-137">Para determinar o tamanho do buffer necessário, chame **EnumPrinterDrivers** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="3aecc-137">To determine the required buffer size, call **EnumPrinterDrivers** with *cbBuf* set to zero.</span></span> <span data-ttu-id="3aecc-138">**EnumPrinterDrivers** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="3aecc-138">**EnumPrinterDrivers** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="3aecc-139">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-139">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-140">O tamanho, em bytes, do buffer apontado por *pDriverInfo*</span><span class="sxs-lookup"><span data-stu-id="3aecc-140">The size, in bytes, of the buffer pointed to by *pDriverInfo*</span></span>

</dd> <dt>

<span data-ttu-id="3aecc-141">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-141">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-142">Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pDriverInfo* se a função for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3aecc-142">A pointer to a variable that receives the number of bytes copied to the *pDriverInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="3aecc-143">Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="3aecc-143">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="3aecc-144">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-144">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aecc-145">Um ponteiro para uma variável que recebe o número de estruturas retornadas no buffer *pDriverInfo* .</span><span class="sxs-lookup"><span data-stu-id="3aecc-145">A pointer to a variable that receives the number of structures returned in the *pDriverInfo* buffer.</span></span> <span data-ttu-id="3aecc-146">Este é o número de drivers de impressora instalados no servidor de impressão especificado.</span><span class="sxs-lookup"><span data-stu-id="3aecc-146">This is the number of printer drivers installed on the specified print server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aecc-147">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3aecc-147">Return value</span></span>

<span data-ttu-id="3aecc-148">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3aecc-148">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="3aecc-149">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="3aecc-149">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aecc-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="3aecc-150">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3aecc-151">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3aecc-151">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3aecc-152">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3aecc-152">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3aecc-153">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="3aecc-153">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3aecc-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aecc-154">Requirements</span></span>



| <span data-ttu-id="3aecc-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aecc-155">Requirement</span></span> | <span data-ttu-id="3aecc-156">Valor</span><span class="sxs-lookup"><span data-stu-id="3aecc-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aecc-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aecc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="3aecc-158">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3aecc-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3aecc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="3aecc-160">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3aecc-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3aecc-161">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3aecc-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aecc-162"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-162"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3aecc-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3aecc-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="3aecc-164"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-164"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3aecc-165">DLL</span><span class="sxs-lookup"><span data-stu-id="3aecc-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aecc-166"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3aecc-166"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="3aecc-167">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3aecc-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3aecc-168">**EnumPrinterDriversW** (Unicode) e **EnumPrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3aecc-168">**EnumPrinterDriversW** (Unicode) and **EnumPrinterDriversA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="3aecc-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="3aecc-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aecc-170">Impressão</span><span class="sxs-lookup"><span data-stu-id="3aecc-170">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3aecc-171">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3aecc-171">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3aecc-172">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="3aecc-172">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="3aecc-173">**Informações do DRIVER \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3aecc-173">**DRIVER\_INFO\_1**</span></span>](driver-info-1.md)
</dt> <dt>

[<span data-ttu-id="3aecc-174">**Informações do DRIVER \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3aecc-174">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="3aecc-175">**Informações do DRIVER \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="3aecc-175">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="3aecc-176">**Informações do DRIVER \_ \_ 4**</span><span class="sxs-lookup"><span data-stu-id="3aecc-176">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="3aecc-177">**Informações do DRIVER \_ \_ 5**</span><span class="sxs-lookup"><span data-stu-id="3aecc-177">**DRIVER\_INFO\_5**</span></span>](driver-info-5.md)
</dt> <dt>

[<span data-ttu-id="3aecc-178">**Informações do DRIVER \_ \_ 6**</span><span class="sxs-lookup"><span data-stu-id="3aecc-178">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="3aecc-179">**GetPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="3aecc-179">**GetPrinterDriver**</span></span>](getprinterdriver.md)
</dt> </dl>

 

