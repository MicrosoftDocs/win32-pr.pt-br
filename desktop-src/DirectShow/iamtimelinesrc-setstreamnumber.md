---
description: O método SetStreamNumber especifica qual fluxo deve ser lido do arquivo de origem associado a esse objeto de origem.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: 'Método IAMTimelineSrc:: SetStreamNumber (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 32deec91d4ae0fe55b4574344dd357932856db81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784024"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a><span data-ttu-id="e7605-103">Método IAMTimelineSrc:: SetStreamNumber</span><span class="sxs-lookup"><span data-stu-id="e7605-103">IAMTimelineSrc::SetStreamNumber method</span></span>

> [!Note]  
> <span data-ttu-id="e7605-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="e7605-104">\[Deprecated.</span></span> <span data-ttu-id="e7605-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7605-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7605-106">O `SetStreamNumber` método especifica qual fluxo deve ser lido do arquivo de origem associado a esse objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="e7605-106">The `SetStreamNumber` method specifies which stream to read from the source file associated with this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7605-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7605-107">Syntax</span></span>


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a><span data-ttu-id="e7605-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7605-109">*Val*</span><span class="sxs-lookup"><span data-stu-id="e7605-109">*Val*</span></span> 
</dt> <dd>

<span data-ttu-id="e7605-110">O número do fluxo, do conjunto de fluxos que correspondem ao tipo de mídia do grupo pai.</span><span class="sxs-lookup"><span data-stu-id="e7605-110">The stream number, from the set of streams matching the media type of the parent group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7605-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7605-111">Return value</span></span>

<span data-ttu-id="e7605-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7605-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7605-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7605-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7605-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7605-114">Remarks</span></span>

<span data-ttu-id="e7605-115">O parâmetro *Val* especifica um número de fluxo do conjunto de fluxos que corresponde ao tipo de mídia do grupo pai, não de todo o conjunto de fluxos no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="e7605-115">The *Val* parameter specifies a stream number from the set of streams that matches the parent group's media type, not from the entire set of streams in the source file.</span></span> <span data-ttu-id="e7605-116">Por exemplo, por exemplo, suponha que um arquivo contenha dois fluxos de vídeo e dois fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="e7605-116">For example, For example, suppose that a file contains two video streams and two audio streams.</span></span> <span data-ttu-id="e7605-117">Se o objeto de origem estiver dentro de um grupo de vídeos, a definição de *Val* como 0 selecionará o primeiro fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7605-117">If the source object is inside a video group, setting *Val* to 0 selects the first video stream.</span></span> <span data-ttu-id="e7605-118">O chamador é responsável por especificar um número de fluxo válido.</span><span class="sxs-lookup"><span data-stu-id="e7605-118">The caller is responsible for specifying a valid stream number.</span></span>

<span data-ttu-id="e7605-119">O número do fluxo assume como padrão zero.</span><span class="sxs-lookup"><span data-stu-id="e7605-119">The stream number defaults to zero.</span></span>

> [!Note]  
> <span data-ttu-id="e7605-120">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="e7605-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7605-121">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e7605-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7605-122">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e7605-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7605-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7605-123">Requirements</span></span>



| <span data-ttu-id="e7605-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7605-124">Requirement</span></span> | <span data-ttu-id="e7605-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e7605-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7605-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7605-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e7605-127"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7605-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7605-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7605-128">Library</span></span><br/> | <dl> <span data-ttu-id="e7605-129"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7605-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7605-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7605-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7605-131">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="e7605-131">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="e7605-132">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="e7605-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




