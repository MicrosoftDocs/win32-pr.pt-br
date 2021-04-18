---
description: Recupera o tamanho máximo de bytes necessário para o fluxo atual, incluindo o número de versão.
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: Método CPersistStream. GetSizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756616"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="f4392-103">Método CPersistStream. GetSizeMax</span><span class="sxs-lookup"><span data-stu-id="f4392-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="f4392-104">Recupera o tamanho máximo de bytes necessário para o fluxo atual, incluindo o número de versão.</span><span class="sxs-lookup"><span data-stu-id="f4392-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4392-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4392-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="f4392-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4392-107">*pcbSize*</span><span class="sxs-lookup"><span data-stu-id="f4392-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="f4392-108">Ponteiro para o tamanho em bytes necessário para salvar este fluxo, incluindo o número de versão.</span><span class="sxs-lookup"><span data-stu-id="f4392-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4392-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4392-109">Return value</span></span>

<span data-ttu-id="f4392-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4392-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4392-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4392-111">Remarks</span></span>

<span data-ttu-id="f4392-112">Essa função de membro implementa o método **IPersistStream:: GetSizeMax** .</span><span class="sxs-lookup"><span data-stu-id="f4392-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4392-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4392-113">Requirements</span></span>



| <span data-ttu-id="f4392-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4392-114">Requirement</span></span> | <span data-ttu-id="f4392-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f4392-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4392-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4392-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f4392-117"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4392-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f4392-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4392-118">Library</span></span><br/> | <dl> <span data-ttu-id="f4392-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f4392-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4392-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4392-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4392-121">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="f4392-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




