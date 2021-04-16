---
description: 'O método SetDefaultEffectB define o efeito padrão. Esse método é equivalente a IAMTimeline:: SetDefaultEffect, mas usa um valor BSTR, em vez de um ponteiro para um GUID.'
ms.assetid: ffee9728-f69e-48a4-ac0a-d41347a20deb
title: 'Método IAMTimeline:: SetDefaultEffectB (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultEffectB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a8722a195078cb032285e4ea2ac449ad045d54f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747565"
---
# <a name="iamtimelinesetdefaulteffectb-method"></a><span data-ttu-id="dbc4d-104">Método IAMTimeline:: SetDefaultEffectB</span><span class="sxs-lookup"><span data-stu-id="dbc4d-104">IAMTimeline::SetDefaultEffectB method</span></span>

> [!Note]  
> <span data-ttu-id="dbc4d-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-105">\[Deprecated.</span></span> <span data-ttu-id="dbc4d-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dbc4d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dbc4d-107">O `SetDefaultEffectB` método define o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-107">The `SetDefaultEffectB` method sets the default effect.</span></span> <span data-ttu-id="dbc4d-108">Esse método é equivalente a [**IAMTimeline:: SetDefaultEffect**](iamtimeline-setdefaulteffect.md), mas usa um valor BSTR, em vez de um ponteiro para um GUID.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-108">This method is equivalent to [**IAMTimeline::SetDefaultEffect**](iamtimeline-setdefaulteffect.md), but takes a BSTR value, rather than a pointer to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbc4d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dbc4d-109">Syntax</span></span>


```C++
HRESULT SetDefaultEffectB(
   BSTR pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="dbc4d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbc4d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc4d-111">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="dbc4d-111">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="dbc4d-112">Valor BSTR que representa o GUID do efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-112">BSTR value representing the GUID of the default effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc4d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbc4d-113">Return value</span></span>

<span data-ttu-id="dbc4d-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dbc4d-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dbc4d-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc4d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbc4d-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dbc4d-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dbc4d-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dbc4d-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dbc4d-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dbc4d-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dbc4d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc4d-120">Requirements</span></span>



| <span data-ttu-id="dbc4d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc4d-121">Requirement</span></span> | <span data-ttu-id="dbc4d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc4d-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc4d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbc4d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="dbc4d-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc4d-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dbc4d-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dbc4d-125">Library</span></span><br/> | <dl> <span data-ttu-id="dbc4d-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbc4d-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc4d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc4d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc4d-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="dbc4d-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="dbc4d-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="dbc4d-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




