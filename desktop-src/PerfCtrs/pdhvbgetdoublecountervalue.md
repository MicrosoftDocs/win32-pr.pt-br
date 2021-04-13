---
description: A função PdhVbGetDoubleCounterValue retorna o valor atual do contador especificado como um valor de ponto flutuante de precisão dupla.
ms.assetid: a2ee63dd-da39-4104-921d-371172bcb45c
title: Função PdhVbGetDoubleCounterValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetDoubleCounterValue
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 67f0372a26649fbe781cf4d9bd25794b82d6346e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296751"
---
# <a name="pdhvbgetdoublecountervalue-function"></a><span data-ttu-id="27c54-103">Função PdhVbGetDoubleCounterValue</span><span class="sxs-lookup"><span data-stu-id="27c54-103">PdhVbGetDoubleCounterValue function</span></span>

<span data-ttu-id="27c54-104">A função **PdhVbGetDoubleCounterValue** retorna o valor atual do contador especificado como um valor de ponto flutuante de precisão dupla.</span><span class="sxs-lookup"><span data-stu-id="27c54-104">The **PdhVbGetDoubleCounterValue** function returns the current value of the specified counter as a double-precision floating point value.</span></span> <span data-ttu-id="27c54-105">Você deve verificar o *status do progresso* antes de usar o número retornado, pois o contador pode não ser válido quando for lido.</span><span class="sxs-lookup"><span data-stu-id="27c54-105">You should check *CounterStatus* before using the returned number, because the counter may not be valid when it is read.</span></span> <span data-ttu-id="27c54-106">Para verificar o status do contador, chame a função [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="27c54-106">To check the counter status, call the [**PdhVbIsGoodStatus**](pdhvbisgoodstatus.md) function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="27c54-107">A função que este tópico descreve pode ser alterada ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="27c54-107">The function that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="27c54-108">Em vez disso, a Microsoft recomenda que você use as funções descritas em [funções de contadores de desempenho](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="27c54-108">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="27c54-109">Função PdhVbGetDoubleCounterValue ( \_ ByVal enhandle, como Long, \_ ByVal status por Long \_ ) como Double</span><span class="sxs-lookup"><span data-stu-id="27c54-109">Function PdhVbGetDoubleCounterValue( \_ ByVal CounterHandle As Long, \_ ByVal CounterStatus As Long \_ ) As Double</span></span>

## <a name="parameters"></a><span data-ttu-id="27c54-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27c54-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27c54-111">*Manipulador*</span><span class="sxs-lookup"><span data-stu-id="27c54-111">*CounterHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="27c54-112">ID do contador cujo valor atual deve ser lido.</span><span class="sxs-lookup"><span data-stu-id="27c54-112">ID of the counter whose current value is to be read.</span></span>

</dd> <dt>

<span data-ttu-id="27c54-113">*Status do progresso*</span><span class="sxs-lookup"><span data-stu-id="27c54-113">*CounterStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="27c54-114">Variável na qual o status atual do valor do contador é retornado para o chamador.</span><span class="sxs-lookup"><span data-stu-id="27c54-114">Variable in which the current status of the counter value is returned to the caller.</span></span> <span data-ttu-id="27c54-115">O valor de dados retornados será válido se e somente se o valor retornado em mystatus for \_ PDH \_ CSTATUS \_ dados válidos ou PDH \_ CSTATUS \_ novos \_ dados (consulte códigos de erro da PDH).</span><span class="sxs-lookup"><span data-stu-id="27c54-115">The returned data value is valid if and only if the value returned in CounterStatus is PDH\_CSTATUS\_VALID\_DATA or PDH\_CSTATUS\_NEW\_DATA (see PDH error codes).</span></span> <span data-ttu-id="27c54-116">Se o valor retornado em mystatus for qualquer outro valor, não use os dados.</span><span class="sxs-lookup"><span data-stu-id="27c54-116">If the value returned in CounterStatus is any other value, do not use the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27c54-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27c54-117">Return value</span></span>

<span data-ttu-id="27c54-118">A função retorna o valor de ponto flutuante de precisão dupla do contador atual, computado e formatado, conforme definido pelo tipo de contador.</span><span class="sxs-lookup"><span data-stu-id="27c54-118">The function returns the double-precision floating point value of the current counter, computed and formatted as defined by the counter type.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c54-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c54-119">Requirements</span></span>



| <span data-ttu-id="27c54-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c54-120">Requirement</span></span> | <span data-ttu-id="27c54-121">Valor</span><span class="sxs-lookup"><span data-stu-id="27c54-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27c54-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27c54-122">Minimum supported client</span></span><br/> | <span data-ttu-id="27c54-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="27c54-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27c54-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27c54-124">Minimum supported server</span></span><br/> | <span data-ttu-id="27c54-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27c54-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27c54-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="27c54-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="27c54-127"><dt>PDH. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27c54-127"><dt>Pdh.lib</dt></span></span> </dl> |
| <span data-ttu-id="27c54-128">DLL</span><span class="sxs-lookup"><span data-stu-id="27c54-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27c54-129"><dt>Pdh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27c54-129"><dt>Pdh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27c54-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="27c54-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c54-131">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="27c54-131">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
</dt> </dl>

 

 




