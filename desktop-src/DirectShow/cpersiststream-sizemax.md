---
description: Recupera o tamanho máximo de bytes necessário para o fluxo atual, não incluindo o número de versão.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Método CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771843"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="50b57-103">Método CPersistStream. SizeMax</span><span class="sxs-lookup"><span data-stu-id="50b57-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="50b57-104">Recupera o tamanho máximo de bytes necessário para o fluxo atual, não incluindo o número de versão.</span><span class="sxs-lookup"><span data-stu-id="50b57-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b57-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="50b57-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="50b57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50b57-106">Parameters</span></span>

<span data-ttu-id="50b57-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="50b57-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50b57-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50b57-108">Return value</span></span>

<span data-ttu-id="50b57-109">Retorna o número de bytes necessários para os dados, não incluindo o número de versão.</span><span class="sxs-lookup"><span data-stu-id="50b57-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="50b57-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="50b57-110">Remarks</span></span>

<span data-ttu-id="50b57-111">A versão padrão retorna zero; Ele deve ser substituído para fornecer algum outro valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="50b57-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="50b57-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b57-112">Requirements</span></span>



| <span data-ttu-id="50b57-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b57-113">Requirement</span></span> | <span data-ttu-id="50b57-114">Valor</span><span class="sxs-lookup"><span data-stu-id="50b57-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50b57-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50b57-115">Header</span></span><br/>  | <dl> <span data-ttu-id="50b57-116"><dt>PStream. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="50b57-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50b57-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50b57-117">Library</span></span><br/> | <dl> <span data-ttu-id="50b57-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="50b57-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b57-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="50b57-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b57-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="50b57-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




