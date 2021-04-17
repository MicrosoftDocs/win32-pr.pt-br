---
description: O método SplitAt divide o objeto na hora especificada.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Método IAMTimelineSplittable:: SplitAt (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784025"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="7de69-103">Método IAMTimelineSplittable:: SplitAt</span><span class="sxs-lookup"><span data-stu-id="7de69-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="7de69-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="7de69-104">\[Deprecated.</span></span> <span data-ttu-id="7de69-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7de69-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7de69-106">O `SplitAt` método divide o objeto na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="7de69-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de69-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7de69-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="7de69-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7de69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de69-109">*Hora*</span><span class="sxs-lookup"><span data-stu-id="7de69-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="7de69-110">Hora na qual dividir o objeto, em relação ao início da linha do tempo, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="7de69-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de69-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7de69-111">Return value</span></span>

<span data-ttu-id="7de69-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7de69-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7de69-113">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7de69-113">Possible values include the following:</span></span>



| <span data-ttu-id="7de69-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7de69-114">Return code</span></span>                                                                                   | <span data-ttu-id="7de69-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7de69-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="7de69-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="7de69-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="7de69-117">Nada para dividir.</span><span class="sxs-lookup"><span data-stu-id="7de69-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="7de69-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7de69-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7de69-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7de69-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="7de69-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7de69-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7de69-121">O objeto não existe no momento.</span><span class="sxs-lookup"><span data-stu-id="7de69-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="7de69-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7de69-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7de69-123">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="7de69-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7de69-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7de69-124">Remarks</span></span>

<span data-ttu-id="7de69-125">Se você dividir uma origem, um efeito ou uma transição, esse método criará um segundo objeto do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="7de69-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="7de69-126">O objeto original é truncado no tempo de divisão especificado e o novo objeto substitui a parte truncada.</span><span class="sxs-lookup"><span data-stu-id="7de69-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="7de69-127">O novo objeto herda todas as mesmas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7de69-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="7de69-128">Em um objeto de origem, o método também divide todos os efeitos que se enquadram no tempo de divisão.</span><span class="sxs-lookup"><span data-stu-id="7de69-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="7de69-129">Chamar esse método em uma faixa divide todas as origens, efeitos e transições que estão contidos na faixa no tempo de divisão especificado.</span><span class="sxs-lookup"><span data-stu-id="7de69-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="7de69-130">Ele não cria uma segunda faixa. (Uma faixa começa no tempo zero e se estende ao infinito.)</span><span class="sxs-lookup"><span data-stu-id="7de69-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="7de69-131">Para uma faixa, se o tempo de divisão for posterior ao que tudo na faixa, o método retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="7de69-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="7de69-132">Para qualquer outro objeto, se o tempo de divisão não cair em nenhum lugar dentro do objeto, o método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="7de69-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="7de69-133">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="7de69-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7de69-134">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7de69-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7de69-135">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7de69-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7de69-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7de69-136">Requirements</span></span>



| <span data-ttu-id="7de69-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="7de69-137">Requirement</span></span> | <span data-ttu-id="7de69-138">Valor</span><span class="sxs-lookup"><span data-stu-id="7de69-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7de69-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7de69-139">Header</span></span><br/>  | <dl> <span data-ttu-id="7de69-140"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7de69-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7de69-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7de69-141">Library</span></span><br/> | <dl> <span data-ttu-id="7de69-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7de69-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7de69-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="7de69-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7de69-144">**Interface IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="7de69-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="7de69-145">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="7de69-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




