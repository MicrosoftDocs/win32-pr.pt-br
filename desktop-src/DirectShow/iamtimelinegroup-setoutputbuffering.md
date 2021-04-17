---
description: O método SetOutputBuffering especifica o número de quadros renderizados antecipadamente durante a visualização.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: 'Método IAMTimelineGroup:: SetOutputBuffering (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760090"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a><span data-ttu-id="5124b-103">Método IAMTimelineGroup:: SetOutputBuffering</span><span class="sxs-lookup"><span data-stu-id="5124b-103">IAMTimelineGroup::SetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="5124b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5124b-104">\[Deprecated.</span></span> <span data-ttu-id="5124b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5124b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5124b-106">O `SetOutputBuffering` método especifica o número de quadros renderizados antecipadamente durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="5124b-106">The `SetOutputBuffering` method specifies the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="5124b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5124b-107">Syntax</span></span>


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="5124b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5124b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5124b-109">*nBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5124b-109">*nBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5124b-110">Número de quadros para armazenar em buffer durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="5124b-110">Number of frames to buffer during preview.</span></span> <span data-ttu-id="5124b-111">Deve ser dois ou mais.</span><span class="sxs-lookup"><span data-stu-id="5124b-111">Must be two or greater.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5124b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5124b-112">Return value</span></span>

<span data-ttu-id="5124b-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5124b-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5124b-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5124b-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5124b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5124b-115">Remarks</span></span>

<span data-ttu-id="5124b-116">Um buffer maior requer mais memória, mas pode resultar em uma visualização mais suave, especialmente durante efeitos ou transições que exigem mais tempo para serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="5124b-116">A larger buffer requires more memory but can result in smoother previewing, especially during effects or transitions that require more time to render.</span></span> <span data-ttu-id="5124b-117">O buffer padrão é de 30 quadros.</span><span class="sxs-lookup"><span data-stu-id="5124b-117">The default buffer is 30 frames.</span></span>

> [!Note]  
> <span data-ttu-id="5124b-118">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5124b-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5124b-119">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5124b-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5124b-120">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5124b-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5124b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5124b-121">Requirements</span></span>



| <span data-ttu-id="5124b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5124b-122">Requirement</span></span> | <span data-ttu-id="5124b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5124b-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5124b-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5124b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5124b-125"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5124b-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5124b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5124b-126">Library</span></span><br/> | <dl> <span data-ttu-id="5124b-127"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5124b-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5124b-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5124b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5124b-129">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="5124b-129">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="5124b-130">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5124b-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




