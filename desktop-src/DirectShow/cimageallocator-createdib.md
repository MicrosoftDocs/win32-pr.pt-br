---
description: O método CreateDIB cria um bitmap independente de dispositivo (DIB) GDI. A DIB é alocada em um bloco mempory compartilhado, que elimina uma operação de cópia quando o filtro proprietário blits a imagem.
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: Método CImageAllocator. CreateDIB (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 316b7aeadfa442a8df4e80075380464758f3c6bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785367"
---
# <a name="cimageallocatorcreatedib-method"></a><span data-ttu-id="1fad0-104">Método CImageAllocator. CreateDIB</span><span class="sxs-lookup"><span data-stu-id="1fad0-104">CImageAllocator.CreateDIB method</span></span>

<span data-ttu-id="1fad0-105">O `CreateDIB` método cria um DIB (bitmap independente de dispositivo) GDI.</span><span class="sxs-lookup"><span data-stu-id="1fad0-105">The `CreateDIB` method creates a GDI device-independent bitmap (DIB).</span></span> <span data-ttu-id="1fad0-106">A DIB é alocada em um bloco mempory compartilhado, que elimina uma operação de cópia quando o filtro proprietário blits a imagem.</span><span class="sxs-lookup"><span data-stu-id="1fad0-106">The DIB is allocated in a shared mempory block, which eliminates a copy operation when the owning filter blits the image.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fad0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fad0-107">Syntax</span></span>


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a><span data-ttu-id="1fad0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fad0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fad0-109">*Insize*</span><span class="sxs-lookup"><span data-stu-id="1fad0-109">*InSize*</span></span> 
</dt> <dd>

<span data-ttu-id="1fad0-110">Tamanho do bitmap.</span><span class="sxs-lookup"><span data-stu-id="1fad0-110">Size of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="1fad0-111">*DibData* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="1fad0-111">*DibData* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="1fad0-112">Referência a uma estrutura [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="1fad0-112">Reference to a [**DIBDATA**](dibdata.md) structure.</span></span> <span data-ttu-id="1fad0-113">O método preenche essa estrutura com informações sobre o DIB.</span><span class="sxs-lookup"><span data-stu-id="1fad0-113">The method fills in this structure with information about the DIB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fad0-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fad0-114">Return value</span></span>

<span data-ttu-id="1fad0-115">Retorna S \_ OK se for bem-sucedido ou um código de erro do contrário.</span><span class="sxs-lookup"><span data-stu-id="1fad0-115">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fad0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fad0-116">Requirements</span></span>



| <span data-ttu-id="1fad0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fad0-117">Requirement</span></span> | <span data-ttu-id="1fad0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1fad0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fad0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fad0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1fad0-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fad0-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fad0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fad0-121">Library</span></span><br/> | <dl> <span data-ttu-id="1fad0-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1fad0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fad0-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fad0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fad0-124">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="1fad0-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> <dt>

[<span data-ttu-id="1fad0-125">**CImageAllocator:: Alloc**</span><span class="sxs-lookup"><span data-stu-id="1fad0-125">**CImageAllocator::Alloc**</span></span>](cimageallocator-alloc.md)
</dt> </dl>

 

 




