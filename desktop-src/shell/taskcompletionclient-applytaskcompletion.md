---
description: Inicia a conclusão da tarefa.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Método TaskCompletionClient:: ApplyTaskCompletion'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989054"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="2c51f-103">Método TaskCompletionClient:: ApplyTaskCompletion</span><span class="sxs-lookup"><span data-stu-id="2c51f-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="2c51f-104">Inicia a conclusão da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2c51f-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c51f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2c51f-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="2c51f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c51f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c51f-107">*ptcfCategory*</span><span class="sxs-lookup"><span data-stu-id="2c51f-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="2c51f-108">Um valor que indica a categoria da tarefa.</span><span class="sxs-lookup"><span data-stu-id="2c51f-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c51f-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2c51f-109">Return value</span></span>

<span data-ttu-id="2c51f-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2c51f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2c51f-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2c51f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c51f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c51f-112">Remarks</span></span>

<span data-ttu-id="2c51f-113">O único valor com suporte para *ptcfCategory* é 0x08000000.</span><span class="sxs-lookup"><span data-stu-id="2c51f-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c51f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c51f-114">Requirements</span></span>



| <span data-ttu-id="2c51f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c51f-115">Requirement</span></span> | <span data-ttu-id="2c51f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2c51f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c51f-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c51f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c51f-118">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2c51f-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c51f-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c51f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c51f-120">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="2c51f-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2c51f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2c51f-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c51f-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c51f-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c51f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c51f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c51f-124">**TaskCompletionClient**</span><span class="sxs-lookup"><span data-stu-id="2c51f-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




