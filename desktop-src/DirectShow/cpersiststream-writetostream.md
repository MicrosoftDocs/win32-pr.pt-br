---
description: Grava os dados do filtro em um determinado fluxo.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Método CPersistStream. WriteToStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810241"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="c960d-103">Método CPersistStream. WriteToStream</span><span class="sxs-lookup"><span data-stu-id="c960d-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="c960d-104">Grava os dados do filtro em um determinado fluxo.</span><span class="sxs-lookup"><span data-stu-id="c960d-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c960d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c960d-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="c960d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c960d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c960d-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="c960d-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="c960d-108">Ponteiro para uma interface **IStream** que especifica o fluxo de destino dos dados do filtro.</span><span class="sxs-lookup"><span data-stu-id="c960d-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c960d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c960d-109">Return value</span></span>

<span data-ttu-id="c960d-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c960d-110">Returns S\_OK.</span></span> <span data-ttu-id="c960d-111">A classe derivada deve retornar um valor **HRESULT** válido.</span><span class="sxs-lookup"><span data-stu-id="c960d-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c960d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c960d-112">Remarks</span></span>

<span data-ttu-id="c960d-113">A versão padrão não grava nada; Ele pode ser substituído para gravar dados específicos para sua classe.</span><span class="sxs-lookup"><span data-stu-id="c960d-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="c960d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c960d-114">Requirements</span></span>



| <span data-ttu-id="c960d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c960d-115">Requirement</span></span> | <span data-ttu-id="c960d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c960d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c960d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c960d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c960d-118"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c960d-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c960d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c960d-119">Library</span></span><br/> | <dl> <span data-ttu-id="c960d-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c960d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c960d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c960d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c960d-122">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="c960d-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




