---
description: O método TransitionsEnabled determina se as transições estão habilitadas.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: 'Método IAMTimeline:: TransitionsEnabled (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7116ccf4ff2015934c9071f4ce2ef073656b89c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796271"
---
# <a name="iamtimelinetransitionsenabled-method"></a><span data-ttu-id="c8e5e-103">Método IAMTimeline:: TransitionsEnabled</span><span class="sxs-lookup"><span data-stu-id="c8e5e-103">IAMTimeline::TransitionsEnabled method</span></span>

> [!Note]  
> <span data-ttu-id="c8e5e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-104">\[Deprecated.</span></span> <span data-ttu-id="c8e5e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8e5e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c8e5e-106">O método **TransitionsEnabled** determina se as transições estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-106">The **TransitionsEnabled** method determines whether transitions are enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e5e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8e5e-107">Syntax</span></span>


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="c8e5e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8e5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8e5e-109">*pfEnabled*</span><span class="sxs-lookup"><span data-stu-id="c8e5e-109">*pfEnabled*</span></span> 
</dt> <dd>

<span data-ttu-id="c8e5e-110">Recebe um valor booliano.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-110">Receives a Boolean value.</span></span> <span data-ttu-id="c8e5e-111">Se **for true**, as transições serão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-111">If **TRUE**, transitions are enabled.</span></span> <span data-ttu-id="c8e5e-112">Caso contrário, as transições serão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-112">Otherwise, transitions are disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8e5e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8e5e-113">Return value</span></span>

<span data-ttu-id="c8e5e-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8e5e-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8e5e-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e5e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8e5e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c8e5e-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c8e5e-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8e5e-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c8e5e-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c8e5e-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c8e5e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8e5e-120">Requirements</span></span>



| <span data-ttu-id="c8e5e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e5e-121">Requirement</span></span> | <span data-ttu-id="c8e5e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c8e5e-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e5e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8e5e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c8e5e-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e5e-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c8e5e-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8e5e-125">Library</span></span><br/> | <dl> <span data-ttu-id="c8e5e-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8e5e-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e5e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8e5e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e5e-128">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="c8e5e-128">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="c8e5e-129">**IAMTimeline::EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="c8e5e-129">**IAMTimeline::EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)
</dt> <dt>

[<span data-ttu-id="c8e5e-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="c8e5e-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




