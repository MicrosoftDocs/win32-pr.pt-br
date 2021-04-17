---
description: Número de threads de streaming usando este pin.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: 'Membro CDynamicOutputPin:: m_dwNumOutstandingOutputPinUsers (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2ba214a2c1c6d3d056147db54c936cb61b73dcfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787409"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a><span data-ttu-id="5d0f6-103">Membro de CDynamicOutputPin:: m \_ dwNumOutstandingOutputPinUsers</span><span class="sxs-lookup"><span data-stu-id="5d0f6-103">CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers member</span></span>

<span data-ttu-id="5d0f6-104">Número de threads de streaming usando este pin.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-104">Number of streaming threads using this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5d0f6-105">Syntax</span></span>


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a><span data-ttu-id="5d0f6-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d0f6-106">Remarks</span></span>

<span data-ttu-id="5d0f6-107">O método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa essa variável e o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) a decrementa.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-107">The [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method increments this variable, and the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method decrements it.</span></span> <span data-ttu-id="5d0f6-108">Quando o valor for maior que zero, algum thread usará esse PIN para transmitir dados ou para alterar o tipo de conexão.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-108">When the value is greater than zero, some thread is using this pin to stream data or to change the connection type.</span></span> <span data-ttu-id="5d0f6-109">O PIN não pode ser bloqueado enquanto este for o caso.</span><span class="sxs-lookup"><span data-stu-id="5d0f6-109">The pin cannot be blocked while this is the case.</span></span>

<span data-ttu-id="5d0f6-110">Antes de acessar essa variável, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="5d0f6-110">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d0f6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d0f6-111">Requirements</span></span>



| <span data-ttu-id="5d0f6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d0f6-112">Requirement</span></span> | <span data-ttu-id="5d0f6-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5d0f6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0f6-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d0f6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="5d0f6-115"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f6-115"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5d0f6-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5d0f6-116">Library</span></span><br/> | <dl> <span data-ttu-id="5d0f6-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d0f6-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d0f6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d0f6-119">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5d0f6-119">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> <dt>

[<span data-ttu-id="5d0f6-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5d0f6-120">**CDynamicOutputPin::StreamingThreadUsingOutputPin**</span></span>](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




