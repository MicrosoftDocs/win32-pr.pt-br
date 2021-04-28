---
description: 'Método CPosPassThru. IsFormatSupported – o método IsFormatSupported determina se há suporte para um formato de hora especificado. Esse método implementa o método IMediaSeeking:: IsFormatSupported.'
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
ms.openlocfilehash: 6bd4b90bbe86e7ba05aa48fb7888c946babd8ed9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095244"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="2be88-104">Método CPosPassThru. IsFormatSupported</span><span class="sxs-lookup"><span data-stu-id="2be88-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="2be88-105">O `IsFormatSupported` método determina se há suporte para um formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="2be88-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="2be88-106">Esse método implementa o método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="2be88-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2be88-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2be88-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="2be88-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2be88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2be88-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="2be88-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="2be88-110">Ponteiro para um GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="2be88-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2be88-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2be88-111">Return value</span></span>

<span data-ttu-id="2be88-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="2be88-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2be88-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2be88-113">Requirements</span></span>



| <span data-ttu-id="2be88-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2be88-114">Requirement</span></span> | <span data-ttu-id="2be88-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2be88-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2be88-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2be88-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2be88-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2be88-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2be88-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2be88-118">Library</span></span><br/> | <dl> <span data-ttu-id="2be88-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2be88-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2be88-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2be88-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2be88-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="2be88-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="2be88-122">**GUIDs de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="2be88-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




