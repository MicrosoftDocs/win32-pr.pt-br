---
description: A função DeletePrinter exclui o objeto de impressora especificado.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: Função DeletePrinter (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 16d82a263b09c87f5c9b9725db48dd6634404ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813526"
---
# <a name="deleteprinter-function"></a><span data-ttu-id="fb96b-103">Função DeletePrinter</span><span class="sxs-lookup"><span data-stu-id="fb96b-103">DeletePrinter function</span></span>

<span data-ttu-id="fb96b-104">A função **DeletePrinter** exclui o objeto de impressora especificado.</span><span class="sxs-lookup"><span data-stu-id="fb96b-104">The **DeletePrinter** function deletes the specified printer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb96b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb96b-105">Syntax</span></span>


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="fb96b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb96b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb96b-107">*hPrinter* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fb96b-107">*hPrinter* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb96b-108">Identificador para um objeto de impressora que será excluído.</span><span class="sxs-lookup"><span data-stu-id="fb96b-108">Handle to a printer object that will be deleted.</span></span> <span data-ttu-id="fb96b-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="fb96b-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb96b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fb96b-110">Return value</span></span>

<span data-ttu-id="fb96b-111">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fb96b-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="fb96b-112">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="fb96b-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb96b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb96b-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fb96b-114">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="fb96b-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="fb96b-115">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb96b-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="fb96b-116">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="fb96b-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="fb96b-117">Se houver trabalhos de impressão restantes para serem processados para a impressora especificada, o **DeletePrinter** marcará a impressora para exclusão pendente e a excluirá quando todos os trabalhos de impressão tiverem sido impressos.</span><span class="sxs-lookup"><span data-stu-id="fb96b-117">If there are print jobs remaining to be processed for the specified printer, **DeletePrinter** marks the printer for pending deletion, and then deletes it when all the print jobs have been printed.</span></span> <span data-ttu-id="fb96b-118">Nenhum trabalho de impressão pode ser adicionado a uma impressora marcada para exclusão pendente.</span><span class="sxs-lookup"><span data-stu-id="fb96b-118">No print jobs can be added to a printer that is marked for pending deletion.</span></span>

<span data-ttu-id="fb96b-119">Uma impressora marcada para exclusão pendente não pode ser mantida, mas seus trabalhos de impressão podem ser retidos, retomados e reiniciados.</span><span class="sxs-lookup"><span data-stu-id="fb96b-119">A printer marked for pending deletion cannot be held, but its print jobs can be held, resumed, and restarted.</span></span> <span data-ttu-id="fb96b-120">Se a impressora for mantida e houver trabalhos para a impressora, **DeletePrinter** falhará com o erro \_ acesso \_ negado.</span><span class="sxs-lookup"><span data-stu-id="fb96b-120">If the printer is held and there are jobs for the printer, **DeletePrinter** fails with ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="fb96b-121">Observe que o **DeletePrinter** não fecha o identificador que é passado para ele.</span><span class="sxs-lookup"><span data-stu-id="fb96b-121">Note that **DeletePrinter** does not close the handle that is passed to it.</span></span> <span data-ttu-id="fb96b-122">Portanto, o aplicativo ainda deve chamar [**ClosePrinter**](closeprinter.md).</span><span class="sxs-lookup"><span data-stu-id="fb96b-122">Thus, the application must still call [**ClosePrinter**](closeprinter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb96b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb96b-123">Requirements</span></span>



| <span data-ttu-id="fb96b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb96b-124">Requirement</span></span> | <span data-ttu-id="fb96b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fb96b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb96b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb96b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fb96b-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb96b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fb96b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb96b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fb96b-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fb96b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fb96b-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fb96b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb96b-131"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb96b-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="fb96b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fb96b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="fb96b-133"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb96b-133"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="fb96b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="fb96b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb96b-135"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb96b-135"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="fb96b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb96b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb96b-137">Impressão</span><span class="sxs-lookup"><span data-stu-id="fb96b-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="fb96b-138">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="fb96b-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="fb96b-139">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="fb96b-139">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="fb96b-140">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="fb96b-140">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="fb96b-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="fb96b-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




