---
description: A função GetTrueColorType recupera o nome legível por humanos de um subtipo de vídeo.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Função GetTrueColorType (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751875"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="058db-103">Função GetTrueColorType</span><span class="sxs-lookup"><span data-stu-id="058db-103">GetTrueColorType function</span></span>

<span data-ttu-id="058db-104">A função **GetTrueColorType** recupera o nome legível por humanos de um subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="058db-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="058db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="058db-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="058db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="058db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="058db-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="058db-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="058db-108">Ponteiro para uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define o bitmap.</span><span class="sxs-lookup"><span data-stu-id="058db-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="058db-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="058db-109">Return value</span></span>

<span data-ttu-id="058db-110">Retorna MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565.</span><span class="sxs-lookup"><span data-stu-id="058db-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="058db-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="058db-111">Requirements</span></span>



| <span data-ttu-id="058db-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="058db-112">Requirement</span></span> | <span data-ttu-id="058db-113">Valor</span><span class="sxs-lookup"><span data-stu-id="058db-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="058db-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="058db-114">Header</span></span><br/>  | <dl> <span data-ttu-id="058db-115"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="058db-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="058db-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="058db-116">Library</span></span><br/> | <dl> <span data-ttu-id="058db-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="058db-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="058db-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="058db-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="058db-119">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="058db-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




