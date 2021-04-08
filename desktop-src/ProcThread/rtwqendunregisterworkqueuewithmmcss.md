---
description: Conclui uma solicitação assíncrona para cancelar o registro de uma fila de trabalho com uma tarefa do serviço de Agendador de classes de multimídia (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: Função RtwqEndUnregisterWorkQueueWithMMCSS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828698"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="115ee-103">Função RtwqEndUnregisterWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="115ee-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="115ee-104">Conclui uma solicitação assíncrona para cancelar o registro de uma fila de trabalho com uma tarefa do serviço de Agendador de classes de multimídia (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="115ee-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="115ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="115ee-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="115ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="115ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="115ee-107">*pResult*</span><span class="sxs-lookup"><span data-stu-id="115ee-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="115ee-108">Ponteiro para a interface [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="115ee-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="115ee-109">Passe o mesmo ponteiro que o seu objeto de retorno de chamada recebeu no método [**IRtwqAsyncCallback:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="115ee-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="115ee-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="115ee-110">Return value</span></span>

<span data-ttu-id="115ee-111">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="115ee-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="115ee-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="115ee-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="115ee-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="115ee-113">Requirements</span></span>



| <span data-ttu-id="115ee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="115ee-114">Requirement</span></span> | <span data-ttu-id="115ee-115">Valor</span><span class="sxs-lookup"><span data-stu-id="115ee-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="115ee-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="115ee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="115ee-117">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="115ee-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="115ee-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="115ee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="115ee-119">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="115ee-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="115ee-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="115ee-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="115ee-121"><dt>Nenhuma</dt></span><span class="sxs-lookup"><span data-stu-id="115ee-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="115ee-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="115ee-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="115ee-123"><dt>Rtworkq. lib</dt></span><span class="sxs-lookup"><span data-stu-id="115ee-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="115ee-124">DLL</span><span class="sxs-lookup"><span data-stu-id="115ee-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="115ee-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="115ee-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
