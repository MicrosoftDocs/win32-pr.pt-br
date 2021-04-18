---
description: O método GetDefaultFPS recupera a taxa de quadros padrão do objeto de origem. O mecanismo de renderização usa esse valor se ele não puder determinar a taxa de quadros a partir da origem original.
ms.assetid: c167cd85-e9bb-46ff-9b35-c88898a6c5a3
title: 'Método IAMTimelineSrc:: GetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e48ee38f385ba5ff06b2ede9b27b4558dac65270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810394"
---
# <a name="iamtimelinesrcgetdefaultfps-method"></a><span data-ttu-id="387b1-104">Método IAMTimelineSrc:: GetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="387b1-104">IAMTimelineSrc::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="387b1-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="387b1-105">\[Deprecated.</span></span> <span data-ttu-id="387b1-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="387b1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="387b1-107">O `GetDefaultFPS` método recupera a taxa de quadros padrão do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="387b1-107">The `GetDefaultFPS` method retrieves the source object's default frame rate.</span></span> <span data-ttu-id="387b1-108">O mecanismo de renderização usa esse valor se ele não puder determinar a taxa de quadros a partir da origem original.</span><span class="sxs-lookup"><span data-stu-id="387b1-108">The render engine uses this value if it cannot determine the frame rate from the original source.</span></span>

## <a name="syntax"></a><span data-ttu-id="387b1-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="387b1-109">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="387b1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="387b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387b1-111">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="387b1-111">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="387b1-112">Recebe a taxa de quadros padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="387b1-112">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387b1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="387b1-113">Return value</span></span>

<span data-ttu-id="387b1-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="387b1-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="387b1-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="387b1-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="387b1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="387b1-116">Remarks</span></span>

<span data-ttu-id="387b1-117">A taxa de quadros padrão não será necessária se o formato de arquivo especificar a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="387b1-117">The default frame rate is not required if the file format specifies the frame rate.</span></span> <span data-ttu-id="387b1-118">Esse é o caso de formatos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="387b1-118">This is the case for audio and video formats.</span></span>

<span data-ttu-id="387b1-119">Se a origem for um bitmap ou uma imagem JPEG, o mecanismo de renderização o usará como a primeira imagem em uma sequência de DIB (bitmap independente de dispositivo), com uma taxa de quadros igual à taxa de quadros padrão.</span><span class="sxs-lookup"><span data-stu-id="387b1-119">If the source is a bitmap or JPEG image, the render engine uses it as the first image in a device-independent bitmap (DIB) sequence, with a frame rate equal to the default frame rate.</span></span> <span data-ttu-id="387b1-120">Para renderizar uma imagem estática, em vez de uma sequência DIB, defina a taxa de quadros padrão como 0.</span><span class="sxs-lookup"><span data-stu-id="387b1-120">To render a static image, rather than a DIB sequence, set the default frame rate to 0.</span></span>

<span data-ttu-id="387b1-121">Se a origem for um GIF, não defina a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="387b1-121">If the source is a GIF, do not set the frame rate.</span></span> <span data-ttu-id="387b1-122">Para GIFs animados, o arquivo GIF especifica o atraso entre cada imagem.</span><span class="sxs-lookup"><span data-stu-id="387b1-122">For animated GIFs, the GIF file specifies the delay between each image.</span></span>

> [!Note]  
> <span data-ttu-id="387b1-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="387b1-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="387b1-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="387b1-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="387b1-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="387b1-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="387b1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="387b1-126">Requirements</span></span>



| <span data-ttu-id="387b1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="387b1-127">Requirement</span></span> | <span data-ttu-id="387b1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="387b1-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="387b1-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="387b1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="387b1-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="387b1-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="387b1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="387b1-131">Library</span></span><br/> | <dl> <span data-ttu-id="387b1-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="387b1-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="387b1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="387b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="387b1-134">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="387b1-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="387b1-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="387b1-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




