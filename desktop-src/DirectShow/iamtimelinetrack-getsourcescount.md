---
description: O método GetSourcesCount recupera o número de fontes na faixa.
ms.assetid: eb7f249f-355f-454d-9fe6-c3271fd13fc7
title: 'Método IAMTimelineTrack:: GetSourcesCount (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSourcesCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e143b16e5cdc1e193760c0b97846be07eb72c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780055"
---
# <a name="iamtimelinetrackgetsourcescount-method"></a><span data-ttu-id="1edcf-103">Método IAMTimelineTrack:: GetSourcesCount</span><span class="sxs-lookup"><span data-stu-id="1edcf-103">IAMTimelineTrack::GetSourcesCount method</span></span>

> [!Note]  
> <span data-ttu-id="1edcf-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="1edcf-104">\[Deprecated.</span></span> <span data-ttu-id="1edcf-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1edcf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1edcf-106">O `GetSourcesCount` método recupera o número de fontes na faixa.</span><span class="sxs-lookup"><span data-stu-id="1edcf-106">The `GetSourcesCount` method retrieves the number of sources in the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="1edcf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1edcf-107">Syntax</span></span>


```C++
HRESULT GetSourcesCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="1edcf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1edcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1edcf-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="1edcf-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="1edcf-110">Recebe o número de fontes na faixa.</span><span class="sxs-lookup"><span data-stu-id="1edcf-110">Receives the number of sources in the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1edcf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1edcf-111">Return value</span></span>

<span data-ttu-id="1edcf-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1edcf-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1edcf-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1edcf-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1edcf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1edcf-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1edcf-115">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="1edcf-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1edcf-116">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1edcf-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1edcf-117">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="1edcf-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1edcf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1edcf-118">Requirements</span></span>



| <span data-ttu-id="1edcf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1edcf-119">Requirement</span></span> | <span data-ttu-id="1edcf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1edcf-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1edcf-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1edcf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1edcf-122"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1edcf-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1edcf-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1edcf-123">Library</span></span><br/> | <dl> <span data-ttu-id="1edcf-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1edcf-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1edcf-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1edcf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edcf-126">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="1edcf-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="1edcf-127">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="1edcf-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




