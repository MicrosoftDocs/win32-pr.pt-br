---
description: Recupera o identificador de classe deste filtro.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Método CPersistStream. GetClassID (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757691"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="601cc-103">Método CPersistStream. GetClassID</span><span class="sxs-lookup"><span data-stu-id="601cc-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="601cc-104">Recupera o identificador de classe deste filtro.</span><span class="sxs-lookup"><span data-stu-id="601cc-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="601cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="601cc-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="601cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="601cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601cc-107">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="601cc-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="601cc-108">Ponteiro para uma estrutura CLSID.</span><span class="sxs-lookup"><span data-stu-id="601cc-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="601cc-109">Copie sua ID de classe para aqui.</span><span class="sxs-lookup"><span data-stu-id="601cc-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601cc-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="601cc-110">Return value</span></span>

<span data-ttu-id="601cc-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="601cc-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="601cc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="601cc-112">Requirements</span></span>



| <span data-ttu-id="601cc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="601cc-113">Requirement</span></span> | <span data-ttu-id="601cc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="601cc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="601cc-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="601cc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="601cc-116"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="601cc-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="601cc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="601cc-117">Library</span></span><br/> | <dl> <span data-ttu-id="601cc-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="601cc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601cc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="601cc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601cc-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="601cc-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




