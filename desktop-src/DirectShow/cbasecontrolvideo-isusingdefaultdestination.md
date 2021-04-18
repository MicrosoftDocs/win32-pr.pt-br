---
description: O método IsUsingDefaultDestination determina se o renderizador está usando a janela de destino padrão.
ms.assetid: 0b956575-4cf0-4f1f-9223-bb1ec3ae8b10
title: Método CBaseControlVideo. IsUsingDefaultDestination (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultDestination
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88168442cf741e5997c2b66fc4b83bf8205e694f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764587"
---
# <a name="cbasecontrolvideoisusingdefaultdestination-method"></a><span data-ttu-id="936cb-103">Método CBaseControlVideo. IsUsingDefaultDestination</span><span class="sxs-lookup"><span data-stu-id="936cb-103">CBaseControlVideo.IsUsingDefaultDestination method</span></span>

<span data-ttu-id="936cb-104">O `IsUsingDefaultDestination` método determina se o renderizador está usando a janela de destino padrão.</span><span class="sxs-lookup"><span data-stu-id="936cb-104">The `IsUsingDefaultDestination` method determines if the renderer is using the default destination window.</span></span>

## <a name="syntax"></a><span data-ttu-id="936cb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="936cb-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultDestination() = 0;
```



## <a name="parameters"></a><span data-ttu-id="936cb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="936cb-106">Parameters</span></span>

<span data-ttu-id="936cb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="936cb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="936cb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="936cb-108">Return value</span></span>

<span data-ttu-id="936cb-109">Retornará S \_ OK se estiver usando o destino padrão; caso contrário, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="936cb-109">Returns S\_OK if using the default destination; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="936cb-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="936cb-110">Requirements</span></span>



| <span data-ttu-id="936cb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="936cb-111">Requirement</span></span> | <span data-ttu-id="936cb-112">Valor</span><span class="sxs-lookup"><span data-stu-id="936cb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936cb-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="936cb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="936cb-114"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="936cb-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="936cb-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="936cb-115">Library</span></span><br/> | <dl> <span data-ttu-id="936cb-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="936cb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936cb-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="936cb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936cb-118">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="936cb-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




