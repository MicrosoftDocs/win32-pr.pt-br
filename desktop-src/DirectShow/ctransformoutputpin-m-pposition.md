---
description: Objeto auxiliar para passar comandos de busca upstream.
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membro CTransformOutputPin:: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749824"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="0d26e-103">Membro de CTransformOutputPin:: m \_ pPosition</span><span class="sxs-lookup"><span data-stu-id="0d26e-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="0d26e-104">Objeto auxiliar para passar comandos de busca upstream.</span><span class="sxs-lookup"><span data-stu-id="0d26e-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d26e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d26e-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="0d26e-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d26e-106">Remarks</span></span>

<span data-ttu-id="0d26e-107">Quando o PIN é consultado pela primeira vez para a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) ou [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , ele cria e agrega um objeto auxiliar [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="0d26e-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d26e-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d26e-108">Requirements</span></span>



| <span data-ttu-id="0d26e-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d26e-109">Requirement</span></span> | <span data-ttu-id="0d26e-110">Valor</span><span class="sxs-lookup"><span data-stu-id="0d26e-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d26e-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d26e-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0d26e-112"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d26e-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0d26e-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d26e-113">Library</span></span><br/> | <dl> <span data-ttu-id="0d26e-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0d26e-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




