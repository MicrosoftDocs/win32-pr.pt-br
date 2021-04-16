---
description: 'O método SplitAt2 divide o objeto na hora especificada. Esse método é equivalente a IAMTimelineSplittable:: SplitAt, mas usa um valor de REFTIME.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'Método IAMTimelineSplittable:: SplitAt2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757682"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="7fae1-104">Método IAMTimelineSplittable:: SplitAt2</span><span class="sxs-lookup"><span data-stu-id="7fae1-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="7fae1-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="7fae1-105">\[Deprecated.</span></span> <span data-ttu-id="7fae1-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fae1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7fae1-107">O `SplitAt2` método divide o objeto na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="7fae1-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="7fae1-108">Esse método é equivalente a [**IAMTimelineSplittable:: SplitAt**](iamtimelinesplittable-splitat.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="7fae1-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fae1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7fae1-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="7fae1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7fae1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fae1-111">*Hora*</span><span class="sxs-lookup"><span data-stu-id="7fae1-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="7fae1-112">Hora na qual dividir o objeto, em relação ao início da linha do tempo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="7fae1-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fae1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7fae1-113">Return value</span></span>

<span data-ttu-id="7fae1-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fae1-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7fae1-115">Os possíveis valores incluem os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7fae1-115">Possible values include the following:</span></span>



| <span data-ttu-id="7fae1-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7fae1-116">Return code</span></span>                                                                                   | <span data-ttu-id="7fae1-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fae1-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="7fae1-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="7fae1-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="7fae1-119">Nada para dividir.</span><span class="sxs-lookup"><span data-stu-id="7fae1-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="7fae1-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7fae1-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7fae1-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7fae1-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="7fae1-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fae1-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7fae1-123">O objeto não existe no momento.</span><span class="sxs-lookup"><span data-stu-id="7fae1-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="7fae1-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7fae1-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7fae1-125">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="7fae1-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="7fae1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fae1-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7fae1-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="7fae1-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7fae1-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fae1-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7fae1-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="7fae1-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7fae1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fae1-130">Requirements</span></span>



| <span data-ttu-id="7fae1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fae1-131">Requirement</span></span> | <span data-ttu-id="7fae1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7fae1-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fae1-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fae1-133">Header</span></span><br/>  | <dl> <span data-ttu-id="7fae1-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fae1-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7fae1-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7fae1-135">Library</span></span><br/> | <dl> <span data-ttu-id="7fae1-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fae1-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fae1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7fae1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fae1-138">**Interface IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="7fae1-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="7fae1-139">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="7fae1-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




