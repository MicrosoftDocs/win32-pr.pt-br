---
description: O \_ método Get OutputStreams recupera o número de fluxos de áudio e vídeo contidos na origem da mídia. Quaisquer outros tipos de fluxo, como fluxos de dados, são ignorados.
ms.assetid: 9acd0a1e-c968-4c3b-a71a-b6aa2219a8cd
title: 'Método IMediaDet:: get_OutputStreams (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_OutputStreams
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0fa53a5ab5c315c4bedb3804ae7cefa618399590
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779523"
---
# <a name="imediadetget_outputstreams-method"></a><span data-ttu-id="62d6d-104">Método IMediaDet:: get \_ OutputStreams</span><span class="sxs-lookup"><span data-stu-id="62d6d-104">IMediaDet::get\_OutputStreams method</span></span>

> [!Note]  
> <span data-ttu-id="62d6d-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="62d6d-105">\[Deprecated.</span></span> <span data-ttu-id="62d6d-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62d6d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="62d6d-107">O `get_OutputStreams` método recupera o número de fluxos de áudio e vídeo contidos na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="62d6d-107">The `get_OutputStreams` method retrieves the number of audio and video streams contained in the media source.</span></span> <span data-ttu-id="62d6d-108">Quaisquer outros tipos de fluxo, como fluxos de dados, são ignorados.</span><span class="sxs-lookup"><span data-stu-id="62d6d-108">Any other stream types, such as data streams, are ignored.</span></span>

## <a name="syntax"></a><span data-ttu-id="62d6d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62d6d-109">Syntax</span></span>


```C++
HRESULT get_OutputStreams(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="62d6d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62d6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62d6d-111">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="62d6d-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="62d6d-112">Recebe o número de fluxos de saída.</span><span class="sxs-lookup"><span data-stu-id="62d6d-112">Receives the number of output streams.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62d6d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62d6d-113">Return value</span></span>

<span data-ttu-id="62d6d-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62d6d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62d6d-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62d6d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62d6d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="62d6d-116">Remarks</span></span>

<span data-ttu-id="62d6d-117">Antes de chamar esse método, chame [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) para definir o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="62d6d-117">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="62d6d-118">Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="62d6d-118">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="62d6d-119">Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="62d6d-119">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="62d6d-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="62d6d-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="62d6d-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62d6d-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="62d6d-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="62d6d-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62d6d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62d6d-123">Requirements</span></span>



| <span data-ttu-id="62d6d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="62d6d-124">Requirement</span></span> | <span data-ttu-id="62d6d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="62d6d-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62d6d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62d6d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="62d6d-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="62d6d-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="62d6d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62d6d-128">Library</span></span><br/> | <dl> <span data-ttu-id="62d6d-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62d6d-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62d6d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="62d6d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62d6d-131">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="62d6d-131">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="62d6d-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="62d6d-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




