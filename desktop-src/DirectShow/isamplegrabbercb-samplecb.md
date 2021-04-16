---
description: O método SampleCB é um método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: 'Método ISampleGrabberCB:: SampleCB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6e66f4a43666add7a5d6cb579fcf15f0fc1ec0cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782227"
---
# <a name="isamplegrabbercbsamplecb-method"></a><span data-ttu-id="ef26a-103">Método ISampleGrabberCB:: SampleCB</span><span class="sxs-lookup"><span data-stu-id="ef26a-103">ISampleGrabberCB::SampleCB method</span></span>

> [!Note]  
> <span data-ttu-id="ef26a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ef26a-104">\[Deprecated.</span></span> <span data-ttu-id="ef26a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef26a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef26a-106">O `SampleCB` método é um método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="ef26a-106">The `SampleCB` method is a callback method that receives a pointer to the media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef26a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef26a-107">Syntax</span></span>


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="ef26a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef26a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef26a-109">*Exemplo de*</span><span class="sxs-lookup"><span data-stu-id="ef26a-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="ef26a-110">Hora de início do exemplo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="ef26a-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ef26a-111">*pSample*</span><span class="sxs-lookup"><span data-stu-id="ef26a-111">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ef26a-112">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="ef26a-112">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef26a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef26a-113">Return value</span></span>

<span data-ttu-id="ef26a-114">Retorna S \_ OK se tiver êxito ou um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef26a-114">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef26a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef26a-115">Remarks</span></span>

<span data-ttu-id="ef26a-116">Para configurar o retorno de chamada, chame [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="ef26a-116">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="ef26a-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ef26a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef26a-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef26a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ef26a-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ef26a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef26a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef26a-120">Requirements</span></span>



| <span data-ttu-id="ef26a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef26a-121">Requirement</span></span> | <span data-ttu-id="ef26a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ef26a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef26a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef26a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ef26a-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ef26a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef26a-125">Library</span></span><br/> | <dl> <span data-ttu-id="ef26a-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef26a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef26a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef26a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef26a-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ef26a-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="ef26a-129">**Interface ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="ef26a-129">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




