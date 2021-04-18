---
description: O \_ método Put OffsetY especifica o deslocamento vertical da origem do apagamento.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: 'IDxtJpeg: método de ut_OffsetY de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f68a18d01acf519032bce31c28515bc7ac81c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758673"
---
# <a name="idxtjpegput_offsety-method"></a><span data-ttu-id="20500-103">IDxtJpeg: método UT \_ OffsetY:p</span><span class="sxs-lookup"><span data-stu-id="20500-103">IDxtJpeg::put\_OffsetY method</span></span>

> [!Note]  
> <span data-ttu-id="20500-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="20500-104">\[Deprecated.</span></span> <span data-ttu-id="20500-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="20500-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="20500-106">O `put_OffsetY` método especifica o deslocamento vertical da origem do apagamento.</span><span class="sxs-lookup"><span data-stu-id="20500-106">The `put_OffsetY` method specifies the vertical offset of the wipe origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="20500-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20500-107">Syntax</span></span>


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="20500-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20500-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20500-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="20500-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20500-110">O deslocamento vertical da origem do apagamento, em pixels.</span><span class="sxs-lookup"><span data-stu-id="20500-110">The vertical offset of the wipe origin, in pixels.</span></span> <span data-ttu-id="20500-111">O centro do apagamento é deslocado por esse valor.</span><span class="sxs-lookup"><span data-stu-id="20500-111">The center of the wipe is offset by this amount.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20500-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="20500-112">Return value</span></span>

<span data-ttu-id="20500-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="20500-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20500-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20500-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20500-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="20500-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="20500-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="20500-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="20500-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="20500-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="20500-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="20500-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20500-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20500-119">Requirements</span></span>



| <span data-ttu-id="20500-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="20500-120">Requirement</span></span> | <span data-ttu-id="20500-121">Valor</span><span class="sxs-lookup"><span data-stu-id="20500-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20500-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20500-122">Header</span></span><br/>  | <dl> <span data-ttu-id="20500-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="20500-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="20500-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20500-124">Library</span></span><br/> | <dl> <span data-ttu-id="20500-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="20500-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20500-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="20500-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20500-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="20500-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




