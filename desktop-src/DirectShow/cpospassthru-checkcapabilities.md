---
description: 'O método CheckCapabilities consulta se um fluxo especificou recursos de busca. Esse método implementa o método IMediaSeeking:: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Método CPosPassThru. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758690"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="caeeb-104">Método CPosPassThru. CheckCapabilities</span><span class="sxs-lookup"><span data-stu-id="caeeb-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="caeeb-105">O `CheckCapabilities` método consulta se um fluxo especificou recursos de busca.</span><span class="sxs-lookup"><span data-stu-id="caeeb-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="caeeb-106">Esse método implementa o método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="caeeb-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="caeeb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="caeeb-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="caeeb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="caeeb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="caeeb-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="caeeb-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="caeeb-110">Ponteiro para uma combinação de bits de um ou mais atributos de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) em busca.</span><span class="sxs-lookup"><span data-stu-id="caeeb-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="caeeb-111">Quando o método retorna, o valor indica quais desses atributos estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="caeeb-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="caeeb-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="caeeb-112">Return value</span></span>

<span data-ttu-id="caeeb-113">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="caeeb-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="caeeb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="caeeb-114">Requirements</span></span>



| <span data-ttu-id="caeeb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="caeeb-115">Requirement</span></span> | <span data-ttu-id="caeeb-116">Valor</span><span class="sxs-lookup"><span data-stu-id="caeeb-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="caeeb-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="caeeb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="caeeb-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="caeeb-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="caeeb-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="caeeb-119">Library</span></span><br/> | <dl> <span data-ttu-id="caeeb-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="caeeb-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="caeeb-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="caeeb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caeeb-122">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="caeeb-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




