---
description: O \_ método Put MaskNum especifica o código de apagamento SMPTE do apagamento.
ms.assetid: d2d2382c-d920-49e7-b9b7-6897356a78de
title: 'IDxtJpeg: método de ut_MaskNum de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f814fab2654a5585567273301dab285c32a1019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789937"
---
# <a name="idxtjpegput_masknum-method"></a><span data-ttu-id="11b37-103">IDxtJpeg: método UT \_ MaskNum:p</span><span class="sxs-lookup"><span data-stu-id="11b37-103">IDxtJpeg::put\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="11b37-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="11b37-104">\[Deprecated.</span></span> <span data-ttu-id="11b37-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11b37-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="11b37-106">O `put_MaskNum` método especifica o código de apagamento SMPTE do apagamento.</span><span class="sxs-lookup"><span data-stu-id="11b37-106">The `put_MaskNum` method specifies the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b37-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11b37-107">Syntax</span></span>


```C++
HRESULT put_MaskNum(
  [in] long newVal
);
```



## <a name="parameters"></a><span data-ttu-id="11b37-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11b37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11b37-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11b37-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b37-110">Especifica o código de apagamento SMPTE.</span><span class="sxs-lookup"><span data-stu-id="11b37-110">Specifies the SMPTE wipe code.</span></span> <span data-ttu-id="11b37-111">Para obter uma lista de apagamentos SMPTE com suporte, consulte [transição de apagamento SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="11b37-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11b37-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11b37-112">Return value</span></span>

<span data-ttu-id="11b37-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="11b37-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="11b37-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="11b37-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="11b37-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="11b37-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="11b37-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="11b37-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="11b37-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="11b37-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="11b37-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="11b37-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="11b37-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11b37-119">Requirements</span></span>



| <span data-ttu-id="11b37-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11b37-120">Requirement</span></span> | <span data-ttu-id="11b37-121">Valor</span><span class="sxs-lookup"><span data-stu-id="11b37-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11b37-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11b37-122">Header</span></span><br/>  | <dl> <span data-ttu-id="11b37-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="11b37-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="11b37-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11b37-124">Library</span></span><br/> | <dl> <span data-ttu-id="11b37-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11b37-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11b37-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="11b37-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b37-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="11b37-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




