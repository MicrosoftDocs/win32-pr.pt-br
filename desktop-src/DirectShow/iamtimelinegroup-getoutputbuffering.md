---
description: O método GetOutputBuffering recupera o número de quadros processados antecipadamente durante a visualização.
ms.assetid: 93cb8d18-f1b7-48f9-af41-97f010304b05
title: 'Método IAMTimelineGroup:: GetOutputBuffering (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.GetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8213be882ca445775137a946d9064487b25f48af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758844"
---
# <a name="iamtimelinegroupgetoutputbuffering-method"></a><span data-ttu-id="374cd-103">Método IAMTimelineGroup:: GetOutputBuffering</span><span class="sxs-lookup"><span data-stu-id="374cd-103">IAMTimelineGroup::GetOutputBuffering method</span></span>

> [!Note]  
> <span data-ttu-id="374cd-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="374cd-104">\[Deprecated.</span></span> <span data-ttu-id="374cd-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="374cd-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="374cd-106">O `GetOutputBuffering` método recupera o número de quadros renderizados antecipadamente durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="374cd-106">The `GetOutputBuffering` method retrieves the number of frames rendered in advance during preview.</span></span>

## <a name="syntax"></a><span data-ttu-id="374cd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="374cd-107">Syntax</span></span>


```C++
HRESULT GetOutputBuffering(
  [out] int *pnBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="374cd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="374cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="374cd-109">*pnBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="374cd-109">*pnBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="374cd-110">Recebe o número de quadros em buffer.</span><span class="sxs-lookup"><span data-stu-id="374cd-110">Receives the number of buffered frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="374cd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="374cd-111">Return value</span></span>

<span data-ttu-id="374cd-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="374cd-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="374cd-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="374cd-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="374cd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="374cd-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="374cd-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="374cd-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="374cd-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="374cd-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="374cd-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="374cd-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="374cd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="374cd-118">Requirements</span></span>



| <span data-ttu-id="374cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="374cd-119">Requirement</span></span> | <span data-ttu-id="374cd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="374cd-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="374cd-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="374cd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="374cd-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="374cd-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="374cd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="374cd-123">Library</span></span><br/> | <dl> <span data-ttu-id="374cd-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="374cd-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="374cd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="374cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374cd-126">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="374cd-126">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="374cd-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="374cd-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




