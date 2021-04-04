---
description: A função FindClosePrinterChangeNotification fecha um objeto de notificação de alteração criado chamando a função FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Função FindClosePrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010974"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="9f878-103">Função FindClosePrinterChangeNotification</span><span class="sxs-lookup"><span data-stu-id="9f878-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="9f878-104">A função **FindClosePrinterChangeNotification** fecha um objeto de notificação de alteração criado chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="9f878-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="9f878-105">A impressora ou o servidor de impressão associado ao objeto de notificação de alteração não será mais monitorado por esse objeto.</span><span class="sxs-lookup"><span data-stu-id="9f878-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f878-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f878-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="9f878-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f878-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f878-108">*hChange* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9f878-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f878-109">Um identificador para o objeto de notificação de alteração a ser fechado.</span><span class="sxs-lookup"><span data-stu-id="9f878-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="9f878-110">Trata-se de um identificador criado chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="9f878-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f878-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f878-111">Return value</span></span>

<span data-ttu-id="9f878-112">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9f878-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="9f878-113">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="9f878-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f878-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f878-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9f878-115">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="9f878-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="9f878-116">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9f878-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="9f878-117">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="9f878-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="9f878-118">Depois de chamar a função **FindClosePrinterChangeNotification** , você não poderá usar o identificador *hChange* em chamadas subsequentes para [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ou [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="9f878-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f878-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f878-119">Requirements</span></span>



| <span data-ttu-id="9f878-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f878-120">Requirement</span></span> | <span data-ttu-id="9f878-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9f878-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f878-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f878-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f878-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f878-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f878-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f878-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f878-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9f878-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f878-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9f878-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f878-127"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f878-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9f878-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f878-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f878-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f878-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="9f878-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9f878-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f878-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f878-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="9f878-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f878-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f878-133">Impressão</span><span class="sxs-lookup"><span data-stu-id="9f878-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9f878-134">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="9f878-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="9f878-135">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="9f878-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="9f878-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="9f878-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




