---
description: A função ScheduleJob solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: Função ScheduleJob (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 1ef938cc2a9b1893a4825255325457d5c210842a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811731"
---
# <a name="schedulejob-function"></a><span data-ttu-id="e86b5-103">Função ScheduleJob</span><span class="sxs-lookup"><span data-stu-id="e86b5-103">ScheduleJob function</span></span>

<span data-ttu-id="e86b5-104">A função **ScheduleJob** solicita que o spooler de impressão agende um trabalho de impressão especificado para impressão.</span><span class="sxs-lookup"><span data-stu-id="e86b5-104">The **ScheduleJob** function requests that the print spooler schedule a specified print job for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e86b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e86b5-105">Syntax</span></span>


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a><span data-ttu-id="e86b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e86b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e86b5-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e86b5-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86b5-108">Um identificador para a impressora para o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="e86b5-108">A handle to the printer for the print job.</span></span> <span data-ttu-id="e86b5-109">Essa deve ser uma impressora local configurada como uma impressora em spool.</span><span class="sxs-lookup"><span data-stu-id="e86b5-109">This must be a local printer that is configured as a spooled printer.</span></span> <span data-ttu-id="e86b5-110">Se *hPrinter* for um identificador para uma conexão de impressora remota, ou se a impressora estiver configurada para impressão direta, a função **ScheduleJob** falhará.</span><span class="sxs-lookup"><span data-stu-id="e86b5-110">If *hPrinter* is a handle to a remote printer connection, or if the printer is configured for direct printing, the **ScheduleJob** function fails.</span></span> <span data-ttu-id="e86b5-111">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="e86b5-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

<span data-ttu-id="e86b5-112">*hPrinter* deve ser o mesmo identificador de impressora especificado na chamada para [**AddJob**](addjob.md) que obteve o identificador do trabalho de impressão *dwJobID* .</span><span class="sxs-lookup"><span data-stu-id="e86b5-112">*hPrinter* must be the same printer handle specified in the call to [**AddJob**](addjob.md) that obtained the *dwJobID* print job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e86b5-113">*dwJobID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e86b5-113">*dwJobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e86b5-114">O trabalho de impressão a ser agendado.</span><span class="sxs-lookup"><span data-stu-id="e86b5-114">The print job to be scheduled.</span></span> <span data-ttu-id="e86b5-115">Você obtém esse identificador de trabalho de impressão chamando a função [**AddJob**](addjob.md) .</span><span class="sxs-lookup"><span data-stu-id="e86b5-115">You obtain this print job identifier by calling the [**AddJob**](addjob.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e86b5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e86b5-116">Return value</span></span>

<span data-ttu-id="e86b5-117">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="e86b5-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e86b5-118">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="e86b5-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e86b5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e86b5-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e86b5-120">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e86b5-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e86b5-121">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e86b5-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e86b5-122">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="e86b5-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e86b5-123">Você deve chamar a função [**AddJob**](addjob.md) com êxito antes de chamar a função **ScheduleJob** .</span><span class="sxs-lookup"><span data-stu-id="e86b5-123">You must successfully call the [**AddJob**](addjob.md) function before calling the **ScheduleJob** function.</span></span> <span data-ttu-id="e86b5-124">**AddJob** Obtém o identificador do trabalho de impressão que você passa para o **ScheduleJob** como *dwJobID*.</span><span class="sxs-lookup"><span data-stu-id="e86b5-124">**AddJob** obtains the print job identifier that you pass to **ScheduleJob** as *dwJobID*.</span></span> <span data-ttu-id="e86b5-125">As duas chamadas devem usar o mesmo valor para *hPrinter*.</span><span class="sxs-lookup"><span data-stu-id="e86b5-125">Both calls must use the same value for *hPrinter*.</span></span>

<span data-ttu-id="e86b5-126">A função **ScheduleJob** verifica um arquivo de spool válido.</span><span class="sxs-lookup"><span data-stu-id="e86b5-126">The **ScheduleJob** function checks for a valid spool file.</span></span> <span data-ttu-id="e86b5-127">Se houver um arquivo de spool inválido, ou se estiver vazio, **ScheduleJob** excluirá o arquivo de spool e a entrada do trabalho de impressão correspondente no spooler de impressão.</span><span class="sxs-lookup"><span data-stu-id="e86b5-127">If there is an invalid spool file, or if it is empty, **ScheduleJob** deletes both the spool file and the corresponding print job entry in the print spooler.</span></span>

## <a name="requirements"></a><span data-ttu-id="e86b5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e86b5-128">Requirements</span></span>



| <span data-ttu-id="e86b5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e86b5-129">Requirement</span></span> | <span data-ttu-id="e86b5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e86b5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e86b5-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e86b5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e86b5-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e86b5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e86b5-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e86b5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e86b5-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e86b5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e86b5-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e86b5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e86b5-136"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e86b5-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e86b5-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e86b5-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e86b5-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e86b5-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e86b5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e86b5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e86b5-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e86b5-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="e86b5-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e86b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e86b5-142">Impressão</span><span class="sxs-lookup"><span data-stu-id="e86b5-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e86b5-143">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="e86b5-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e86b5-144">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="e86b5-144">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="e86b5-145">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="e86b5-145">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




