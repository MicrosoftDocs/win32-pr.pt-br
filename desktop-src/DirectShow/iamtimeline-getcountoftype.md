---
description: O método GetCountOfType recupera o número de objetos do tipo especificado que estão contidos em um grupo especificado e todos os seus filhos.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'Método IAMTimeline:: GetCountOfType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751873"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="c6ab9-103">Método IAMTimeline:: GetCountOfType</span><span class="sxs-lookup"><span data-stu-id="c6ab9-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="c6ab9-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-104">\[Deprecated.</span></span> <span data-ttu-id="c6ab9-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6ab9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c6ab9-106">O `GetCountOfType` método recupera o número de objetos do tipo especificado que estão contidos em um grupo especificado e todos os seus filhos.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ab9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6ab9-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="c6ab9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6ab9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6ab9-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="c6ab9-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="c6ab9-110">Número de índice do grupo para o qual a contagem será recuperada.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="c6ab9-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="c6ab9-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="c6ab9-112">Recebe o número de objetos do tipo especificado contido no grupo e todas as suas faixas virtuais, recursivamente.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="c6ab9-113">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="c6ab9-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="c6ab9-114">Recebe a contagem retornada em *PVal* mais o número de composições pesquisadas, incluindo esta.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="c6ab9-115">*Majortype*</span><span class="sxs-lookup"><span data-stu-id="c6ab9-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="c6ab9-116">Membro do tipo enumerado de [**\_ \_ tipo principal da linha de tempo**](timeline-major-type.md) , especificando o tipo de objeto a ser contabilizado.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6ab9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6ab9-117">Return value</span></span>

<span data-ttu-id="c6ab9-118">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="c6ab9-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c6ab9-119">Return code</span></span>                                                                                  | <span data-ttu-id="c6ab9-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6ab9-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c6ab9-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ab9-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c6ab9-122">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="c6ab9-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ab9-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c6ab9-124">Número de grupo inválido.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="c6ab9-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c6ab9-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="c6ab9-126">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c6ab9-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c6ab9-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6ab9-127">Remarks</span></span>

<span data-ttu-id="c6ab9-128">Chamar esse método é equivalente a chamar [**IAMTimelineComp:: GetCountOfType**](iamtimelinecomp-getcountoftype.md) no grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="c6ab9-129">Consulte a seção comentários desse método para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="c6ab9-130">Normalmente, um aplicativo não chamará esse método.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="c6ab9-131">Ele é chamado internamente pelo mecanismo de processamento.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="c6ab9-132">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6ab9-133">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c6ab9-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c6ab9-134">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c6ab9-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6ab9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6ab9-135">Requirements</span></span>



| <span data-ttu-id="c6ab9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ab9-136">Requirement</span></span> | <span data-ttu-id="c6ab9-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c6ab9-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ab9-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6ab9-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c6ab9-139"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ab9-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c6ab9-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6ab9-140">Library</span></span><br/> | <dl> <span data-ttu-id="c6ab9-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6ab9-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ab9-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6ab9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ab9-143">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="c6ab9-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c6ab9-144">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="c6ab9-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




