---
description: O método EffectsEnabled determina se os efeitos estão habilitados. Se os efeitos estiverem desabilitados, eles permanecerão na linha do tempo, mas não serão renderizados.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: 'Método IAMTimeline:: EffectsEnabled (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d988e8a4c10dc6dba52269c6729b8d7fea1f090e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749000"
---
# <a name="iamtimelineeffectsenabled-method"></a><span data-ttu-id="6e49e-104">Método IAMTimeline:: EffectsEnabled</span><span class="sxs-lookup"><span data-stu-id="6e49e-104">IAMTimeline::EffectsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="6e49e-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6e49e-105">\[Deprecated.</span></span> <span data-ttu-id="6e49e-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6e49e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6e49e-107">O `EffectsEnabled` método determina se os efeitos estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="6e49e-107">The `EffectsEnabled` method determines whether effects are enabled.</span></span> <span data-ttu-id="6e49e-108">Se os efeitos estiverem desabilitados, eles permanecerão na linha do tempo, mas não serão renderizados.</span><span class="sxs-lookup"><span data-stu-id="6e49e-108">If effects are disabled, they remain in the timeline but are not rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e49e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6e49e-109">Syntax</span></span>


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="6e49e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e49e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e49e-111">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="6e49e-111">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="6e49e-112">Recebe um valor booliano que indica se os efeitos estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="6e49e-112">Receives a Boolean value indicating whether effects are enabled.</span></span> <span data-ttu-id="6e49e-113">Se **for true**, os efeitos serão habilitados.</span><span class="sxs-lookup"><span data-stu-id="6e49e-113">If **TRUE**, effects are enabled.</span></span> <span data-ttu-id="6e49e-114">Se **for false**, os efeitos serão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="6e49e-114">If **FALSE**, effects are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e49e-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6e49e-115">Return value</span></span>

<span data-ttu-id="6e49e-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6e49e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6e49e-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6e49e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e49e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e49e-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6e49e-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6e49e-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6e49e-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6e49e-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6e49e-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6e49e-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6e49e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e49e-122">Requirements</span></span>



| <span data-ttu-id="6e49e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e49e-123">Requirement</span></span> | <span data-ttu-id="6e49e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6e49e-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e49e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6e49e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6e49e-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e49e-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6e49e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e49e-127">Library</span></span><br/> | <dl> <span data-ttu-id="6e49e-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e49e-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e49e-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6e49e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e49e-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="6e49e-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="6e49e-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6e49e-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




