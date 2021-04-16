---
description: O método SetDefaultTransition define a transição padrão. Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.
ms.assetid: 5ee84a12-402f-4f1c-9f08-206431c7ecdb
title: 'Método IAMTimeline:: SetDefaultTransition (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultTransition
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: eeea5563ca9a2548507d3b4333d857d7cc156dd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757888"
---
# <a name="iamtimelinesetdefaulttransition-method"></a><span data-ttu-id="9e372-104">Método IAMTimeline:: SetDefaultTransition</span><span class="sxs-lookup"><span data-stu-id="9e372-104">IAMTimeline::SetDefaultTransition method</span></span>

> [!Note]  
> <span data-ttu-id="9e372-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9e372-105">\[Deprecated.</span></span> <span data-ttu-id="9e372-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e372-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9e372-107">O `SetDefaultTransition` método define a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="9e372-107">The `SetDefaultTransition` method sets the default transition.</span></span> <span data-ttu-id="9e372-108">Se o mecanismo de renderização não puder renderizar uma transição, ele substituirá a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="9e372-108">If the render engine cannot render a transition, it substitutes the default transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e372-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e372-109">Syntax</span></span>


```C++
HRESULT SetDefaultTransition(
   GUID *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="9e372-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e372-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e372-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="9e372-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="9e372-112">Ponteiro para uma variável que contém o GUID da transição padrão.</span><span class="sxs-lookup"><span data-stu-id="9e372-112">Pointer to a variable that contains the GUID of the default transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e372-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e372-113">Return value</span></span>

<span data-ttu-id="9e372-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9e372-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e372-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9e372-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e372-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e372-116">Remarks</span></span>

<span data-ttu-id="9e372-117">Se você não definir uma transição padrão ou se a transição que você especificar como padrão causar um erro, o DES usará sua própria transição padrão.</span><span class="sxs-lookup"><span data-stu-id="9e372-117">If you do not set a default transition, or if the transition that you specify as a default causes an error, DES uses its own default transition.</span></span>

> [!Note]  
> <span data-ttu-id="9e372-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9e372-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9e372-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9e372-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9e372-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9e372-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9e372-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e372-121">Requirements</span></span>



| <span data-ttu-id="9e372-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e372-122">Requirement</span></span> | <span data-ttu-id="9e372-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9e372-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e372-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e372-124">Header</span></span><br/>  | <dl> <span data-ttu-id="9e372-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e372-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9e372-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e372-126">Library</span></span><br/> | <dl> <span data-ttu-id="9e372-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e372-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e372-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e372-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e372-129">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="9e372-129">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="9e372-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="9e372-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




