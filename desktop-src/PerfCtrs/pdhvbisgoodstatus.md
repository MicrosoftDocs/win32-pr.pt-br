---
description: A função PdhVbIsGoodStatus testa um valor de status para determinar se ele é um código de êxito ou de falha. Se o valor de status for bem-sucedido, o valor de retorno será diferente de zero. Se for um código de status de falha, o valor de retorno será zero.
ms.assetid: bdca8f64-5dcd-4ecb-ba95-72f7a56c0439
title: Função PdhVbIsGoodStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbIsGoodStatus
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: d21686be0398a84a57a303ad816b8a25f50aa611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756698"
---
# <a name="pdhvbisgoodstatus-function"></a><span data-ttu-id="48f58-105">Função PdhVbIsGoodStatus</span><span class="sxs-lookup"><span data-stu-id="48f58-105">PdhVbIsGoodStatus function</span></span>

<span data-ttu-id="48f58-106">A função **PdhVbIsGoodStatus** testa um valor de status para determinar se ele é um código de êxito ou de falha.</span><span class="sxs-lookup"><span data-stu-id="48f58-106">The **PdhVbIsGoodStatus** function tests a status value to determine if it is a success or failure code.</span></span> <span data-ttu-id="48f58-107">Se o valor de status for bem-sucedido, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="48f58-107">If the status value is a successful one, then the return value will be nonzero.</span></span> <span data-ttu-id="48f58-108">Se for um código de status de falha, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="48f58-108">If it is a failure status code, the return value will be zero.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48f58-109">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="48f58-109">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="48f58-110">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="48f58-110">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="48f58-111">Função PdhVbIsGoodStatus ( \_ ByVal statusvalue como longo \_ ) enquanto longo</span><span class="sxs-lookup"><span data-stu-id="48f58-111">Function PdhVbIsGoodStatus( \_ ByVal StatusValue As Long \_ ) As Long</span></span>

## <a name="parameters"></a><span data-ttu-id="48f58-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48f58-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48f58-113">*Statusvalue*</span><span class="sxs-lookup"><span data-stu-id="48f58-113">*StatusValue*</span></span> 
</dt> <dd>

<span data-ttu-id="48f58-114">Valor de status retornado por outra função PDH a ser testada.</span><span class="sxs-lookup"><span data-stu-id="48f58-114">Status value returned by another PDH function that is to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48f58-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48f58-115">Return value</span></span>

<span data-ttu-id="48f58-116">A função retornará zero se o código de status for um código de status de falha.</span><span class="sxs-lookup"><span data-stu-id="48f58-116">The function returns zero if the status code is a failure status code.</span></span> <span data-ttu-id="48f58-117">Ele retornará diferente de zero se o código de status for um código de status de êxito.</span><span class="sxs-lookup"><span data-stu-id="48f58-117">It returns nonzero if the status code is a success status code.</span></span>

## <a name="requirements"></a><span data-ttu-id="48f58-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48f58-118">Requirements</span></span>



| <span data-ttu-id="48f58-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="48f58-119">Requirement</span></span> | <span data-ttu-id="48f58-120">Valor</span><span class="sxs-lookup"><span data-stu-id="48f58-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="48f58-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="48f58-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="48f58-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="48f58-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48f58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="48f58-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48f58-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="48f58-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="48f58-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="48f58-126"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48f58-126"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="48f58-127">DLL</span><span class="sxs-lookup"><span data-stu-id="48f58-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48f58-128"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48f58-128"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48f58-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="48f58-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48f58-130">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="48f58-130">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
</dt> </dl>

 

 




