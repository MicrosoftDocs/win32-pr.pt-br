---
description: 'O método GetPreroll recupera a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o método IMediaSeeking:: GetPreroll.'
ms.assetid: b00de2fa-ba3c-4a16-ad67-adf3df52ef9a
title: Método CPosPassThru. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e72d7c83c8cdb0fa08a4b395fd65c80edbe3fb05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759305"
---
# <a name="cpospassthrugetpreroll-method"></a><span data-ttu-id="30656-104">Método CPosPassThru. GetPreroll</span><span class="sxs-lookup"><span data-stu-id="30656-104">CPosPassThru.GetPreroll method</span></span>

<span data-ttu-id="30656-105">O `GetPreroll` método recupera a quantidade de dados que serão enfileirados antes da posição inicial.</span><span class="sxs-lookup"><span data-stu-id="30656-105">The `GetPreroll` method retrieves the amount of data that will be queued before the start position.</span></span> <span data-ttu-id="30656-106">Esse método implementa o método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="30656-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30656-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30656-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pllPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="30656-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30656-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30656-109">*pllPreroll*</span><span class="sxs-lookup"><span data-stu-id="30656-109">*pllPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="30656-110">Ponteiro para uma variável que recebe a hora de preversão, em unidades do formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="30656-110">Pointer to a variable that receives the preroll time, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30656-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30656-111">Return value</span></span>

<span data-ttu-id="30656-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="30656-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="30656-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30656-113">Requirements</span></span>



| <span data-ttu-id="30656-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="30656-114">Requirement</span></span> | <span data-ttu-id="30656-115">Valor</span><span class="sxs-lookup"><span data-stu-id="30656-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30656-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30656-116">Header</span></span><br/>  | <dl> <span data-ttu-id="30656-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30656-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30656-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30656-118">Library</span></span><br/> | <dl> <span data-ttu-id="30656-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="30656-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30656-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="30656-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30656-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="30656-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




