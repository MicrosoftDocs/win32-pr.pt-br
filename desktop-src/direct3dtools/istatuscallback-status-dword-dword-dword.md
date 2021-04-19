---
description: Uma função de retorno de chamada usada para notificar o host do progresso dos mecanismos. Isso também serve como uma maneira para o host determinar que o mecanismo ainda está em execução.
title: 'Método IStatusCallback:: status'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812339"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span data-ttu-id="7a782-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Método IStatusCallback:: status</span><span class="sxs-lookup"><span data-stu-id="7a782-104"><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status method</span></span>

<span data-ttu-id="7a782-105">Uma função de retorno de chamada usada para notificar o host do progresso do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="7a782-105">A callback function used to notify the host of the engine's progress.</span></span> <span data-ttu-id="7a782-106">Isso também serve como uma maneira para o host determinar que o mecanismo ainda está em execução.</span><span class="sxs-lookup"><span data-stu-id="7a782-106">This also serves as a way for the host to determine that the engine is still running.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a782-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a782-107">Syntax</span></span>


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a><span data-ttu-id="7a782-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a782-108">Parameters</span></span>

<span data-ttu-id="7a782-109">*dwMillisecondsElapsed* </span><span class="sxs-lookup"><span data-stu-id="7a782-109">*dwMillisecondsElapsed* </span></span>  
<span data-ttu-id="7a782-110">O tempo decorrido desde a última chamada para status, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="7a782-110">The time elapsed since the last call to Status, in milliseconds.</span></span>

<span data-ttu-id="7a782-111">*dwFramesCaptured* </span><span class="sxs-lookup"><span data-stu-id="7a782-111">*dwFramesCaptured* </span></span>  
<span data-ttu-id="7a782-112">O número de quadros que foram capturados desde a última chamada para o status.</span><span class="sxs-lookup"><span data-stu-id="7a782-112">The number of frames that have been captures since the last call to Status.</span></span>

<span data-ttu-id="7a782-113">*dwFramesElapsed* </span><span class="sxs-lookup"><span data-stu-id="7a782-113">*dwFramesElapsed* </span></span>  
<span data-ttu-id="7a782-114">O número de quadros decorridos desde a última chamada para o status.</span><span class="sxs-lookup"><span data-stu-id="7a782-114">The number of frames elapsed since the last call to Status.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a782-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a782-115">Return value</span></span>

<span data-ttu-id="7a782-116">Se esse método tiver sucesso, ele retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="7a782-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="7a782-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7a782-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a782-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a782-118">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="7a782-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7a782-119">Header</span></span></p></td><td><span data-ttu-id="7a782-120">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="7a782-120">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="7a782-121"><span id="see_also"></span>Confira também</span><span class="sxs-lookup"><span data-stu-id="7a782-121"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="7a782-122">**IStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="7a782-122">**IStatusCallback**</span></span>](/windows/desktop/direct3dtools/istatuscallback)

 

 
