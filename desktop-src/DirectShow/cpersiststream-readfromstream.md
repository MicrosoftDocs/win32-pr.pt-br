---
description: Lê os dados do filtro a partir do fluxo especificado.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Método CPersistStream. ReadFromStream (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753747"
---
# <a name="cpersiststreamreadfromstream-method"></a><span data-ttu-id="904a2-103">Método CPersistStream. ReadFromStream</span><span class="sxs-lookup"><span data-stu-id="904a2-103">CPersistStream.ReadFromStream method</span></span>

<span data-ttu-id="904a2-104">Lê os dados do filtro a partir do fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="904a2-104">Reads the filter's data from the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="904a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="904a2-105">Syntax</span></span>


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="904a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="904a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="904a2-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="904a2-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="904a2-108">Ponteiro para uma interface **IStream** da qual os dados serão lidos.</span><span class="sxs-lookup"><span data-stu-id="904a2-108">Pointer to an **IStream** interface from which data is to be read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="904a2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="904a2-109">Return value</span></span>

<span data-ttu-id="904a2-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="904a2-110">Returns S\_OK.</span></span> <span data-ttu-id="904a2-111">A classe derivada deve retornar um valor **HRESULT** válido.</span><span class="sxs-lookup"><span data-stu-id="904a2-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="904a2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="904a2-112">Remarks</span></span>

<span data-ttu-id="904a2-113">A versão padrão não lê nada; Ele pode ser substituído para ler dados específicos para sua classe.</span><span class="sxs-lookup"><span data-stu-id="904a2-113">The default version reads nothing; it can be overridden to read data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="904a2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="904a2-114">Requirements</span></span>



| <span data-ttu-id="904a2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="904a2-115">Requirement</span></span> | <span data-ttu-id="904a2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="904a2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="904a2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="904a2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="904a2-118"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="904a2-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="904a2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="904a2-119">Library</span></span><br/> | <dl> <span data-ttu-id="904a2-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="904a2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904a2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="904a2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904a2-122">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="904a2-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




