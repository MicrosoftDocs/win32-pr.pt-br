---
description: O \_ método Put CurrentStream especifica o número de fluxo para o detector de mídia a ser usado.
ms.assetid: 01fb7ccf-9b45-434c-b574-f3027d85ea8a
title: 'IMediaDet: método de ut_CurrentStream de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_CurrentStream
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864848f646e4a9e06ca12e2bfec742c1741d77e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789936"
---
# <a name="imediadetput_currentstream-method"></a><span data-ttu-id="d86da-103">IMediaDet: método UT \_ CurrentStream:p</span><span class="sxs-lookup"><span data-stu-id="d86da-103">IMediaDet::put\_CurrentStream method</span></span>

> [!Note]  
> <span data-ttu-id="d86da-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d86da-104">\[Deprecated.</span></span> <span data-ttu-id="d86da-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d86da-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d86da-106">O `put_CurrentStream` método especifica o número de fluxo para o detector de mídia a ser usado.</span><span class="sxs-lookup"><span data-stu-id="d86da-106">The `put_CurrentStream` method specifies the stream number for the media detector to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="d86da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d86da-107">Syntax</span></span>


```C++
HRESULT put_CurrentStream(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="d86da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d86da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d86da-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d86da-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d86da-110">Número do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d86da-110">Stream number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d86da-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d86da-111">Return value</span></span>

<span data-ttu-id="d86da-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d86da-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d86da-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d86da-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d86da-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d86da-114">Remarks</span></span>

<span data-ttu-id="d86da-115">Antes de chamar esse método, chame [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) para definir o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d86da-115">Before calling this method, call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to set the file name.</span></span> <span data-ttu-id="d86da-116">Chame [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para determinar o número de fluxos contidos no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="d86da-116">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to determine the number of streams contained in the source file.</span></span>

<span data-ttu-id="d86da-117">Se o detector de mídia estiver no modo de captura de bitmap, esse método retornará E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d86da-117">If the media detector is in bitmap grab mode, this method returns E\_INVALIDARG.</span></span> <span data-ttu-id="d86da-118">Para obter mais informações, consulte [**IMediaDet:: EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span><span class="sxs-lookup"><span data-stu-id="d86da-118">For more information, see [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).</span></span>

> [!Note]  
> <span data-ttu-id="d86da-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d86da-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d86da-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d86da-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d86da-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d86da-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d86da-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d86da-122">Requirements</span></span>



| <span data-ttu-id="d86da-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d86da-123">Requirement</span></span> | <span data-ttu-id="d86da-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d86da-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d86da-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d86da-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d86da-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d86da-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d86da-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d86da-127">Library</span></span><br/> | <dl> <span data-ttu-id="d86da-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d86da-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d86da-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d86da-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d86da-130">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="d86da-130">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="d86da-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d86da-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




