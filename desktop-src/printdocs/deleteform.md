---
description: A função DeleteForm remove um nome de formulário da lista de formulários com suporte.
ms.assetid: a2d0345f-2469-46ab-935f-777f2b33b621
title: Função DeleteForm (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteForm
- DeleteFormA
- DeleteFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 70ead5026c3b5cf21b28d230f79819bf71eeaf10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011008"
---
# <a name="deleteform-function"></a><span data-ttu-id="f87ee-103">Função DeleteForm</span><span class="sxs-lookup"><span data-stu-id="f87ee-103">DeleteForm function</span></span>

<span data-ttu-id="f87ee-104">A função **DeleteForm** remove um nome de formulário da lista de formulários com suporte.</span><span class="sxs-lookup"><span data-stu-id="f87ee-104">The **DeleteForm** function removes a form name from the list of supported forms.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f87ee-105">Syntax</span></span>


```C++
BOOL DeleteForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName
);
```



## <a name="parameters"></a><span data-ttu-id="f87ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f87ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87ee-107">*hPrinter* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f87ee-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f87ee-108">Indica o identificador de impressora aberta no qual essa função deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="f87ee-108">Indicates the open printer handle that this function is to be performed upon.</span></span> <span data-ttu-id="f87ee-109">Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.</span><span class="sxs-lookup"><span data-stu-id="f87ee-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="f87ee-110">*pFormName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f87ee-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f87ee-111">Ponteiro para o nome do formulário a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f87ee-111">Pointer to the form name to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87ee-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f87ee-112">Return value</span></span>

<span data-ttu-id="f87ee-113">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="f87ee-113">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="f87ee-114">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="f87ee-114">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f87ee-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f87ee-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f87ee-116">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="f87ee-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f87ee-117">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f87ee-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f87ee-118">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="f87ee-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f87ee-119">**DeleteForm** só pode excluir nomes de formulário que foram adicionados usando a função [**AddForm**](addform.md) .</span><span class="sxs-lookup"><span data-stu-id="f87ee-119">**DeleteForm** can only delete form names that were added by using the [**AddForm**](addform.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87ee-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f87ee-120">Requirements</span></span>



| <span data-ttu-id="f87ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f87ee-121">Requirement</span></span> | <span data-ttu-id="f87ee-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f87ee-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87ee-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f87ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f87ee-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f87ee-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f87ee-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f87ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f87ee-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f87ee-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f87ee-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f87ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f87ee-128"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f87ee-128"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f87ee-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f87ee-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="f87ee-130"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f87ee-130"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f87ee-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f87ee-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f87ee-132"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="f87ee-132"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="f87ee-133">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f87ee-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f87ee-134">**DeleteFormW** (Unicode) e **DeleteFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f87ee-134">**DeleteFormW** (Unicode) and **DeleteFormA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="f87ee-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f87ee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87ee-136">Impressão</span><span class="sxs-lookup"><span data-stu-id="f87ee-136">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f87ee-137">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="f87ee-137">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="f87ee-138">**AddFormat**</span><span class="sxs-lookup"><span data-stu-id="f87ee-138">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="f87ee-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="f87ee-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




