---
description: A função GetBitmapSize calcula o número de bytes exigidos por um bitmap independente de dispositivo (DIB). Essa função simplesmente chama a macro DIBSize.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Função GetBitmapSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752478"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="dbc63-104">Função GetBitmapSize</span><span class="sxs-lookup"><span data-stu-id="dbc63-104">GetBitmapSize function</span></span>

<span data-ttu-id="dbc63-105">A `GetBitmapSize` função calcula o número de bytes exigidos por um bitmap independente de dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="dbc63-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="dbc63-106">Essa função simplesmente chama a macro [**dibsize**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .</span><span class="sxs-lookup"><span data-stu-id="dbc63-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc63-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbc63-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="dbc63-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbc63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc63-109">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="dbc63-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="dbc63-110">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="dbc63-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc63-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbc63-111">Return value</span></span>

<span data-ttu-id="dbc63-112">Retorna o tamanho em bytes.</span><span class="sxs-lookup"><span data-stu-id="dbc63-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc63-113">Requirements</span></span>



| <span data-ttu-id="dbc63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc63-114">Requirement</span></span> | <span data-ttu-id="dbc63-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc63-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc63-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbc63-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dbc63-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc63-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="dbc63-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbc63-118">Library</span></span><br/> | <dl> <span data-ttu-id="dbc63-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc63-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc63-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc63-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc63-121">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="dbc63-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




