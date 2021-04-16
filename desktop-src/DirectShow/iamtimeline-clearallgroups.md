---
description: O método ClearAllGroups remove todos os grupos da linha do tempo, juntamente com todos os objetos contidos nesses grupos.
ms.assetid: b0d2a463-bd18-4377-893c-ea4fdf77b1c8
title: 'Método IAMTimeline:: ClearAllGroups (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ClearAllGroups
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 05d847bdae9d6f5f5672d555a31505c2739af41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752475"
---
# <a name="iamtimelineclearallgroups-method"></a><span data-ttu-id="ab8be-103">Método IAMTimeline:: ClearAllGroups</span><span class="sxs-lookup"><span data-stu-id="ab8be-103">IAMTimeline::ClearAllGroups method</span></span>

> [!Note]  
> <span data-ttu-id="ab8be-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ab8be-104">\[Deprecated.</span></span> <span data-ttu-id="ab8be-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ab8be-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ab8be-106">O `ClearAllGroups` método remove todos os grupos da linha do tempo, juntamente com todos os objetos contidos nesses grupos.</span><span class="sxs-lookup"><span data-stu-id="ab8be-106">The `ClearAllGroups` method removes all groups from the timeline, along with all objects contained in those groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab8be-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab8be-107">Syntax</span></span>


```C++
HRESULT ClearAllGroups();
```



## <a name="parameters"></a><span data-ttu-id="ab8be-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab8be-108">Parameters</span></span>

<span data-ttu-id="ab8be-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ab8be-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab8be-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab8be-110">Return value</span></span>

<span data-ttu-id="ab8be-111">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ab8be-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab8be-112">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ab8be-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab8be-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab8be-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ab8be-114">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ab8be-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ab8be-115">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ab8be-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ab8be-116">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ab8be-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ab8be-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab8be-117">Requirements</span></span>



| <span data-ttu-id="ab8be-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab8be-118">Requirement</span></span> | <span data-ttu-id="ab8be-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ab8be-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab8be-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab8be-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ab8be-121"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab8be-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ab8be-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab8be-122">Library</span></span><br/> | <dl> <span data-ttu-id="ab8be-123"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab8be-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab8be-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab8be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab8be-125">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="ab8be-125">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="ab8be-126">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ab8be-126">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




