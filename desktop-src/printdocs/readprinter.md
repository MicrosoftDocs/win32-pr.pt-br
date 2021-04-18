---
description: A função ReadPrinter recupera dados da impressora especificada.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: Função ReadPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788913"
---
# <a name="readprinter-function"></a><span data-ttu-id="e748b-103">Função ReadPrinter</span><span class="sxs-lookup"><span data-stu-id="e748b-103">ReadPrinter function</span></span>

<span data-ttu-id="e748b-104">A função **ReadPrinter** recupera dados da impressora especificada.</span><span class="sxs-lookup"><span data-stu-id="e748b-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e748b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e748b-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="e748b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e748b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e748b-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e748b-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e748b-108">Um identificador para o objeto de impressora para o qual recuperar dados.</span><span class="sxs-lookup"><span data-stu-id="e748b-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="e748b-109">Use a função [**OpenPrinter**](openprinter.md) para recuperar um identificador de objeto de impressora.</span><span class="sxs-lookup"><span data-stu-id="e748b-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="e748b-110">Use o formato: PrinterName, trabalho xxxx.</span><span class="sxs-lookup"><span data-stu-id="e748b-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="e748b-111">*pBuf* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e748b-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e748b-112">Um ponteiro para um buffer que recebe os dados da impressora.</span><span class="sxs-lookup"><span data-stu-id="e748b-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="e748b-113">*cbBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e748b-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e748b-114">O tamanho, em bytes, do buffer para o qual *pBuf* aponta.</span><span class="sxs-lookup"><span data-stu-id="e748b-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="e748b-115">*pNoBytesRead* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e748b-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e748b-116">Um ponteiro para uma variável que recebe o número de bytes de dados copiados para a matriz para a qual *pBuf* aponta.</span><span class="sxs-lookup"><span data-stu-id="e748b-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e748b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e748b-117">Return value</span></span>

<span data-ttu-id="e748b-118">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e748b-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e748b-119">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="e748b-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e748b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="e748b-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e748b-121">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e748b-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e748b-122">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e748b-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e748b-123">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e748b-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e748b-124">**ReadPrinter** retornará um erro se o dispositivo ou a impressora não for bidirecional.</span><span class="sxs-lookup"><span data-stu-id="e748b-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="e748b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e748b-125">Requirements</span></span>



| <span data-ttu-id="e748b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e748b-126">Requirement</span></span> | <span data-ttu-id="e748b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e748b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e748b-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e748b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e748b-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e748b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e748b-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e748b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e748b-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e748b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e748b-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e748b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e748b-133"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e748b-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e748b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e748b-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="e748b-135"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e748b-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e748b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e748b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e748b-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e748b-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e748b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e748b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e748b-139">Impressão</span><span class="sxs-lookup"><span data-stu-id="e748b-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e748b-140">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e748b-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e748b-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e748b-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




