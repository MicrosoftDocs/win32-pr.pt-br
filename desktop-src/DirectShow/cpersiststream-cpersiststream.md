---
description: Método de construtor.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Construtor CPersistStream. CPersistStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757308"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="936cc-103">Construtor CPersistStream. CPersistStream</span><span class="sxs-lookup"><span data-stu-id="936cc-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="936cc-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="936cc-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="936cc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="936cc-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="936cc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="936cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="936cc-107">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="936cc-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="936cc-108">Ponteiro para a interface **IUnknown** do objeto de delegação.</span><span class="sxs-lookup"><span data-stu-id="936cc-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="936cc-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="936cc-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="936cc-110">Ponteiro para o valor de retorno de COM geral.</span><span class="sxs-lookup"><span data-stu-id="936cc-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="936cc-111">Esse valor só será alterado se essa função falhar.</span><span class="sxs-lookup"><span data-stu-id="936cc-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="936cc-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="936cc-112">Requirements</span></span>



| <span data-ttu-id="936cc-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="936cc-113">Requirement</span></span> | <span data-ttu-id="936cc-114">Valor</span><span class="sxs-lookup"><span data-stu-id="936cc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936cc-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="936cc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="936cc-116"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="936cc-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="936cc-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="936cc-117">Library</span></span><br/> | <dl> <span data-ttu-id="936cc-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="936cc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936cc-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="936cc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936cc-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="936cc-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




