---
description: Altera o sinalizador sujo para o fluxo atual.
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: Método CPersistStream. SetDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759306"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="56209-103">Método CPersistStream. SetDirty</span><span class="sxs-lookup"><span data-stu-id="56209-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="56209-104">Altera o sinalizador sujo para o fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="56209-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="56209-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56209-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="56209-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56209-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56209-107">*fDirty*</span><span class="sxs-lookup"><span data-stu-id="56209-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="56209-108">Novo sinalizador sujo para este fluxo.</span><span class="sxs-lookup"><span data-stu-id="56209-108">New dirty flag for this stream.</span></span> <span data-ttu-id="56209-109">**Verdadeiro** significa que os dados não foram salvos.</span><span class="sxs-lookup"><span data-stu-id="56209-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56209-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56209-110">Return value</span></span>

<span data-ttu-id="56209-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56209-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56209-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56209-112">Requirements</span></span>



| <span data-ttu-id="56209-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="56209-113">Requirement</span></span> | <span data-ttu-id="56209-114">Valor</span><span class="sxs-lookup"><span data-stu-id="56209-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56209-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56209-115">Header</span></span><br/>  | <dl> <span data-ttu-id="56209-116"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56209-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56209-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56209-117">Library</span></span><br/> | <dl> <span data-ttu-id="56209-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="56209-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56209-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="56209-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56209-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="56209-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




