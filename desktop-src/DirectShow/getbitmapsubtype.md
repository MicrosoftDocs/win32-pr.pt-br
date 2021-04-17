---
description: A função GetBitmapSubtype retorna o GUID do subtipo de mídia para o bitmap especificado.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Função GetBitmapSubtype (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759297"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="92e8b-103">Função GetBitmapSubtype</span><span class="sxs-lookup"><span data-stu-id="92e8b-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="92e8b-104">A `GetBitmapSubtype` função retorna o **GUID** do subtipo de mídia para o bitmap especificado.</span><span class="sxs-lookup"><span data-stu-id="92e8b-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e8b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92e8b-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="92e8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92e8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e8b-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="92e8b-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="92e8b-108">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="92e8b-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e8b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92e8b-109">Return value</span></span>

<span data-ttu-id="92e8b-110">Retorna o **GUID** do subtipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="92e8b-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="92e8b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="92e8b-111">Remarks</span></span>

<span data-ttu-id="92e8b-112">Para tipos RGB não compactados, essa função mapeia o campo **biBitCount** para o subtipo.</span><span class="sxs-lookup"><span data-stu-id="92e8b-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="92e8b-113">Para tipos de vídeo compactados, essa função usa a classe [**FOURCCMap**](fourccmap.md) para mapear o campo de **bicompactação** para o subtipo.</span><span class="sxs-lookup"><span data-stu-id="92e8b-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="92e8b-114">Se a função não puder corresponder ao formato de um subtipo, o valor de retorno será o GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="92e8b-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e8b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92e8b-115">Requirements</span></span>



| <span data-ttu-id="92e8b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="92e8b-116">Requirement</span></span> | <span data-ttu-id="92e8b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="92e8b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92e8b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92e8b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="92e8b-119"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92e8b-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="92e8b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92e8b-120">Library</span></span><br/> | <dl> <span data-ttu-id="92e8b-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="92e8b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e8b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="92e8b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e8b-123">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="92e8b-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




