---
description: O método GetDefaultTransition recupera a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.
ms.assetid: 3fe5d984-480b-4b35-970f-2f571e0fde7d
title: 'Método IAMTimeline:: GetDefaultTransition (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f594c0c0be10f93d0e90997df53074a9e69aec6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750272"
---
# <a name="iamtimelinegetdefaulttransition-method"></a><span data-ttu-id="70e52-104">Método IAMTimeline:: GetDefaultTransition</span><span class="sxs-lookup"><span data-stu-id="70e52-104">IAMTimeline::GetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="70e52-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="70e52-105">\[Deprecated.</span></span> <span data-ttu-id="70e52-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70e52-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70e52-107">O `GetDefaultTransition` método recupera a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="70e52-107">The `GetDefaultTransition` method retrieves the default transition.</span></span> <span data-ttu-id="70e52-108">Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="70e52-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e52-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="70e52-109">Syntax</span></span>


```C++
HRESULT GetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="70e52-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70e52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e52-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="70e52-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="70e52-112">Recebe o GUID da transição padrão.</span><span class="sxs-lookup"><span data-stu-id="70e52-112">Receives the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e52-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70e52-113">Return value</span></span>

<span data-ttu-id="70e52-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="70e52-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70e52-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70e52-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70e52-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="70e52-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70e52-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="70e52-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70e52-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="70e52-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70e52-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="70e52-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70e52-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70e52-120">Requirements</span></span>



| <span data-ttu-id="70e52-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e52-121">Requirement</span></span> | <span data-ttu-id="70e52-122">Valor</span><span class="sxs-lookup"><span data-stu-id="70e52-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70e52-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70e52-123">Header</span></span><br/>  | <dl> <span data-ttu-id="70e52-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e52-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70e52-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70e52-125">Library</span></span><br/> | <dl> <span data-ttu-id="70e52-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70e52-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70e52-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="70e52-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e52-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="70e52-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="70e52-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="70e52-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




