---
description: A função GetFrameTimeStamp retorna o carimbo de data/hora de um determinado quadro.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Função GetFrameTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757499"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="90d07-103">Função GetFrameTimeStamp</span><span class="sxs-lookup"><span data-stu-id="90d07-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="90d07-104">A função **GetFrameTimeStamp** retorna o carimbo de data/hora de um determinado quadro.</span><span class="sxs-lookup"><span data-stu-id="90d07-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="90d07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90d07-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="90d07-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90d07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90d07-107">*hFrame* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90d07-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90d07-108">Identificador para o quadro.</span><span class="sxs-lookup"><span data-stu-id="90d07-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90d07-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90d07-109">Return value</span></span>

<span data-ttu-id="90d07-110">Se a função for bem-sucedida, o valor de retorno será o carimbo de data/hora do quadro em microssegundos.</span><span class="sxs-lookup"><span data-stu-id="90d07-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="90d07-111">Se a função não for bem-sucedida, o valor de retorno será menos um (-1).</span><span class="sxs-lookup"><span data-stu-id="90d07-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="90d07-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="90d07-112">Remarks</span></span>

<span data-ttu-id="90d07-113">A função **GetFrameTimeStamp** retorna um carimbo de data/hora que mostra o tempo decorrido entre o início do processo de captura e a gravação do quadro.</span><span class="sxs-lookup"><span data-stu-id="90d07-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="90d07-114">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetFrameTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="90d07-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="90d07-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90d07-115">Requirements</span></span>



| <span data-ttu-id="90d07-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="90d07-116">Requirement</span></span> | <span data-ttu-id="90d07-117">Valor</span><span class="sxs-lookup"><span data-stu-id="90d07-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="90d07-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90d07-118">Minimum supported client</span></span><br/> | <span data-ttu-id="90d07-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90d07-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="90d07-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90d07-120">Minimum supported server</span></span><br/> | <span data-ttu-id="90d07-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="90d07-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="90d07-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="90d07-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="90d07-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="90d07-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="90d07-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90d07-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="90d07-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90d07-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="90d07-126">DLL</span><span class="sxs-lookup"><span data-stu-id="90d07-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90d07-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90d07-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




