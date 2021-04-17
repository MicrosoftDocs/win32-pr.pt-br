---
description: O método InsertSpace divide todos os objetos que existem no tempo especificado e insere um espaço entre eles.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Método IAMTimelineTrack:: InsertSpace (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760880"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="1245e-103">Método IAMTimelineTrack:: InsertSpace</span><span class="sxs-lookup"><span data-stu-id="1245e-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="1245e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1245e-104">\[Deprecated.</span></span> <span data-ttu-id="1245e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1245e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1245e-106">O `InsertSpace` método divide todos os objetos existentes na hora especificada e insere o espaço entre eles.</span><span class="sxs-lookup"><span data-stu-id="1245e-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="1245e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1245e-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="1245e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1245e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1245e-109">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="1245e-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="1245e-110">Hora na qual criar a divisão e o ponto inicial do espaço inserido, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="1245e-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1245e-111">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="1245e-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1245e-112">Ponto de extremidade do espaço inserido, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="1245e-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1245e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1245e-113">Return value</span></span>

<span data-ttu-id="1245e-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1245e-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1245e-115">Os possíveis valores de retorno incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1245e-115">Possible return values include the following:</span></span>



| <span data-ttu-id="1245e-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1245e-116">Return code</span></span>                                                                                   | <span data-ttu-id="1245e-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="1245e-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="1245e-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="1245e-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="1245e-119">Não há objetos no horário especificado.</span><span class="sxs-lookup"><span data-stu-id="1245e-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="1245e-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1245e-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1245e-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1245e-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1245e-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1245e-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="1245e-123">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="1245e-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="1245e-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1245e-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1245e-125">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1245e-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="1245e-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1245e-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1245e-127">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1245e-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1245e-128">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1245e-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1245e-129">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1245e-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1245e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1245e-130">Requirements</span></span>



| <span data-ttu-id="1245e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1245e-131">Requirement</span></span> | <span data-ttu-id="1245e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1245e-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1245e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1245e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="1245e-134"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1245e-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1245e-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1245e-135">Library</span></span><br/> | <dl> <span data-ttu-id="1245e-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1245e-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1245e-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1245e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1245e-138">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="1245e-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="1245e-139">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1245e-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




