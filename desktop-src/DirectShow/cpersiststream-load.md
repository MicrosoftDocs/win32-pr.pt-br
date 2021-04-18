---
description: Carrega os dados do filtro de um determinado fluxo.
ms.assetid: c2bfd379-2916-4698-bc41-653161723706
title: Método CPersistStream. Load (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Load
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 83b16c3fe7bf905d1ade6b7f38cf27c61b44e4d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756590"
---
# <a name="cpersiststreamload-method"></a><span data-ttu-id="9283c-103">Método CPersistStream. Load</span><span class="sxs-lookup"><span data-stu-id="9283c-103">CPersistStream.Load method</span></span>

<span data-ttu-id="9283c-104">Carrega os dados do filtro de um determinado fluxo.</span><span class="sxs-lookup"><span data-stu-id="9283c-104">Loads the filter's data from a given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9283c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9283c-105">Syntax</span></span>


```C++
HRESULT Load(
   LPSTREAM pStm
);
```



## <a name="parameters"></a><span data-ttu-id="9283c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9283c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9283c-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="9283c-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="9283c-108">Ponteiro para o fluxo do qual será carregado.</span><span class="sxs-lookup"><span data-stu-id="9283c-108">Pointer to the stream from which to be loaded.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9283c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9283c-109">Return value</span></span>

<span data-ttu-id="9283c-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9283c-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9283c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9283c-111">Remarks</span></span>

<span data-ttu-id="9283c-112">Essa função de membro implementa o método **IPersistStream:: Load** .</span><span class="sxs-lookup"><span data-stu-id="9283c-112">This member function implements the **IPersistStream::Load** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9283c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9283c-113">Requirements</span></span>



| <span data-ttu-id="9283c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9283c-114">Requirement</span></span> | <span data-ttu-id="9283c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9283c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9283c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9283c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9283c-117"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9283c-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9283c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9283c-118">Library</span></span><br/> | <dl> <span data-ttu-id="9283c-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9283c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9283c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9283c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9283c-121">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="9283c-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




