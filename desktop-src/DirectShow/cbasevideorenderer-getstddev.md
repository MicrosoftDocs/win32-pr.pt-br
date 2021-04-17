---
description: O método GetStdDev estima o desvio padrão em milissegundos entre quando cada quadro é devido e quando é realmente renderizado para estatísticas por quadro.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Método CBaseVideoRenderer. GetStdDev (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755603"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="47438-103">Método CBaseVideoRenderer. GetStdDev</span><span class="sxs-lookup"><span data-stu-id="47438-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="47438-104">O `GetStdDev` método estima o desvio padrão em milissegundos entre quando cada quadro é devido e quando é realmente renderizado para estatísticas por quadro.</span><span class="sxs-lookup"><span data-stu-id="47438-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="47438-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47438-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="47438-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47438-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47438-107">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="47438-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="47438-108">Valor inteiro que contém o número de amostras de vídeo recebidas pelo processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="47438-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="47438-109">*piResult*</span><span class="sxs-lookup"><span data-stu-id="47438-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="47438-110">Ponteiro para um valor inteiro que conterá o desvio padrão.</span><span class="sxs-lookup"><span data-stu-id="47438-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="47438-111">*llSumSq*</span><span class="sxs-lookup"><span data-stu-id="47438-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="47438-112">Valor que representa o desvio padrão, em milissegundos, de todos os exemplos de vídeo renderizados.</span><span class="sxs-lookup"><span data-stu-id="47438-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="47438-113">Quanto menor o valor, mais consistente é a renderização.</span><span class="sxs-lookup"><span data-stu-id="47438-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="47438-114">*iTot*</span><span class="sxs-lookup"><span data-stu-id="47438-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="47438-115">Valor que representa o valor médio, em milissegundos, entre a hora carimbada e o tempo processado para todos os exemplos de vídeo renderizados.</span><span class="sxs-lookup"><span data-stu-id="47438-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47438-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47438-116">Return value</span></span>

<span data-ttu-id="47438-117">Retorna NOERROR.</span><span class="sxs-lookup"><span data-stu-id="47438-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="47438-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47438-118">Requirements</span></span>



| <span data-ttu-id="47438-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="47438-119">Requirement</span></span> | <span data-ttu-id="47438-120">Valor</span><span class="sxs-lookup"><span data-stu-id="47438-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47438-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47438-121">Header</span></span><br/>  | <dl> <span data-ttu-id="47438-122"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47438-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47438-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47438-123">Library</span></span><br/> | <dl> <span data-ttu-id="47438-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="47438-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47438-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="47438-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47438-126">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="47438-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




