---
description: O método setstretchmode define o modo de ampliação. O modo de ampliação determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.
ms.assetid: 4f720975-5035-4539-895f-3eb3c3b31719
title: 'Método IAMTimelineSrc:: setstretchmode (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStretchMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2fae71362f6e09d2eae6c2cdf574a2fbda43930b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761759"
---
# <a name="iamtimelinesrcsetstretchmode-method"></a><span data-ttu-id="93bda-104">Método IAMTimelineSrc:: setstretchmode</span><span class="sxs-lookup"><span data-stu-id="93bda-104">IAMTimelineSrc::SetStretchMode method</span></span>

> [!Note]  
> <span data-ttu-id="93bda-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="93bda-105">\[Deprecated.</span></span> <span data-ttu-id="93bda-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="93bda-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="93bda-107">O `SetStretchMode` método define o modo Stretch.</span><span class="sxs-lookup"><span data-stu-id="93bda-107">The `SetStretchMode` method sets the stretch mode.</span></span> <span data-ttu-id="93bda-108">O modo de ampliação determina como uma fonte de vídeo será renderizada se seu tamanho não corresponder às dimensões de saída.</span><span class="sxs-lookup"><span data-stu-id="93bda-108">The stretch mode determines how a video source is rendered if its size does not match the output dimensions.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bda-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93bda-109">Syntax</span></span>


```C++
HRESULT SetStretchMode(
   int nStretchMode
);
```



## <a name="parameters"></a><span data-ttu-id="93bda-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93bda-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bda-111">*nStretchMode*</span><span class="sxs-lookup"><span data-stu-id="93bda-111">*nStretchMode*</span></span> 
</dt> <dd>

<span data-ttu-id="93bda-112">Sinalizador que indica o modo de Stretch atual.</span><span class="sxs-lookup"><span data-stu-id="93bda-112">Flag indicating the current stretch mode.</span></span> <span data-ttu-id="93bda-113">Para obter uma lista de valores possíveis, consulte [**redimensionar sinalizadores**](resize-flags.md).</span><span class="sxs-lookup"><span data-stu-id="93bda-113">For a list of possible values, see [**Resize Flags**](resize-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bda-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93bda-114">Return value</span></span>

<span data-ttu-id="93bda-115">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="93bda-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="93bda-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="93bda-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="93bda-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="93bda-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="93bda-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="93bda-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="93bda-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="93bda-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93bda-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93bda-120">Requirements</span></span>



| <span data-ttu-id="93bda-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="93bda-121">Requirement</span></span> | <span data-ttu-id="93bda-122">Valor</span><span class="sxs-lookup"><span data-stu-id="93bda-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93bda-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93bda-123">Header</span></span><br/>  | <dl> <span data-ttu-id="93bda-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="93bda-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="93bda-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93bda-125">Library</span></span><br/> | <dl> <span data-ttu-id="93bda-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="93bda-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93bda-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="93bda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bda-128">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="93bda-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="93bda-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="93bda-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




