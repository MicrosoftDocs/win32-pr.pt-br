---
description: O método CheckVideoType verifica se um formato VIDEOINFO especificado é compatível com o formato de exibição.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Método CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749014"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="e6071-103">Método CImageDisplay. CheckVideoType</span><span class="sxs-lookup"><span data-stu-id="e6071-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="e6071-104">O `CheckVideoType` método verifica se um formato [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) especificado é compatível com o formato de exibição.</span><span class="sxs-lookup"><span data-stu-id="e6071-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6071-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6071-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="e6071-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6071-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6071-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="e6071-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="e6071-108">Ponteiro para uma estrutura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="e6071-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6071-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6071-109">Return value</span></span>

<span data-ttu-id="e6071-110">Retorna S \_ OK se o formato for compatível ou E \_ INVALIDARG de outra forma.</span><span class="sxs-lookup"><span data-stu-id="e6071-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6071-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6071-111">Remarks</span></span>

<span data-ttu-id="e6071-112">Esse método retornará S \_ OK se o tipo proposto puder ser exibido facilmente nas configurações de exibição atuais.</span><span class="sxs-lookup"><span data-stu-id="e6071-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6071-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6071-113">Requirements</span></span>



| <span data-ttu-id="e6071-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6071-114">Requirement</span></span> | <span data-ttu-id="e6071-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e6071-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6071-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6071-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e6071-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6071-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6071-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6071-118">Library</span></span><br/> | <dl> <span data-ttu-id="e6071-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e6071-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6071-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6071-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6071-121">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="e6071-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




