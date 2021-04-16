---
description: O método BufferCB é um método de retorno de chamada que recebe um ponteiro para o buffer de exemplo.
ms.assetid: 9ee16dd6-8d05-4a9a-84c3-1b3bb95eaa04
title: 'Método ISampleGrabberCB:: BufferCB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.BufferCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8af11545db1a3ed839f409deb141e5d910abe198
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768594"
---
# <a name="isamplegrabbercbbuffercb-method"></a><span data-ttu-id="1a35c-103">Método ISampleGrabberCB:: BufferCB</span><span class="sxs-lookup"><span data-stu-id="1a35c-103">ISampleGrabberCB::BufferCB method</span></span>

> [!Note]  
> <span data-ttu-id="1a35c-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1a35c-104">\[Deprecated.</span></span> <span data-ttu-id="1a35c-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1a35c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a35c-106">O método **BufferCB** é um método de retorno de chamada que recebe um ponteiro para o buffer de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1a35c-106">The **BufferCB** method is a callback method that receives a pointer to the sample buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a35c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a35c-107">Syntax</span></span>


```C++
HRESULT BufferCB(
   double SampleTime,
   BYTE   *pBuffer,
   long   BufferLen
);
```



## <a name="parameters"></a><span data-ttu-id="1a35c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a35c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a35c-109">*Exemplo de*</span><span class="sxs-lookup"><span data-stu-id="1a35c-109">*SampleTime*</span></span> 
</dt> <dd>

<span data-ttu-id="1a35c-110">Hora de início do exemplo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="1a35c-110">Starting time of the sample, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1a35c-111">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="1a35c-111">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="1a35c-112">Ponteiro para um buffer que contém os dados de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1a35c-112">Pointer to a buffer that contains the sample data.</span></span> <span data-ttu-id="1a35c-113">O formato dos dados depende do tipo de mídia do pino de entrada do exemplo de apoio.</span><span class="sxs-lookup"><span data-stu-id="1a35c-113">The format of the data depends on the media type of the Sample Grabber's input pin.</span></span> <span data-ttu-id="1a35c-114">Para obter o tipo de mídia, chame [**ISampleGrabber:: GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="1a35c-114">To get the media type, call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="1a35c-115">*BufferLen*</span><span class="sxs-lookup"><span data-stu-id="1a35c-115">*BufferLen*</span></span> 
</dt> <dd>

<span data-ttu-id="1a35c-116">Comprimento do buffer apontado por *pBuffer*, em bytes.</span><span class="sxs-lookup"><span data-stu-id="1a35c-116">Length of the buffer pointed to by *pBuffer*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a35c-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a35c-117">Return value</span></span>

<span data-ttu-id="1a35c-118">Retorna S \_ OK se tiver êxito ou um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a35c-118">Returns S\_OK if successful, or an **HRESULT** error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a35c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a35c-119">Remarks</span></span>

<span data-ttu-id="1a35c-120">Esse método de retorno de chamada recebe um ponteiro para os dados no exemplo de mídia mais recente.</span><span class="sxs-lookup"><span data-stu-id="1a35c-120">This callback method receives a pointer to the data in the most recent media sample.</span></span>

> [!Note]  
> <span data-ttu-id="1a35c-121">Esse método recebe um ponteiro para os dados de exemplo originais, não para uma cópia.</span><span class="sxs-lookup"><span data-stu-id="1a35c-121">This method receives a pointer to the original sample data, not a copy.</span></span> <span data-ttu-id="1a35c-122">A documentação original incorretamente afirmou que *pBuffer* contém uma cópia dos dados.</span><span class="sxs-lookup"><span data-stu-id="1a35c-122">The original documentation incorrectly stated that *pBuffer* contains a copy of the data.</span></span>

 

<span data-ttu-id="1a35c-123">Para configurar o retorno de chamada, chame [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md).</span><span class="sxs-lookup"><span data-stu-id="1a35c-123">To set up the callback, call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).</span></span>

> [!Note]  
> <span data-ttu-id="1a35c-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1a35c-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a35c-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1a35c-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a35c-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1a35c-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a35c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a35c-127">Requirements</span></span>



| <span data-ttu-id="1a35c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a35c-128">Requirement</span></span> | <span data-ttu-id="1a35c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1a35c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a35c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a35c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1a35c-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a35c-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a35c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a35c-132">Library</span></span><br/> | <dl> <span data-ttu-id="1a35c-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a35c-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a35c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a35c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a35c-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1a35c-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="1a35c-136">**Interface ISampleGrabberCB**</span><span class="sxs-lookup"><span data-stu-id="1a35c-136">**ISampleGrabberCB Interface**</span></span>](isamplegrabbercb.md)
</dt> </dl>

 

 




