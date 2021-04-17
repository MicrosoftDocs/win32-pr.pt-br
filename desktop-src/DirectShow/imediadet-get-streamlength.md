---
description: O \_ método Get streamLength recupera a duração do fluxo atual.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: 'Método IMediaDet:: get_StreamLength (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 61fe92fcb845a626fafc8ebb49126a35cf633aea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757015"
---
# <a name="imediadetget_streamlength-method"></a><span data-ttu-id="72069-103">Método IMediaDet:: get \_ streamLength</span><span class="sxs-lookup"><span data-stu-id="72069-103">IMediaDet::get\_StreamLength method</span></span>

> [!Note]  
> <span data-ttu-id="72069-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="72069-104">\[Deprecated.</span></span> <span data-ttu-id="72069-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="72069-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="72069-106">O `get_StreamLength` método recupera a duração do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="72069-106">The `get_StreamLength` method retrieves the duration of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="72069-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72069-107">Syntax</span></span>


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="72069-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72069-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72069-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="72069-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="72069-110">Recebe a duração do fluxo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="72069-110">Receives the duration of the stream, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72069-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72069-111">Return value</span></span>

<span data-ttu-id="72069-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72069-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72069-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72069-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72069-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="72069-114">Remarks</span></span>

<span data-ttu-id="72069-115">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="72069-115">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="72069-116">Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="72069-116">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="72069-117">Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="72069-117">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="72069-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="72069-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="72069-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="72069-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="72069-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="72069-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="72069-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72069-121">Requirements</span></span>



| <span data-ttu-id="72069-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="72069-122">Requirement</span></span> | <span data-ttu-id="72069-123">Valor</span><span class="sxs-lookup"><span data-stu-id="72069-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72069-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72069-124">Header</span></span><br/>  | <dl> <span data-ttu-id="72069-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="72069-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="72069-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72069-126">Library</span></span><br/> | <dl> <span data-ttu-id="72069-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72069-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72069-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="72069-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72069-129">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="72069-129">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="72069-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="72069-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




