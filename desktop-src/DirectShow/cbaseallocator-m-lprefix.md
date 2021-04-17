---
description: Prefixo de cada buffer, em bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Membro CBaseAllocator:: m_lPrefix (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755397"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="4f6e0-103">Membro de CBaseAllocator:: m \_ lPrefix</span><span class="sxs-lookup"><span data-stu-id="4f6e0-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="4f6e0-104">Prefixo de cada buffer, em bytes.</span><span class="sxs-lookup"><span data-stu-id="4f6e0-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="4f6e0-105">Se o valor for diferente de zero, cada ponteiro de buffer retornado pelo método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) será precedido por um bloco de bytes de tamanho *m \_ lPrefix*.</span><span class="sxs-lookup"><span data-stu-id="4f6e0-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="4f6e0-106">Esse bloco de memória é chamado de *prefixo*.</span><span class="sxs-lookup"><span data-stu-id="4f6e0-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="4f6e0-107">A variável de membro [**CBaseAllocator:: m \_ lSize**](cbaseallocator-m-lsize.md) não inclui o valor de prefixo.</span><span class="sxs-lookup"><span data-stu-id="4f6e0-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f6e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f6e0-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="4f6e0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f6e0-109">Requirements</span></span>



| <span data-ttu-id="4f6e0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f6e0-110">Requirement</span></span> | <span data-ttu-id="4f6e0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4f6e0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f6e0-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f6e0-112">Header</span></span><br/>  | <dl> <span data-ttu-id="4f6e0-113"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e0-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4f6e0-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f6e0-114">Library</span></span><br/> | <dl> <span data-ttu-id="4f6e0-115"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4f6e0-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f6e0-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f6e0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f6e0-117">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="4f6e0-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




