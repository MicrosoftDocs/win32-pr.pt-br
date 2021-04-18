---
description: O método WriteBitmapBits recupera um quadro de vídeo no tempo de mídia especificado e o grava em um arquivo. O quadro de vídeo está sempre no formato RGB de 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'Método IMediaDet:: WriteBitmapBits (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766992"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="0c7a6-104">Método IMediaDet:: WriteBitmapBits</span><span class="sxs-lookup"><span data-stu-id="0c7a6-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="0c7a6-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-105">\[Deprecated.</span></span> <span data-ttu-id="0c7a6-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0c7a6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0c7a6-107">O `WriteBitmapBits` método recupera um quadro de vídeo no tempo de mídia especificado e o grava em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="0c7a6-108">O quadro de vídeo está sempre no formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7a6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c7a6-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="0c7a6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c7a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c7a6-111">*Fluxo de transmissão*</span><span class="sxs-lookup"><span data-stu-id="0c7a6-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0c7a6-112">Hora em que o quadro de vídeo será recuperado.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="0c7a6-113">*Largura*</span><span class="sxs-lookup"><span data-stu-id="0c7a6-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="0c7a6-114">Largura da imagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0c7a6-115">*Altura*</span><span class="sxs-lookup"><span data-stu-id="0c7a6-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="0c7a6-116">Altura da imagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="0c7a6-117">*Filename*</span><span class="sxs-lookup"><span data-stu-id="0c7a6-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="0c7a6-118">Caminho do arquivo no qual salvar o bitmap.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="0c7a6-119">Se o arquivo já existir, esse método o substituirá.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c7a6-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0c7a6-120">Return value</span></span>

<span data-ttu-id="0c7a6-121">Retorna S \_ OK com êxito.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="0c7a6-122">Caso contrário, retorna um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="0c7a6-123">Os códigos de erro possíveis incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0c7a6-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="0c7a6-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0c7a6-124">Return code</span></span>                                                                                             | <span data-ttu-id="0c7a6-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c7a6-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c7a6-126"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="0c7a6-127">Não foi possível adicionar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ao grafo.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="0c7a6-128"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="0c7a6-129">Falha.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="0c7a6-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="0c7a6-131">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="0c7a6-132"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="0c7a6-133">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="0c7a6-134"><dt>**STG \_ E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="0c7a6-135">Não é possível substituir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="0c7a6-136"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="0c7a6-137">Tipo de mídia inválido.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0c7a6-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c7a6-138">Remarks</span></span>

<span data-ttu-id="0c7a6-139">Antes de chamar esse método, defina o nome do arquivo e o fluxo chamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="0c7a6-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="0c7a6-140">Esse método coloca o detector de mídia no modo de captura de bitmap.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="0c7a6-141">Depois que esse método for chamado, os vários métodos de informações de fluxo no **IMediaDet** não funcionarão, a menos que você crie uma nova instância do detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="0c7a6-142">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0c7a6-143">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0c7a6-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0c7a6-144">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0c7a6-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0c7a6-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c7a6-145">Requirements</span></span>



| <span data-ttu-id="0c7a6-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c7a6-146">Requirement</span></span> | <span data-ttu-id="0c7a6-147">Valor</span><span class="sxs-lookup"><span data-stu-id="0c7a6-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7a6-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c7a6-148">Header</span></span><br/>  | <dl> <span data-ttu-id="0c7a6-149"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0c7a6-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c7a6-150">Library</span></span><br/> | <dl> <span data-ttu-id="0c7a6-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c7a6-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c7a6-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c7a6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7a6-153">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="0c7a6-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="0c7a6-154">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="0c7a6-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




