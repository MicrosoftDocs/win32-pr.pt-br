---
description: O método SetDIBData especifica informações sobre o bitmap independente de dispositivo (DIB) GDI que esse objeto está gerenciando. Chame esse método para inicializar o objeto CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Método CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756598"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="6a159-104">Método CImageSample. SetDIBData</span><span class="sxs-lookup"><span data-stu-id="6a159-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="6a159-105">O `SetDIBData` método especifica informações sobre o DIB (bitmap independente de dispositivo) GDI que esse objeto está gerenciando.</span><span class="sxs-lookup"><span data-stu-id="6a159-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="6a159-106">Chame esse método para inicializar o objeto **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="6a159-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a159-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6a159-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="6a159-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a159-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a159-109">*pDibData*</span><span class="sxs-lookup"><span data-stu-id="6a159-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="6a159-110">Ponteiro para uma estrutura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6a159-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a159-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a159-111">Return value</span></span>

<span data-ttu-id="6a159-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6a159-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a159-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a159-113">Requirements</span></span>



| <span data-ttu-id="6a159-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a159-114">Requirement</span></span> | <span data-ttu-id="6a159-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6a159-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a159-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a159-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6a159-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6a159-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6a159-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6a159-118">Library</span></span><br/> | <dl> <span data-ttu-id="6a159-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6a159-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a159-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a159-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a159-121">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="6a159-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




