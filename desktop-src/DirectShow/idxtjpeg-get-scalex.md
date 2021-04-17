---
description: O \_ método Get ScaleX recupera o valor pelo qual o apagamento é alongado horizontalmente.
ms.assetid: 74c3f60b-68d9-4a8e-a6e5-767ce281a9fb
title: 'Método IDxtJpeg:: get_ScaleX (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0532e3c068c0ea9641d1fffbcc3d1327290bae02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812821"
---
# <a name="idxtjpegget_scalex-method"></a><span data-ttu-id="ef107-103">Método IDxtJpeg:: get \_ ScaleX</span><span class="sxs-lookup"><span data-stu-id="ef107-103">IDxtJpeg::get\_ScaleX method</span></span>

> [!Note]  
> <span data-ttu-id="ef107-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ef107-104">\[Deprecated.</span></span> <span data-ttu-id="ef107-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef107-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ef107-106">O `get_ScaleX` método recupera a quantidade pela qual o apagamento é alongado horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="ef107-106">The `get_ScaleX` method retrieves the amount by which the wipe is stretched horizontally.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef107-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef107-107">Syntax</span></span>


```C++
HRESULT get_ScaleX(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="ef107-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef107-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef107-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ef107-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ef107-110">Recebe o valor pelo qual o apagamento é alongado horizontalmente, como uma porcentagem da definição de apagamento original.</span><span class="sxs-lookup"><span data-stu-id="ef107-110">Receives the amount by which the wipe is stretched horizontally, as a percentage of the original wipe definition.</span></span> <span data-ttu-id="ef107-111">Por exemplo, o valor 1,0 significa sem alargamento e 2,0 significa 200% de alongamento.</span><span class="sxs-lookup"><span data-stu-id="ef107-111">For example, the value 1.0 means no stretching, and 2.0 means 200% stretching.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef107-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ef107-112">Return value</span></span>

<span data-ttu-id="ef107-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ef107-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef107-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef107-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef107-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef107-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ef107-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ef107-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef107-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ef107-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ef107-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ef107-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ef107-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef107-119">Requirements</span></span>



| <span data-ttu-id="ef107-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef107-120">Requirement</span></span> | <span data-ttu-id="ef107-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ef107-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef107-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef107-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ef107-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef107-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ef107-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef107-124">Library</span></span><br/> | <dl> <span data-ttu-id="ef107-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef107-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef107-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef107-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef107-127">**Interface IDxtJpeg**</span><span class="sxs-lookup"><span data-stu-id="ef107-127">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




