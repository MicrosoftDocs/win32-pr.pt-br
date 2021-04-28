---
description: Construtor de CImageSample. CImageSample-método de construtor.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Construtor CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095604"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="a55ea-103">Construtor CImageSample. CImageSample</span><span class="sxs-lookup"><span data-stu-id="a55ea-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="a55ea-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a55ea-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a55ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a55ea-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="a55ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a55ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a55ea-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="a55ea-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="a55ea-108">Ponteiro para o alocador que criou este exemplo.</span><span class="sxs-lookup"><span data-stu-id="a55ea-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="a55ea-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="a55ea-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a55ea-110">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="a55ea-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a55ea-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="a55ea-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a55ea-112">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="a55ea-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a55ea-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="a55ea-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="a55ea-114">Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *.*</span><span class="sxs-lookup"><span data-stu-id="a55ea-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="a55ea-115">O buffer deve conter um bitmap independente de dispositivo (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="a55ea-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="a55ea-116">*length*</span><span class="sxs-lookup"><span data-stu-id="a55ea-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="a55ea-117">Comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="a55ea-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a55ea-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a55ea-118">Remarks</span></span>

<span data-ttu-id="a55ea-119">A classe [**CImageAllocator**](cimageallocator.md) cria um DIB usando um objeto de mapeamento de arquivo que é apoiado pelo arquivo de paginação do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a55ea-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="a55ea-120">O identificador para o objeto de mapeamento de arquivo é armazenado no membro **hMapping** da estrutura **m \_ DibData** .</span><span class="sxs-lookup"><span data-stu-id="a55ea-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a55ea-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a55ea-121">Requirements</span></span>



| <span data-ttu-id="a55ea-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a55ea-122">Requirement</span></span> | <span data-ttu-id="a55ea-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a55ea-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a55ea-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a55ea-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a55ea-125"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a55ea-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a55ea-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a55ea-126">Library</span></span><br/> | <dl> <span data-ttu-id="a55ea-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a55ea-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a55ea-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a55ea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a55ea-129">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="a55ea-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




