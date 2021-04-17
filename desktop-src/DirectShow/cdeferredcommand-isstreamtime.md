---
description: O método isstreamtime especifica se o comando deve ser executado no horário do fluxo ou na hora da apresentação.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Método CDeferredCommand. isstreamtime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e15b579f911f6461df30c6b5ae9d3fc29f6fa1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758696"
---
# <a name="cdeferredcommandisstreamtime-method"></a><span data-ttu-id="37916-103">Método CDeferredCommand. isstreamtime</span><span class="sxs-lookup"><span data-stu-id="37916-103">CDeferredCommand.IsStreamTime method</span></span>

<span data-ttu-id="37916-104">O `IsStreamTime` método especifica se o comando deve ser executado no momento do fluxo ou na hora da apresentação.</span><span class="sxs-lookup"><span data-stu-id="37916-104">The `IsStreamTime` method specifies whether the command is to be run at stream time or presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="37916-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37916-105">Syntax</span></span>


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a><span data-ttu-id="37916-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37916-106">Parameters</span></span>

<span data-ttu-id="37916-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37916-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37916-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37916-108">Return value</span></span>

<span data-ttu-id="37916-109">Retorna **true** se definido como Stream time; caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="37916-109">Returns **TRUE** if set to stream time; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="37916-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37916-110">Requirements</span></span>



| <span data-ttu-id="37916-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="37916-111">Requirement</span></span> | <span data-ttu-id="37916-112">Valor</span><span class="sxs-lookup"><span data-stu-id="37916-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37916-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37916-113">Header</span></span><br/>  | <dl> <span data-ttu-id="37916-114"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37916-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37916-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37916-115">Library</span></span><br/> | <dl> <span data-ttu-id="37916-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="37916-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37916-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="37916-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37916-118">**Classe CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="37916-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




