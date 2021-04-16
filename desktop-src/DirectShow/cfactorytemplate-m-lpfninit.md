---
description: Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL. Pode ser NULL.
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'Membro CFactoryTemplate:: m_lpfnInit (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750659"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="078ab-104">Membro de CFactoryTemplate:: m \_ lpfnInit</span><span class="sxs-lookup"><span data-stu-id="078ab-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="078ab-105">Ponteiro para uma função que é chamada a partir do ponto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="078ab-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="078ab-106">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="078ab-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="078ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="078ab-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="078ab-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="078ab-108">Remarks</span></span>

<span data-ttu-id="078ab-109">O tipo de ponteiro de função é [**LPFNInitRoutine**](lpfninitroutine.md).</span><span class="sxs-lookup"><span data-stu-id="078ab-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="078ab-110">Se você fornecer essa função em sua DLL, a função de ponto de entrada de DLL a chamará com os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="078ab-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="078ab-111">*bLoading*: **true** quando a dll é carregada, **false** quando a dll é descarregada.</span><span class="sxs-lookup"><span data-stu-id="078ab-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="078ab-112">*rclsid*: ponteiro para o CLISD do objeto, especificado na variável de membro [**\_ ClsID CFactoryTemplate:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="078ab-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="078ab-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="078ab-113">Requirements</span></span>



| <span data-ttu-id="078ab-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="078ab-114">Requirement</span></span> | <span data-ttu-id="078ab-115">Valor</span><span class="sxs-lookup"><span data-stu-id="078ab-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="078ab-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="078ab-116">Header</span></span><br/>  | <dl> <span data-ttu-id="078ab-117"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="078ab-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="078ab-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="078ab-118">Library</span></span><br/> | <dl> <span data-ttu-id="078ab-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="078ab-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="078ab-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="078ab-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="078ab-121">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="078ab-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




