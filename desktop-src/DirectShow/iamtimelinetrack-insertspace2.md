---
description: 'O método InsertSpace2 divide todos os objetos que existem no tempo especificado e insere um espaço entre eles. Esse método é equivalente a IAMTimelineTrack:: InsertSpace, mas usa os valores de REFTIME.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Método IAMTimelineTrack:: InsertSpace2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785487"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="b8bd8-104">Método IAMTimelineTrack:: InsertSpace2</span><span class="sxs-lookup"><span data-stu-id="b8bd8-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="b8bd8-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-105">\[Deprecated.</span></span> <span data-ttu-id="b8bd8-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8bd8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8bd8-107">O `InsertSpace2` método divide todos os objetos existentes na hora especificada e insere o espaço entre eles.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="b8bd8-108">Esse método é equivalente a [**IAMTimelineTrack:: InsertSpace**](iamtimelinetrack-insertspace.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="b8bd8-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8bd8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8bd8-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="b8bd8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8bd8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8bd8-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="b8bd8-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="b8bd8-112">Hora na qual criar a divisão e o ponto inicial do espaço inserido, em segundos.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="b8bd8-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="b8bd8-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b8bd8-114">Ponto de extremidade do espaço inserido, em segundos.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8bd8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8bd8-115">Return value</span></span>

<span data-ttu-id="b8bd8-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8bd8-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b8bd8-117">Os possíveis valores de retorno incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b8bd8-117">Possible return values include the following:</span></span>



| <span data-ttu-id="b8bd8-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b8bd8-118">Return code</span></span>                                                                                   | <span data-ttu-id="b8bd8-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8bd8-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="b8bd8-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="b8bd8-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="b8bd8-121">Não há objetos no horário especificado.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="b8bd8-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8bd8-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b8bd8-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b8bd8-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b8bd8-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b8bd8-125">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="b8bd8-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b8bd8-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b8bd8-127">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="b8bd8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8bd8-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8bd8-129">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8bd8-130">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8bd8-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b8bd8-131">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b8bd8-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8bd8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8bd8-132">Requirements</span></span>



| <span data-ttu-id="b8bd8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8bd8-133">Requirement</span></span> | <span data-ttu-id="b8bd8-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b8bd8-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8bd8-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8bd8-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b8bd8-136"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8bd8-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8bd8-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8bd8-137">Library</span></span><br/> | <dl> <span data-ttu-id="b8bd8-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8bd8-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8bd8-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8bd8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8bd8-140">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="b8bd8-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="b8bd8-141">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="b8bd8-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




