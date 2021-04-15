---
description: A função EnumPrintProcessorDatatypes enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Função EnumPrintProcessorDatatypes (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505843"
---
# <a name="enumprintprocessordatatypes-function"></a><span data-ttu-id="8b942-103">Função EnumPrintProcessorDatatypes</span><span class="sxs-lookup"><span data-stu-id="8b942-103">EnumPrintProcessorDatatypes function</span></span>

<span data-ttu-id="8b942-104">A função **EnumPrintProcessorDatatypes** enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8b942-104">The **EnumPrintProcessorDatatypes** function enumerates the data types that a specified print processor supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b942-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b942-105">Syntax</span></span>


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="8b942-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b942-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b942-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b942-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o processador de impressão reside.</span><span class="sxs-lookup"><span data-stu-id="8b942-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor resides.</span></span> <span data-ttu-id="8b942-109">Se esse parâmetro for **nulo**, os tipos de dados do processador de impressão local serão enumerados.</span><span class="sxs-lookup"><span data-stu-id="8b942-109">If this parameter is **NULL**, the data types for the local print processor are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="8b942-110">*pPrintProcessorName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b942-110">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão cujos tipos de dados são enumerados.</span><span class="sxs-lookup"><span data-stu-id="8b942-111">A pointer to a null-terminated string that specifies the name of the print processor whose data types are enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="8b942-112">*Nível* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8b942-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-113">O tipo de informação retornado no buffer *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="8b942-113">The type of information returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="8b942-114">Esse parâmetro deve ser 1.</span><span class="sxs-lookup"><span data-stu-id="8b942-114">This parameter must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="8b942-115">*pDatatypes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8b942-115">*pDatatypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-116">Um ponteiro para um buffer que recebe uma matriz de tipos de conjuntos de [**\_ informações \_ 1**](datatypes-info-1.md) estruturas.</span><span class="sxs-lookup"><span data-stu-id="8b942-116">A pointer to a buffer that receives an array of [**DATATYPES\_INFO\_1**](datatypes-info-1.md) structures.</span></span> <span data-ttu-id="8b942-117">Cada estrutura descreve um tipo de dados disponível.</span><span class="sxs-lookup"><span data-stu-id="8b942-117">Each structure describes an available data type.</span></span> <span data-ttu-id="8b942-118">O buffer deve ser grande o suficiente para receber a matriz de estruturas e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.</span><span class="sxs-lookup"><span data-stu-id="8b942-118">The buffer must be large enough to receive the array of structures and any strings or other data to which the structure members point.</span></span>

<span data-ttu-id="8b942-119">Para determinar o tamanho do buffer necessário, chame **EnumPrintProcessorDatatypes** com *cbBuf* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="8b942-119">To determine the required buffer size, call **EnumPrintProcessorDatatypes** with *cbBuf* set to zero.</span></span> <span data-ttu-id="8b942-120">**EnumPrintProcessorDatatypes** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.</span><span class="sxs-lookup"><span data-stu-id="8b942-120">**EnumPrintProcessorDatatypes** fails, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, and the *pcbNeeded* parameter returns the size, in bytes, of the buffer required to hold the array of structures and their data.</span></span>

</dd> <dt>

<span data-ttu-id="8b942-121">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8b942-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-122">O tamanho, em bytes, do buffer apontado por *pDatatypes*.</span><span class="sxs-lookup"><span data-stu-id="8b942-122">The size, in bytes, of the buffer pointed to by *pDatatypes*.</span></span>

</dd> <dt>

<span data-ttu-id="8b942-123">*pcbNeeded* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8b942-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-124">Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pDatatypes* se a função for realizada com sucesso.</span><span class="sxs-lookup"><span data-stu-id="8b942-124">A pointer to a variable that receives the number of bytes copied to the *pDatatypes* buffer if the function succeeds.</span></span> <span data-ttu-id="8b942-125">Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="8b942-125">If the buffer is too small, the function fails and the variable receives the number of bytes required.</span></span>

</dd> <dt>

<span data-ttu-id="8b942-126">*pcReturned* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8b942-126">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b942-127">Um ponteiro para uma variável que recebe o número de estruturas retornadas no buffer *pDatatypes* .</span><span class="sxs-lookup"><span data-stu-id="8b942-127">A pointer to a variable that receives the number of structures returned in the *pDatatypes* buffer.</span></span> <span data-ttu-id="8b942-128">Este é o número de tipos de dados com suporte.</span><span class="sxs-lookup"><span data-stu-id="8b942-128">This is the number of supported data types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b942-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b942-129">Return value</span></span>

<span data-ttu-id="8b942-130">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8b942-130">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8b942-131">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="8b942-131">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b942-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b942-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8b942-133">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8b942-133">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8b942-134">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8b942-134">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8b942-135">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="8b942-135">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8b942-136">v</span><span class="sxs-lookup"><span data-stu-id="8b942-136">v</span></span>

<span data-ttu-id="8b942-137">A partir do Windows Vista, as informações de tipo de dados de servidores de impressão remotos são recuperadas de um cache local.</span><span class="sxs-lookup"><span data-stu-id="8b942-137">Starting with Windows Vista, the data type information from remote print servers is retrieved from a local cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b942-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b942-138">Requirements</span></span>



| <span data-ttu-id="8b942-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b942-139">Requirement</span></span> | <span data-ttu-id="8b942-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8b942-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b942-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b942-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8b942-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b942-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8b942-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b942-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8b942-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8b942-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8b942-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8b942-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b942-146"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b942-146"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8b942-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b942-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="8b942-148"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b942-148"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8b942-149">DLL</span><span class="sxs-lookup"><span data-stu-id="8b942-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b942-150"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8b942-150"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8b942-151">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="8b942-151">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8b942-152">**EnumPrintProcessorDatatypesW** (Unicode) e **EnumPrintProcessorDatatypesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8b942-152">**EnumPrintProcessorDatatypesW** (Unicode) and **EnumPrintProcessorDatatypesA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="8b942-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b942-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b942-154">Impressão</span><span class="sxs-lookup"><span data-stu-id="8b942-154">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8b942-155">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="8b942-155">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8b942-156">**Informações de tipos de tipo \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8b942-156">**DATATYPES\_INFO\_1**</span></span>](datatypes-info-1.md)
</dt> <dt>

[<span data-ttu-id="8b942-157">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="8b942-157">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> </dl>

 

