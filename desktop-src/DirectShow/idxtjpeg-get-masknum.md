---
description: O \_ método Get MaskNum recupera o código de apagamento SMPTE do apagamento.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Método IDxtJpeg:: get_MaskNum (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 869809fdea6e1c329088abca50a1670239554327
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757677"
---
# <a name="idxtjpegget_masknum-method"></a><span data-ttu-id="73010-103">Método IDxtJpeg:: get \_ MaskNum</span><span class="sxs-lookup"><span data-stu-id="73010-103">IDxtJpeg::get\_MaskNum method</span></span>

> [!Note]  
> <span data-ttu-id="73010-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="73010-104">\[Deprecated.</span></span> <span data-ttu-id="73010-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73010-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="73010-106">O `get_MaskNum` método recupera o código de apagamento SMPTE do apagamento.</span><span class="sxs-lookup"><span data-stu-id="73010-106">The `get_MaskNum` method retrieves the SMPTE wipe code of the wipe.</span></span>

## <a name="syntax"></a><span data-ttu-id="73010-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73010-107">Syntax</span></span>


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="73010-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73010-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73010-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="73010-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="73010-110">Recebe o código de apagamento SMPTE.</span><span class="sxs-lookup"><span data-stu-id="73010-110">Receives the SMPTE wipe code.</span></span> <span data-ttu-id="73010-111">Para obter uma lista de apagamentos SMPTE com suporte, consulte [transição de apagamento SMPTE](smpte-wipe-transition.md).</span><span class="sxs-lookup"><span data-stu-id="73010-111">For a list of supported SMPTE wipes, see [SMPTE Wipe Transition](smpte-wipe-transition.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73010-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73010-112">Return value</span></span>

<span data-ttu-id="73010-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73010-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73010-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73010-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73010-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="73010-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="73010-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="73010-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="73010-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="73010-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="73010-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="73010-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="73010-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73010-119">Requirements</span></span>



| <span data-ttu-id="73010-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="73010-120">Requirement</span></span> | <span data-ttu-id="73010-121">Valor</span><span class="sxs-lookup"><span data-stu-id="73010-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73010-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73010-122">Header</span></span><br/>  | <dl> <span data-ttu-id="73010-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="73010-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="73010-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73010-124">Library</span></span><br/> | <dl> <span data-ttu-id="73010-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="73010-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73010-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="73010-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73010-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="73010-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




