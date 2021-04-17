---
description: O método GetCountOfType recupera o número de objetos de um determinado tipo contido nessa composição e todas as suas faixas virtuais, recursivamente.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'Método IAMTimelineComp:: GetCountOfType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754251"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="93efd-103">Método IAMTimelineComp:: GetCountOfType</span><span class="sxs-lookup"><span data-stu-id="93efd-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="93efd-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="93efd-104">\[Deprecated.</span></span> <span data-ttu-id="93efd-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93efd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="93efd-106">O `GetCountOfType` método recupera o número de objetos de um determinado tipo contido nessa composição e todas as suas faixas virtuais, recursivamente.</span><span class="sxs-lookup"><span data-stu-id="93efd-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="93efd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93efd-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="93efd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93efd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93efd-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="93efd-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="93efd-110">Recebe o número de objetos do tipo especificado contido nesta composição e todas as suas faixas virtuais, recursivamente.</span><span class="sxs-lookup"><span data-stu-id="93efd-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="93efd-111">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="93efd-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="93efd-112">Recebe a contagem retornada em *PVal* mais o número de composições pesquisadas, incluindo esta.</span><span class="sxs-lookup"><span data-stu-id="93efd-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="93efd-113">*Majortype*</span><span class="sxs-lookup"><span data-stu-id="93efd-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="93efd-114">Membro do tipo enumerado de [**\_ \_ tipo principal da linha de tempo**](timeline-major-type.md) , especificando o tipo de objeto a ser contabilizado.</span><span class="sxs-lookup"><span data-stu-id="93efd-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93efd-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93efd-115">Return value</span></span>

<span data-ttu-id="93efd-116">Retorna S \_ OK se for bem-sucedido ou o \_ ponteiro do contrário.</span><span class="sxs-lookup"><span data-stu-id="93efd-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="93efd-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="93efd-117">Remarks</span></span>

<span data-ttu-id="93efd-118">Normalmente, um aplicativo não chamará esse método.</span><span class="sxs-lookup"><span data-stu-id="93efd-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="93efd-119">Ele é chamado pelo mecanismo de processamento.</span><span class="sxs-lookup"><span data-stu-id="93efd-119">It is called by the render engine.</span></span>

<span data-ttu-id="93efd-120">Se você contar as composições, o valor retornado em *PVal* será zero e o valor retornado em *pValWithComps* será o número de composições.</span><span class="sxs-lookup"><span data-stu-id="93efd-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="93efd-121">O valor de *\* pValWithComps* inclui a composição na qual você chama o método.</span><span class="sxs-lookup"><span data-stu-id="93efd-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="93efd-122">Por exemplo, se você chamar esse método em uma composição vazia, *\* pValWithComps* será igual a 1.</span><span class="sxs-lookup"><span data-stu-id="93efd-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="93efd-123">Os grupos não podem residir em composições, portanto, você não pode usar esse método para contar grupos.</span><span class="sxs-lookup"><span data-stu-id="93efd-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="93efd-124">(A contagem retornada sempre será zero.) Para contar grupos, chame o método [**IAMTimeline:: GetGroupCount**](iamtimeline-getgroupcount.md) .</span><span class="sxs-lookup"><span data-stu-id="93efd-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="93efd-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="93efd-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="93efd-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="93efd-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="93efd-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="93efd-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93efd-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93efd-128">Requirements</span></span>



| <span data-ttu-id="93efd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="93efd-129">Requirement</span></span> | <span data-ttu-id="93efd-130">Valor</span><span class="sxs-lookup"><span data-stu-id="93efd-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93efd-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93efd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="93efd-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="93efd-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="93efd-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93efd-133">Library</span></span><br/> | <dl> <span data-ttu-id="93efd-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93efd-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93efd-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="93efd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93efd-136">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="93efd-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="93efd-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="93efd-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




