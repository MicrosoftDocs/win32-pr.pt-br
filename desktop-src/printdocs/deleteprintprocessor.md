---
description: A função DeletePrintProcessor remove um processador de impressão adicionado pela função AddPrintProcessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Função DeletePrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169349"
---
# <a name="deleteprintprocessor-function"></a><span data-ttu-id="93ddd-103">Função DeletePrintProcessor</span><span class="sxs-lookup"><span data-stu-id="93ddd-103">DeletePrintProcessor function</span></span>

<span data-ttu-id="93ddd-104">A função **DeletePrintProcessor** remove um processador de impressão adicionado pela função [**AddPrintProcessor**](addprintprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="93ddd-104">The **DeletePrintProcessor** function removes a print processor added by the [**AddPrintProcessor**](addprintprocessor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ddd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93ddd-105">Syntax</span></span>


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="93ddd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93ddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93ddd-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ddd-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ddd-108">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o processador deve ser removido.</span><span class="sxs-lookup"><span data-stu-id="93ddd-108">A pointer to a null-terminated string that specifies the name of the server from which the processor is to be removed.</span></span> <span data-ttu-id="93ddd-109">Se esse parâmetro for **nulo**, o processador da impressora será removido localmente.</span><span class="sxs-lookup"><span data-stu-id="93ddd-109">If this parameter is **NULL**, the printer processor is removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="93ddd-110">*pEnvironment* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ddd-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ddd-111">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o processador deve ser removido (por exemplo, Windows NT x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="93ddd-111">A pointer to a null-terminated string that specifies the environment from which the processor is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="93ddd-112">Se esse parâmetro for **nulo**, o processador será removido do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).</span><span class="sxs-lookup"><span data-stu-id="93ddd-112">If this parameter is **NULL**, the processor is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="93ddd-113">**NULL** é o valor recomendado, pois fornece a portabilidade máxima.</span><span class="sxs-lookup"><span data-stu-id="93ddd-113">**NULL** is the recommended value, as it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="93ddd-114">*pPrintProcessorName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="93ddd-114">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93ddd-115">Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador a ser removido.</span><span class="sxs-lookup"><span data-stu-id="93ddd-115">A pointer to a null-terminated string that specifies the name of the processor to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93ddd-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93ddd-116">Return value</span></span>

<span data-ttu-id="93ddd-117">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="93ddd-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="93ddd-118">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="93ddd-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="93ddd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="93ddd-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="93ddd-120">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="93ddd-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="93ddd-121">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="93ddd-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="93ddd-122">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="93ddd-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="93ddd-123">O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="93ddd-123">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

## <a name="requirements"></a><span data-ttu-id="93ddd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93ddd-124">Requirements</span></span>



| <span data-ttu-id="93ddd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="93ddd-125">Requirement</span></span> | <span data-ttu-id="93ddd-126">Valor</span><span class="sxs-lookup"><span data-stu-id="93ddd-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93ddd-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93ddd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="93ddd-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93ddd-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="93ddd-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93ddd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="93ddd-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="93ddd-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="93ddd-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="93ddd-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ddd-132"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93ddd-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="93ddd-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93ddd-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="93ddd-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93ddd-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="93ddd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="93ddd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93ddd-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="93ddd-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="93ddd-137">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="93ddd-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="93ddd-138">**DeletePrintProcessorW** (Unicode) e **DeletePrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="93ddd-138">**DeletePrintProcessorW** (Unicode) and **DeletePrintProcessorA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="93ddd-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="93ddd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93ddd-140">Impressão</span><span class="sxs-lookup"><span data-stu-id="93ddd-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="93ddd-141">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="93ddd-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="93ddd-142">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="93ddd-142">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

