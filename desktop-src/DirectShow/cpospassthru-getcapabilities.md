---
description: 'O método GetCapabilities recupera todos os recursos de busca do fluxo. Esse método implementa o método IMediaSeeking:: GetCapabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Método CPosPassThru. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751242"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="1d89e-104">Método CPosPassThru. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="1d89e-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="1d89e-105">O método **GetCapabilities** recupera todos os recursos de busca do fluxo.</span><span class="sxs-lookup"><span data-stu-id="1d89e-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="1d89e-106">Esse método implementa o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="1d89e-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d89e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d89e-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="1d89e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d89e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d89e-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="1d89e-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="1d89e-110">O ponteiro para uma variável que recebe uma combinação de bits bit a procurar sinalizadores de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="1d89e-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d89e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d89e-111">Return value</span></span>

<span data-ttu-id="1d89e-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="1d89e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d89e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d89e-113">Requirements</span></span>



| <span data-ttu-id="1d89e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d89e-114">Requirement</span></span> | <span data-ttu-id="1d89e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1d89e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d89e-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d89e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1d89e-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d89e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d89e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d89e-118">Library</span></span><br/> | <dl> <span data-ttu-id="1d89e-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d89e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d89e-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d89e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d89e-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="1d89e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




