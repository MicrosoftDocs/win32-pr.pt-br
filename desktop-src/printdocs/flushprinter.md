---
description: A função FlushPrinter envia um buffer para a impressora a fim de limpá-lo de um estado transitório.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: Função FlushPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: d46a4a8d7143e10fc13722d278ca21a0602b7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505842"
---
# <a name="flushprinter-function"></a><span data-ttu-id="3fb32-103">Função FlushPrinter</span><span class="sxs-lookup"><span data-stu-id="3fb32-103">FlushPrinter function</span></span>

<span data-ttu-id="3fb32-104">A função **FlushPrinter** envia um buffer para a impressora a fim de limpá-lo de um estado transitório.</span><span class="sxs-lookup"><span data-stu-id="3fb32-104">The **FlushPrinter** function sends a buffer to the printer in order to clear it from a transient state.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fb32-105">Syntax</span></span>


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a><span data-ttu-id="3fb32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fb32-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb32-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb32-108">Um identificador para o objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="3fb32-108">A handle to the printer object.</span></span> <span data-ttu-id="3fb32-109">Deve ser o mesmo identificador que foi usado, em uma chamada [**WritePrinter**](writeprinter.md) anterior, pelo driver de impressora.</span><span class="sxs-lookup"><span data-stu-id="3fb32-109">This should be the same handle that was used, in a prior [**WritePrinter**](writeprinter.md) call, by the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="3fb32-110">*pBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-110">*pBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb32-111">Um ponteiro para uma matriz de bytes que contém os dados a serem gravados na impressora.</span><span class="sxs-lookup"><span data-stu-id="3fb32-111">A pointer to an array of bytes that contains the data to be written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="3fb32-112">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-112">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb32-113">O tamanho, em bytes, da matriz apontada por *pBuf*.</span><span class="sxs-lookup"><span data-stu-id="3fb32-113">The size, in bytes, of the array pointed to by *pBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="3fb32-114">*pcWritten* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-114">*pcWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb32-115">Um ponteiro para um valor que recebe o número de bytes de dados que foram gravados na impressora.</span><span class="sxs-lookup"><span data-stu-id="3fb32-115">A pointer to a value that receives the number of bytes of data that were written to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="3fb32-116">*cSleep* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-116">*cSleep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fb32-117">O tempo, em milissegundos, para o qual a linha de e/s para a porta de impressora deve ser mantida ociosa.</span><span class="sxs-lookup"><span data-stu-id="3fb32-117">The time, in milliseconds, for which the I/O line to the printer port should be kept idle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb32-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3fb32-118">Return value</span></span>

<span data-ttu-id="3fb32-119">Se a função for bem-sucedida, o valor retornado será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3fb32-119">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="3fb32-120">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="3fb32-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb32-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fb32-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3fb32-122">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3fb32-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="3fb32-123">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3fb32-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="3fb32-124">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="3fb32-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="3fb32-125">**FlushPrinter** deverá ser chamado somente se [**WritePrinter**](writeprinter.md) falhar, deixando a impressora em um estado transitório.</span><span class="sxs-lookup"><span data-stu-id="3fb32-125">**FlushPrinter** should be called only if [**WritePrinter**](writeprinter.md) failed, leaving the printer in a transient state.</span></span> <span data-ttu-id="3fb32-126">Por exemplo, a impressora pode entrar em um estado transitório quando o trabalho é anulado e o driver de impressora enviou parcialmente alguns dados brutos para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3fb32-126">For example, the printer could get into a transient state when the job gets aborted and the printer driver has partially sent some raw data to the printer.</span></span>

<span data-ttu-id="3fb32-127">**FlushPrinter** também pode especificar um período ocioso durante o qual o spooler de impressão não agenda nenhum trabalho para a porta de impressora correspondente.</span><span class="sxs-lookup"><span data-stu-id="3fb32-127">**FlushPrinter** also can specify an idle period during which the print spooler does not schedule any jobs to the corresponding printer port.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb32-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb32-128">Requirements</span></span>



| <span data-ttu-id="3fb32-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb32-129">Requirement</span></span> | <span data-ttu-id="3fb32-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3fb32-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb32-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fb32-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb32-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3fb32-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fb32-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb32-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3fb32-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3fb32-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3fb32-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb32-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fb32-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="3fb32-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fb32-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="3fb32-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fb32-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="3fb32-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3fb32-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fb32-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="3fb32-140"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="3fb32-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fb32-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb32-142">Impressão</span><span class="sxs-lookup"><span data-stu-id="3fb32-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="3fb32-143">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="3fb32-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="3fb32-144">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="3fb32-144">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




