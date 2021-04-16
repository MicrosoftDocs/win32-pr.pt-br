---
description: O método IsUsingDefaultSource determina se o renderizador está usando a janela de origem padrão.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Método CBaseControlVideo. IsUsingDefaultSource (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751281"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a><span data-ttu-id="4e76a-103">Método CBaseControlVideo. IsUsingDefaultSource</span><span class="sxs-lookup"><span data-stu-id="4e76a-103">CBaseControlVideo.IsUsingDefaultSource method</span></span>

<span data-ttu-id="4e76a-104">O `IsUsingDefaultSource` método determina se o renderizador está usando a janela de origem padrão.</span><span class="sxs-lookup"><span data-stu-id="4e76a-104">The `IsUsingDefaultSource` method determines if the renderer is using the default source window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e76a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e76a-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a><span data-ttu-id="4e76a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e76a-106">Parameters</span></span>

<span data-ttu-id="4e76a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4e76a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e76a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e76a-108">Return value</span></span>

<span data-ttu-id="4e76a-109">Retornará S \_ OK se o renderizador estiver usando a origem padrão; caso contrário, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="4e76a-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e76a-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e76a-110">Requirements</span></span>



| <span data-ttu-id="4e76a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e76a-111">Requirement</span></span> | <span data-ttu-id="4e76a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4e76a-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e76a-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e76a-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4e76a-114"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e76a-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e76a-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e76a-115">Library</span></span><br/> | <dl> <span data-ttu-id="4e76a-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4e76a-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e76a-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e76a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e76a-118">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="4e76a-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




