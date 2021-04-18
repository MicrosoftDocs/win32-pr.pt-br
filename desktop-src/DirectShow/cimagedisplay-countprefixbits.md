---
description: O método CountPrefixBits calcula o número de zero bits no início de um campo de bits especificado.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Método CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751687"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="8aea8-103">Método CImageDisplay. CountPrefixBits</span><span class="sxs-lookup"><span data-stu-id="8aea8-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="8aea8-104">O `CountPrefixBits` método calcula o número de zero bits no início de um campo de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="8aea8-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aea8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8aea8-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="8aea8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8aea8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aea8-107">*Campo*</span><span class="sxs-lookup"><span data-stu-id="8aea8-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="8aea8-108">Especifica um campo de bits como um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8aea8-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aea8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8aea8-109">Return value</span></span>

<span data-ttu-id="8aea8-110">Retorna o número de zero bits que ocorrem antes do primeiro 1 bit ou 0x80000000 se todos os bits forem zero.</span><span class="sxs-lookup"><span data-stu-id="8aea8-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aea8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8aea8-111">Remarks</span></span>

<span data-ttu-id="8aea8-112">Esse método é útil para trabalhar com máscaras de cores em estruturas [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="8aea8-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aea8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aea8-113">Requirements</span></span>



| <span data-ttu-id="8aea8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aea8-114">Requirement</span></span> | <span data-ttu-id="8aea8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8aea8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aea8-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8aea8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8aea8-117"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8aea8-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8aea8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8aea8-118">Library</span></span><br/> | <dl> <span data-ttu-id="8aea8-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8aea8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aea8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8aea8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aea8-121">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="8aea8-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




