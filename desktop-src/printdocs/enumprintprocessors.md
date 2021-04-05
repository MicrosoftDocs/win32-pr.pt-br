---
description: A função EnumPrintProcessors enumera os processadores de impressão instalados no servidor especificado.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Função EnumPrintProcessors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0c446c39cdfc37ae7c578f5123afe57d61519704
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922070"
---
# <a name="enumprintprocessors-function"></a><span data-ttu-id="6f876-103">Função EnumPrintProcessors</span><span class="sxs-lookup"><span data-stu-id="6f876-103">EnumPrintProcessors function</span></span>

<span data-ttu-id="6f876-104">A função **EnumPrintProcessors** enumera os processadores de impressão instalados no servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="6f876-104">The **EnumPrintProcessors** function enumerates the print processors installed on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f876-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f876-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="6f876-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f876-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f876-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6f876-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual os processadores de impressão residem.</span><span class="sxs-lookup"><span data-stu-id="6f876-108">A pointer to a null-terminated string that specifies the name of the server on which the print processors reside.</span></span> <span data-ttu-id="6f876-109">Se esse parâmetro for **nulo**, os processadores de impressão local serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="6f876-109">If this parameter is **NULL**, the local print processors are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="6f876-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6f876-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="6f876-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="6f876-112">Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.</span><span class="sxs-lookup"><span data-stu-id="6f876-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="6f876-113">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="6f876-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-114">O tipo de informação retornado no buffer *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="6f876-114">The type of information returned in the *pPrintProcessorInfo* buffer.</span></span> <span data-ttu-id="6f876-115">Esse parâmetro deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="6f876-115">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="6f876-116">*pPrintProcessorInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f876-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-117">Um ponteiro para um buffer que recebe uma matriz de estruturas de [**informações do multiprocessador \_ \_ 1**](printprocessor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="6f876-117">A pointer to a buffer that receives an array of [**PRINTPROCESSOR\_INFO\_1**](printprocessor-info-1.md) structures.</span></span> <span data-ttu-id="6f876-118">Cada estrutura descreve um processador de impressão disponível.</span><span class="sxs-lookup"><span data-stu-id="6f876-118">Each structure describes an available print processor.</span></span> <span data-ttu-id="6f876-119">O buffer deve ser grande o suficiente para receber a matriz de estruturas e todas as cadeias de caracteres às quais os membros da estrutura apontam.</span><span class="sxs-lookup"><span data-stu-id="6f876-119">The buffer must be large enough to receive the array of structures and any strings to which the structure members point.</span></span>

<span data-ttu-id="6f876-120">Para determinar o tamanho do buffer necessário, chame **EnumPrintProcessors** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6f876-120">To determine the required buffer size, call **EnumPrintProcessors** with *cbBuf* set to zero.</span></span> <span data-ttu-id="6f876-121">**EnumPrintProcessors** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="6f876-121">**EnumPrintProcessors** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="6f876-122">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6f876-122">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-123">O tamanho, em bytes, do buffer apontado por *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="6f876-123">The size, in bytes, of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="6f876-124">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f876-124">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-125">Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pPrintProcessorInfo* se a função for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="6f876-125">A pointer to a variable that receives the number of bytes copied to the *pPrintProcessorInfo* buffer if the function succeeds.</span></span> <span data-ttu-id="6f876-126">Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="6f876-126">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="6f876-127">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6f876-127">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f876-128">Um ponteiro para uma variável que recebe o número de estruturas retornadas no buffer *pPrintProcessorInfo* .</span><span class="sxs-lookup"><span data-stu-id="6f876-128">A pointer to a variable that receives the number of structures returned in the *pPrintProcessorInfo* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f876-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f876-129">Return value</span></span>

<span data-ttu-id="6f876-130">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6f876-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="6f876-131">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="6f876-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f876-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f876-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6f876-133">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6f876-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6f876-134">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6f876-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6f876-135">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="6f876-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f876-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f876-136">Requirements</span></span>



| <span data-ttu-id="6f876-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f876-137">Requirement</span></span> | <span data-ttu-id="6f876-138">Valor</span><span class="sxs-lookup"><span data-stu-id="6f876-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f876-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f876-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6f876-140">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f876-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6f876-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f876-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6f876-142">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6f876-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6f876-143">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6f876-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f876-144"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f876-144"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6f876-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f876-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="6f876-146"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f876-146"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6f876-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6f876-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f876-148"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6f876-148"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6f876-149">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6f876-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6f876-150">**EnumPrintProcessorsW** (Unicode) e **EnumPrintProcessorsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6f876-150">**EnumPrintProcessorsW** (Unicode) and **EnumPrintProcessorsA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="6f876-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f876-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f876-152">Impressão</span><span class="sxs-lookup"><span data-stu-id="6f876-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6f876-153">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="6f876-153">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6f876-154">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="6f876-154">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> <dt>

[<span data-ttu-id="6f876-155">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="6f876-155">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="6f876-156">**Informações do multiprocessador \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="6f876-156">**PRINTPROCESSOR\_INFO\_1**</span></span>](printprocessor-info-1.md)
</dt> </dl>

 

