---
description: A função GetDefaultPrinter recupera o nome da impressora padrão para o usuário atual no computador local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: Função GetDefaultPrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811473"
---
# <a name="getdefaultprinter-function"></a><span data-ttu-id="0a97e-103">Função GetDefaultPrinter</span><span class="sxs-lookup"><span data-stu-id="0a97e-103">GetDefaultPrinter function</span></span>

<span data-ttu-id="0a97e-104">A função **GetDefaultPrinter** recupera o nome da impressora padrão para o usuário atual no computador local.</span><span class="sxs-lookup"><span data-stu-id="0a97e-104">The **GetDefaultPrinter** function retrieves the printer name of the default printer for the current user on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a97e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a97e-105">Syntax</span></span>


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="0a97e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a97e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a97e-107">*pszBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a97e-107">*pszBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a97e-108">Um ponteiro para um buffer que recebe uma cadeia de caracteres terminada em nulo que contém o nome da impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="0a97e-108">A pointer to a buffer that receives a null-terminated character string containing the default printer name.</span></span> <span data-ttu-id="0a97e-109">Se esse parâmetro for **NULL**, a função falhará e a variável apontada por *pcchBuffer* retornará o tamanho de buffer necessário, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a97e-109">If this parameter is **NULL**, the function fails and the variable pointed to by *pcchBuffer* returns the required buffer size, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="0a97e-110">*pcchBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="0a97e-110">*pcchBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a97e-111">Na entrada, especifica o tamanho, em caracteres, do buffer *pszBuffer* .</span><span class="sxs-lookup"><span data-stu-id="0a97e-111">On input, specifies the size, in characters, of the *pszBuffer* buffer.</span></span> <span data-ttu-id="0a97e-112">Na saída, recebe o tamanho, em caracteres, da cadeia de caracteres do nome da impressora, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="0a97e-112">On output, receives the size, in characters, of the printer name string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a97e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a97e-113">Return value</span></span>

<span data-ttu-id="0a97e-114">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero e a variável apontada por *pcchBuffer* conterá o número de caracteres copiados para o buffer *pszBuffer* , incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="0a97e-114">If the function succeeds, the return value is a nonzero value and the variable pointed to by *pcchBuffer* contains the number of characters copied to the *pszBuffer* buffer, including the terminating null character.</span></span>

<span data-ttu-id="0a97e-115">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="0a97e-115">If the function fails, the return value is zero.</span></span>



| <span data-ttu-id="0a97e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0a97e-116">Value</span></span>                       | <span data-ttu-id="0a97e-117">Significado</span><span class="sxs-lookup"><span data-stu-id="0a97e-117">Meaning</span></span>                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a97e-118">ERRO \_ de \_ buffer insuficiente</span><span class="sxs-lookup"><span data-stu-id="0a97e-118">ERROR\_INSUFFICIENT\_BUFFER</span></span> | <span data-ttu-id="0a97e-119">O buffer *pszBuffer* é muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="0a97e-119">The *pszBuffer* buffer is too small.</span></span> <span data-ttu-id="0a97e-120">A variável apontada por *pcchBuffer* contém o tamanho de buffer necessário, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="0a97e-120">The variable pointed to by *pcchBuffer* contains the required buffer size, in characters.</span></span> |
| <span data-ttu-id="0a97e-121">arquivo de erro \_ \_ não \_ encontrado</span><span class="sxs-lookup"><span data-stu-id="0a97e-121">ERROR\_FILE\_NOT\_FOUND</span></span>     | <span data-ttu-id="0a97e-122">Não há nenhuma impressora padrão.</span><span class="sxs-lookup"><span data-stu-id="0a97e-122">There is no default printer.</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="0a97e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a97e-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a97e-124">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="0a97e-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="0a97e-125">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0a97e-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="0a97e-126">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="0a97e-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a97e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a97e-127">Requirements</span></span>



| <span data-ttu-id="0a97e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a97e-128">Requirement</span></span> | <span data-ttu-id="0a97e-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0a97e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a97e-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a97e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0a97e-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0a97e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0a97e-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a97e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0a97e-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0a97e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0a97e-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0a97e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a97e-135"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a97e-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="0a97e-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a97e-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a97e-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a97e-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="0a97e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0a97e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a97e-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="0a97e-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="0a97e-140">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0a97e-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0a97e-141">**GetDefaultPrinterW** (Unicode) e **GetDefaultPrinterA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0a97e-141">**GetDefaultPrinterW** (Unicode) and **GetDefaultPrinterA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="0a97e-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a97e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a97e-143">Impressão</span><span class="sxs-lookup"><span data-stu-id="0a97e-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0a97e-144">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="0a97e-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="0a97e-145">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="0a97e-145">**SetDefaultPrinter**</span></span>](setdefaultprinter.md)
</dt> </dl>

 

 




