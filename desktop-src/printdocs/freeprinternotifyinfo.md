---
description: A função FreePrinterNotifyInfo libera um buffer alocado pelo sistema criado pela função FindNextPrinterChangeNotification.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: Função FreePrinterNotifyInfo (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813736"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="8fd29-103">Função FreePrinterNotifyInfo</span><span class="sxs-lookup"><span data-stu-id="8fd29-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="8fd29-104">A função **FreePrinterNotifyInfo** libera um buffer alocado pelo sistema criado pela função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd29-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd29-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fd29-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="8fd29-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fd29-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fd29-107">*pPrinterNotifyInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fd29-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fd29-108">Ponteiro para um buffer de [**\_ \_ informações de notificação de impressora**](printer-notify-info.md) retornado de uma chamada para a função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd29-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="8fd29-109">**FreePrinterNotifyInfo** desaloca esse buffer.</span><span class="sxs-lookup"><span data-stu-id="8fd29-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fd29-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fd29-110">Return value</span></span>

<span data-ttu-id="8fd29-111">Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="8fd29-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8fd29-112">Se a função falhar, o valor retornado será zero.</span><span class="sxs-lookup"><span data-stu-id="8fd29-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fd29-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fd29-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8fd29-114">Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8fd29-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8fd29-115">A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8fd29-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8fd29-116">Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.</span><span class="sxs-lookup"><span data-stu-id="8fd29-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fd29-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fd29-117">Requirements</span></span>



| <span data-ttu-id="8fd29-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd29-118">Requirement</span></span> | <span data-ttu-id="8fd29-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8fd29-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd29-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fd29-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd29-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fd29-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8fd29-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fd29-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd29-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fd29-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8fd29-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8fd29-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fd29-125"><dt>Winspool. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8fd29-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8fd29-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8fd29-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="8fd29-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fd29-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8fd29-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8fd29-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fd29-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fd29-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="8fd29-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fd29-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fd29-131">Impressão</span><span class="sxs-lookup"><span data-stu-id="8fd29-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8fd29-132">Funções da API do Spooler de impressão</span><span class="sxs-lookup"><span data-stu-id="8fd29-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8fd29-133">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="8fd29-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="8fd29-134">**\_informações de notificação da impressora \_**</span><span class="sxs-lookup"><span data-stu-id="8fd29-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




