---
description: A função GetSubtypeName recupera o nome legível por humanos de um subtipo de vídeo.
ms.assetid: 493b434e-2d36-4897-a5b2-7be0eb0a560f
title: Função GetSubtypeName (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSubtypeName
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f5cae835a3a7f1b5510d85ecf3f2ae9d15251a45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750276"
---
# <a name="getsubtypename-function"></a><span data-ttu-id="1f552-103">Função GetSubtypeName</span><span class="sxs-lookup"><span data-stu-id="1f552-103">GetSubtypeName function</span></span>

<span data-ttu-id="1f552-104">A `GetSubtypeName` função recupera o nome legível por humanos de um subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1f552-104">The `GetSubtypeName` function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f552-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f552-105">Syntax</span></span>


```C++
TCHAR* GetSubtypeName(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="1f552-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f552-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f552-107">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="1f552-107">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="1f552-108">Ponteiro para um **GUID** de subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1f552-108">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f552-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f552-109">Return value</span></span>

<span data-ttu-id="1f552-110">Retorna uma cadeia de caracteres que contém o nome.</span><span class="sxs-lookup"><span data-stu-id="1f552-110">Returns a string containing the name.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f552-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f552-111">Requirements</span></span>



| <span data-ttu-id="1f552-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f552-112">Requirement</span></span> | <span data-ttu-id="1f552-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1f552-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f552-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f552-114">Header</span></span><br/>  | <dl> <span data-ttu-id="1f552-115"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f552-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1f552-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f552-116">Library</span></span><br/> | <dl> <span data-ttu-id="1f552-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1f552-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f552-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f552-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f552-119">Funções de vídeo e imagem</span><span class="sxs-lookup"><span data-stu-id="1f552-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




