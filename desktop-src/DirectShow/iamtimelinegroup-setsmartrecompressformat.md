---
description: O método SetSmartRecompressFormat especifica um formato de compactação de vídeo a ser usado para a recompactação inteligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'Método IAMTimelineGroup:: SetSmartRecompressFormat (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810400"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="d1747-103">Método IAMTimelineGroup:: SetSmartRecompressFormat</span><span class="sxs-lookup"><span data-stu-id="d1747-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="d1747-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d1747-104">\[Deprecated.</span></span> <span data-ttu-id="d1747-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1747-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d1747-106">O `SetSmartRecompressFormat` método especifica um formato de compactação de vídeo a ser usado para a recompactação inteligente.</span><span class="sxs-lookup"><span data-stu-id="d1747-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="d1747-107">A recompactação inteligente não tem suporte para grupos de áudio.</span><span class="sxs-lookup"><span data-stu-id="d1747-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1747-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1747-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d1747-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1747-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1747-110">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="d1747-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d1747-111">Ponteiro para uma estrutura que descreve o formato de compactação.</span><span class="sxs-lookup"><span data-stu-id="d1747-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="d1747-112">Atualmente, apenas a estrutura [**SCompFmt0**](scompfmt0.md) é válida.</span><span class="sxs-lookup"><span data-stu-id="d1747-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="d1747-113">Você deve converter esse parâmetro para um ponteiro do tipo **Long**.</span><span class="sxs-lookup"><span data-stu-id="d1747-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1747-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1747-114">Return value</span></span>

<span data-ttu-id="d1747-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d1747-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1747-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d1747-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1747-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1747-117">Remarks</span></span>

<span data-ttu-id="d1747-118">Antes de chamar esse método, chame o método [**IAMTimelineGroup:: SetMediaType**](iamtimelinegroup-setmediatype.md) no mesmo grupo, para especificar um formato descompactado.</span><span class="sxs-lookup"><span data-stu-id="d1747-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="d1747-119">Se o `SetSmartRecompressFormat` método tiver sucesso, você poderá usar o mecanismo de processamento inteligente para gerar um fluxo de vídeo compactado.</span><span class="sxs-lookup"><span data-stu-id="d1747-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="d1747-120">O vídeo compactado terá a largura, a altura e a taxa de quadros que foi especificada no parâmetro *pFormat* .</span><span class="sxs-lookup"><span data-stu-id="d1747-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="d1747-121">Esses valores substituirão aqueles fornecidos para o formato descompactado no método **SetMediaType** .</span><span class="sxs-lookup"><span data-stu-id="d1747-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="d1747-122">No entanto, para obter os benefícios da recompactação inteligente, os dois formatos devem corresponder.</span><span class="sxs-lookup"><span data-stu-id="d1747-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="d1747-123">Em outras palavras, os formatos compactados e descompactados devem ter a mesma altura, largura e taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="d1747-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="d1747-124">Se o mecanismo de processamento inteligente não puder produzir o formato compactado, ele produzirá um fluxo de vídeo não compactado.</span><span class="sxs-lookup"><span data-stu-id="d1747-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="d1747-125">Se isso ocorrer, o mecanismo de processamento inteligente relata que as IDs do DEX não \_ \_ \_ encontrarão \_ erro de renderização de compressor durante o método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="d1747-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="d1747-126">O aplicativo pode capturar esse erro por meio do método [**IAMErrorLog:: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="d1747-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="d1747-127">(Para obter mais informações, consulte [registrando](logging-errors.md) erros e [erros de renderização](rendering-errors.md).)</span><span class="sxs-lookup"><span data-stu-id="d1747-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="d1747-128">O formato de recompactação inteligente não é persistente.</span><span class="sxs-lookup"><span data-stu-id="d1747-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="d1747-129">Se um aplicativo usar a recompactação inteligente, ele deverá definir o formato de recompactação sempre que carregar um arquivo de projeto.</span><span class="sxs-lookup"><span data-stu-id="d1747-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="d1747-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d1747-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d1747-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d1747-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d1747-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d1747-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d1747-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1747-133">Requirements</span></span>



| <span data-ttu-id="d1747-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1747-134">Requirement</span></span> | <span data-ttu-id="d1747-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d1747-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1747-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1747-136">Header</span></span><br/>  | <dl> <span data-ttu-id="d1747-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1747-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d1747-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1747-138">Library</span></span><br/> | <dl> <span data-ttu-id="d1747-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1747-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1747-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1747-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1747-141">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="d1747-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="d1747-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d1747-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="d1747-143">Mecanismo de processamento inteligente</span><span class="sxs-lookup"><span data-stu-id="d1747-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="d1747-144">Gravando um projeto em um arquivo</span><span class="sxs-lookup"><span data-stu-id="d1747-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




