---
description: Bloquear para proteger a criação de objetos dentro do filtro.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Membro CBaseRenderer:: m_ObjectCreationLock (Renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756821"
---
# <a name="cbaserendererm_objectcreationlock-member"></a><span data-ttu-id="8e43c-103">Membro de CBaseRenderer:: m \_ ObjectCreationLock</span><span class="sxs-lookup"><span data-stu-id="8e43c-103">CBaseRenderer::m\_ObjectCreationLock member</span></span>

<span data-ttu-id="8e43c-104">Bloquear para proteger a criação de objetos dentro do filtro.</span><span class="sxs-lookup"><span data-stu-id="8e43c-104">Lock to protect the creation of objects inside the filter.</span></span> <span data-ttu-id="8e43c-105">O filtro mantém esse bloqueio quando cria o pino de entrada ([**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) ou o objeto [**CRendererPosPassThru**](crendererpospassthru.md) ([**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md)).</span><span class="sxs-lookup"><span data-stu-id="8e43c-105">The filter holds this lock when it creates the input pin ([**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md)) or the [**CRendererPosPassThru**](crendererpospassthru.md) object ([**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md)).</span></span> <span data-ttu-id="8e43c-106">Esse bloqueio impede que vários threads tentem criar um desses objetos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8e43c-106">This lock prevents multiple threads from attempting to create one of these objects at the same time.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e43c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e43c-107">Syntax</span></span>


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a><span data-ttu-id="8e43c-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e43c-108">Requirements</span></span>



| <span data-ttu-id="8e43c-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e43c-109">Requirement</span></span> | <span data-ttu-id="8e43c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="8e43c-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e43c-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e43c-111">Header</span></span><br/>  | <dl> <span data-ttu-id="8e43c-112"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e43c-112"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e43c-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e43c-113">Library</span></span><br/> | <dl> <span data-ttu-id="8e43c-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8e43c-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e43c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e43c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e43c-116">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="8e43c-116">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




