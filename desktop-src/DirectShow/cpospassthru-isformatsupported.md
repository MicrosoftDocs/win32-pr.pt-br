---
description: 'O método IsFormatSupported determina se há suporte para um formato de hora especificado. Esse método implementa o método IMediaSeeking:: IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Método CPosPassThru. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758536"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="7be68-104">Método CPosPassThru. IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="7be68-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="7be68-105">O `IsFormatSupported` método determina se há suporte para um formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="7be68-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="7be68-106">Esse método implementa o método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="7be68-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be68-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7be68-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="7be68-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7be68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7be68-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="7be68-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="7be68-110">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="7be68-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7be68-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7be68-111">Return value</span></span>

<span data-ttu-id="7be68-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="7be68-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="7be68-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7be68-113">Requirements</span></span>



| <span data-ttu-id="7be68-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be68-114">Requirement</span></span> | <span data-ttu-id="7be68-115">Valor</span><span class="sxs-lookup"><span data-stu-id="7be68-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be68-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7be68-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7be68-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7be68-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7be68-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7be68-118">Library</span></span><br/> | <dl> <span data-ttu-id="7be68-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7be68-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7be68-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7be68-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be68-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="7be68-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="7be68-122">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="7be68-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




