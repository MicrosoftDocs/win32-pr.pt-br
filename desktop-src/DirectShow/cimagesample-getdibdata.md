---
description: O método GetDIBData recupera informações sobre o DIB (bitmap independente de dispositivo) do GDI que esse objeto está gerenciando.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Método CImageSample. GetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786989"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="f5d5e-103">Método CImageSample. GetDIBData</span><span class="sxs-lookup"><span data-stu-id="f5d5e-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="f5d5e-104">O `GetDIBData` método recupera informações sobre o DIB (bitmap independente de dispositivo) do GDI que esse objeto está gerenciando.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d5e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5d5e-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="f5d5e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5d5e-106">Parameters</span></span>

<span data-ttu-id="f5d5e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5d5e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5d5e-108">Return value</span></span>

<span data-ttu-id="f5d5e-109">Retorna um ponteiro para uma estrutura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f5d5e-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5d5e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5d5e-110">Remarks</span></span>

<span data-ttu-id="f5d5e-111">O chamador deve inicializar a estrutura **DIBDATA** antes de chamar esse método; Verifique o valor de **CImageSample:: m \_ bInit**.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="f5d5e-112">Para inicializar a estrutura, chame o método [**CImageSample:: SetDIBData**](cimagesample-setdibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="f5d5e-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d5e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5d5e-113">Requirements</span></span>



| <span data-ttu-id="f5d5e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5d5e-114">Requirement</span></span> | <span data-ttu-id="f5d5e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f5d5e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d5e-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5d5e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f5d5e-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5e-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5d5e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f5d5e-118">Library</span></span><br/> | <dl> <span data-ttu-id="f5d5e-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f5d5e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5d5e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5d5e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5d5e-121">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="f5d5e-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




