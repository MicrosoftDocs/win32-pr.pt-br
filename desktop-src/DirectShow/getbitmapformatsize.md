---
description: A função GetBitmapFormatSize calcula o tamanho necessário para uma estrutura VIDEOINFO que pode conter uma estrutura BITMAPINFOHEADER especificada.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Função GetBitmapFormatSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750026"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="3bca8-103">Função GetBitmapFormatSize</span><span class="sxs-lookup"><span data-stu-id="3bca8-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="3bca8-104">A `GetBitmapFormatSize` função calcula o tamanho necessário para uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que pode conter uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.</span><span class="sxs-lookup"><span data-stu-id="3bca8-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bca8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bca8-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="3bca8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bca8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bca8-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="3bca8-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="3bca8-108">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="3bca8-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bca8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bca8-109">Return value</span></span>

<span data-ttu-id="3bca8-110">Retorna o tamanho, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3bca8-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bca8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bca8-111">Remarks</span></span>

<span data-ttu-id="3bca8-112">Uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) pode ser seguida por máscaras de cor ou entradas de paleta, portanto, pode ser difícil determinar o número de bytes necessários para construir uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) de uma estrutura **BITMAPINFOHEADER** existente.</span><span class="sxs-lookup"><span data-stu-id="3bca8-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="3bca8-113">Para copiar uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) em uma estrutura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , use a macro [**header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) , que calcula o deslocamento correto.</span><span class="sxs-lookup"><span data-stu-id="3bca8-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="3bca8-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3bca8-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="3bca8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bca8-115">Requirements</span></span>



| <span data-ttu-id="3bca8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bca8-116">Requirement</span></span> | <span data-ttu-id="3bca8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3bca8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bca8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bca8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3bca8-119"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3bca8-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3bca8-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bca8-120">Library</span></span><br/> | <dl> <span data-ttu-id="3bca8-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3bca8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bca8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bca8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bca8-123">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="3bca8-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




