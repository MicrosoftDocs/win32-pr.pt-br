---
description: O \_ método Put ScaleX especifica a quantidade pela qual o apagamento é alongado horizontalmente.
ms.assetid: d57af5dc-41e0-45a7-8f11-55ef3bc62549
title: 'IDxtJpeg: método de ut_ScaleX de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fff0583ce3163ebf5626cfdbb82edf5c927bdc9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810220"
---
# <a name="idxtjpegput_scalex-method"></a><span data-ttu-id="4e3d8-103">Método IDxtJpeg::p UT \_ ScaleX</span><span class="sxs-lookup"><span data-stu-id="4e3d8-103">IDxtJpeg::put\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="4e3d8-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-104">\[Deprecated.</span></span> <span data-ttu-id="4e3d8-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e3d8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4e3d8-106">O `put_ScaleX` método especifica a quantidade pela qual o apagamento é alongado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-106">The `put_ScaleX` method specifies the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e3d8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e3d8-107">Syntax</span></span>


```C++
HRESULT put_ScaleX(
  [in] double newVal
);
```



## <a name="parameters"></a><span data-ttu-id="4e3d8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e3d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e3d8-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4e3d8-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e3d8-110">O valor pelo qual o apagamento é alongado horizontalmente, como uma porcentagem da definição de apagamento original.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-110">The amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="4e3d8-111">Por exemplo, o valor 1,0 significa sem alargamento e 2,0 significa 200% de alongamento.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e3d8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4e3d8-112">Return value</span></span>

<span data-ttu-id="4e3d8-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4e3d8-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e3d8-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e3d8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e3d8-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e3d8-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4e3d8-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e3d8-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4e3d8-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4e3d8-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4e3d8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e3d8-119">Requirements</span></span>



| <span data-ttu-id="4e3d8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e3d8-120">Requirement</span></span> | <span data-ttu-id="4e3d8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4e3d8-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e3d8-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4e3d8-122">Header</span></span><br/>  | <dl> <span data-ttu-id="4e3d8-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e3d8-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4e3d8-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e3d8-124">Library</span></span><br/> | <dl> <span data-ttu-id="4e3d8-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e3d8-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e3d8-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e3d8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e3d8-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="4e3d8-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




