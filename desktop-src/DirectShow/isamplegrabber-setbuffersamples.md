---
description: O método SetBufferSamples especifica se os dados de exemplo devem ser copiados em um buffer conforme eles passam pelo filtro.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: 'Método ISampleGrabber:: SetBufferSamples (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9fab426b7bcad1a12895f632a719a40b4aaa8da4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759283"
---
# <a name="isamplegrabbersetbuffersamples-method"></a><span data-ttu-id="e845d-103">Método ISampleGrabber:: SetBufferSamples</span><span class="sxs-lookup"><span data-stu-id="e845d-103">ISampleGrabber::SetBufferSamples method</span></span>

> [!Note]  
> <span data-ttu-id="e845d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e845d-104">\[Deprecated.</span></span> <span data-ttu-id="e845d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e845d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e845d-106">O método **SetBufferSamples** especifica se os dados de exemplo devem ser copiados em um buffer conforme eles passam pelo filtro.</span><span class="sxs-lookup"><span data-stu-id="e845d-106">The **SetBufferSamples** method specifies whether to copy sample data into a buffer as it goes through the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e845d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e845d-107">Syntax</span></span>


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a><span data-ttu-id="e845d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e845d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e845d-109">*BufferThem*</span><span class="sxs-lookup"><span data-stu-id="e845d-109">*BufferThem*</span></span> 
</dt> <dd>

<span data-ttu-id="e845d-110">Valor booliano que especifica se os dados de exemplo devem ser armazenados em buffer.</span><span class="sxs-lookup"><span data-stu-id="e845d-110">Boolean value specifying whether to buffer sample data.</span></span> <span data-ttu-id="e845d-111">Se **for true**, o filtro copiará dados de exemplo em um buffer interno.</span><span class="sxs-lookup"><span data-stu-id="e845d-111">If **TRUE**, the filter copies sample data into an internal buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e845d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e845d-112">Return value</span></span>

<span data-ttu-id="e845d-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e845d-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e845d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e845d-114">Remarks</span></span>

<span data-ttu-id="e845d-115">Para obter o buffer copiado, chame [**ISampleGrabber:: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e845d-115">To get the copied buffer, call [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md).</span></span>

> [!Note]  
> <span data-ttu-id="e845d-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e845d-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e845d-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e845d-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e845d-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e845d-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e845d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e845d-119">Requirements</span></span>



| <span data-ttu-id="e845d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e845d-120">Requirement</span></span> | <span data-ttu-id="e845d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e845d-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e845d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e845d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e845d-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e845d-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e845d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e845d-124">Library</span></span><br/> | <dl> <span data-ttu-id="e845d-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e845d-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e845d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="e845d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e845d-127">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="e845d-127">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="e845d-128">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="e845d-128">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




