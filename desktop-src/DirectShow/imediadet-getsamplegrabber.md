---
description: O método GetSampleGrabber recupera um ponteiro para a interface ISampleGrabber, que permite que um aplicativo recupere amostras individuais de um fluxo de mídia.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Método IMediaDet:: GetSampleGrabber (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789641"
---
# <a name="imediadetgetsamplegrabber-method"></a><span data-ttu-id="188c3-103">Método IMediaDet:: GetSampleGrabber</span><span class="sxs-lookup"><span data-stu-id="188c3-103">IMediaDet::GetSampleGrabber method</span></span>

> [!Note]  
> <span data-ttu-id="188c3-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="188c3-104">\[Deprecated.</span></span> <span data-ttu-id="188c3-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="188c3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="188c3-106">O `GetSampleGrabber` método recupera um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) , que permite que um aplicativo recupere amostras individuais de um fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="188c3-106">The `GetSampleGrabber` method retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface, which enables an application to retrieve individual samples from a media stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="188c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="188c3-107">Syntax</span></span>


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a><span data-ttu-id="188c3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="188c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="188c3-109">*ppVal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="188c3-109">*ppVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="188c3-110">Recebe um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="188c3-110">Receives a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="188c3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="188c3-111">Return value</span></span>

<span data-ttu-id="188c3-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="188c3-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="188c3-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="188c3-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="188c3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="188c3-114">Remarks</span></span>

<span data-ttu-id="188c3-115">Chame [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="188c3-115">Call [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) before calling this method.</span></span> <span data-ttu-id="188c3-116">A interface [**ISampleGrabber**](isamplegrabber.md) permite que você recupere amostras de mídia individuais do fluxo.</span><span class="sxs-lookup"><span data-stu-id="188c3-116">The [**ISampleGrabber**](isamplegrabber.md) interface enables you to retrieve individual media samples from the stream.</span></span> <span data-ttu-id="188c3-117">Se você apenas precisar de um bitmap de um quadro de vídeo, chame o método [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) .</span><span class="sxs-lookup"><span data-stu-id="188c3-117">If you just need a bitmap from a video frame, call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method instead.</span></span> <span data-ttu-id="188c3-118">A interface **ISampleGrabber** é mais flexível, mas requer mais trabalho pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="188c3-118">The **ISampleGrabber** interface is more flexible, but requires more work by the application.</span></span>

<span data-ttu-id="188c3-119">Se esse método tiver sucesso, a interface [**ISampleGrabber**](isamplegrabber.md) que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="188c3-119">If this method succeeds, the [**ISampleGrabber**](isamplegrabber.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="188c3-120">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="188c3-120">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="188c3-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="188c3-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="188c3-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="188c3-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="188c3-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="188c3-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="188c3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="188c3-124">Requirements</span></span>



| <span data-ttu-id="188c3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="188c3-125">Requirement</span></span> | <span data-ttu-id="188c3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="188c3-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="188c3-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="188c3-127">Header</span></span><br/>  | <dl> <span data-ttu-id="188c3-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="188c3-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="188c3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="188c3-129">Library</span></span><br/> | <dl> <span data-ttu-id="188c3-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="188c3-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="188c3-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="188c3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="188c3-132">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="188c3-132">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="188c3-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="188c3-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




