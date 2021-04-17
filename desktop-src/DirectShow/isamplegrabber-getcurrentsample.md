---
description: O método GetCurrentSample não está implementado.
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: 'Método ISampleGrabber:: GetCurrentSample (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a21f50f84f030502cfd3243d36595e465e1b85b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759496"
---
# <a name="isamplegrabbergetcurrentsample-method"></a><span data-ttu-id="c7dab-103">Método ISampleGrabber:: GetCurrentSample</span><span class="sxs-lookup"><span data-stu-id="c7dab-103">ISampleGrabber::GetCurrentSample method</span></span>

> [!Note]  
> <span data-ttu-id="c7dab-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c7dab-104">\[Deprecated.</span></span> <span data-ttu-id="c7dab-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7dab-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7dab-106">O método `GetCurrentSample` não está implementado.</span><span class="sxs-lookup"><span data-stu-id="c7dab-106">The `GetCurrentSample` method is not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7dab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c7dab-107">Syntax</span></span>


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a><span data-ttu-id="c7dab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7dab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7dab-109">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="c7dab-109">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c7dab-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="c7dab-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7dab-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7dab-111">Return value</span></span>

<span data-ttu-id="c7dab-112">Retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c7dab-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7dab-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7dab-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c7dab-114">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c7dab-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7dab-115">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c7dab-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c7dab-116">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c7dab-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7dab-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7dab-117">Requirements</span></span>



| <span data-ttu-id="c7dab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7dab-118">Requirement</span></span> | <span data-ttu-id="c7dab-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c7dab-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7dab-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7dab-120">Header</span></span><br/>  | <dl> <span data-ttu-id="c7dab-121"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7dab-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c7dab-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7dab-122">Library</span></span><br/> | <dl> <span data-ttu-id="c7dab-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7dab-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7dab-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7dab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7dab-125">Usando o exemplo de apoio</span><span class="sxs-lookup"><span data-stu-id="c7dab-125">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="c7dab-126">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="c7dab-126">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




