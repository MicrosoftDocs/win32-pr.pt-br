---
description: 'Método CPosPassThru. GetCapabilities – o método GetCapabilities recupera todos os recursos de busca do fluxo. Esse método implementa o método IMediaSeeking:: GetCapabilities.'
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
ms.openlocfilehash: c21838d3df72d52255d0a2e35dd0b7d34ef55411
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085564"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="418f1-104">Método CPosPassThru. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="418f1-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="418f1-105">O método **GetCapabilities** recupera todos os recursos de busca do fluxo.</span><span class="sxs-lookup"><span data-stu-id="418f1-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="418f1-106">Esse método implementa o método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="418f1-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="418f1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="418f1-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="418f1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="418f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="418f1-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="418f1-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="418f1-110">O ponteiro para uma variável que recebe uma combinação de bits bit a procurar sinalizadores de [**\_ \_ \_ recursos de busca**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="418f1-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="418f1-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="418f1-111">Return value</span></span>

<span data-ttu-id="418f1-112">Retorna o valor **HRESULT** do PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="418f1-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="418f1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="418f1-113">Requirements</span></span>



| <span data-ttu-id="418f1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="418f1-114">Requirement</span></span> | <span data-ttu-id="418f1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="418f1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="418f1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="418f1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="418f1-117"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="418f1-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="418f1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="418f1-118">Library</span></span><br/> | <dl> <span data-ttu-id="418f1-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="418f1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="418f1-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="418f1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="418f1-121">**Classe CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="418f1-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




