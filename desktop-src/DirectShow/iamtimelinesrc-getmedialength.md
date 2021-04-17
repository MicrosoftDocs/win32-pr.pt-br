---
description: O método GetMediaLength recupera o tamanho da mídia desse objeto de origem.
ms.assetid: 70298d8f-67e7-4774-a7ae-f0b48e4afda7
title: 'Método IAMTimelineSrc:: GetMediaLength (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5cd896ed0890a199f85838a01c4c6ebec6d0895d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768639"
---
# <a name="iamtimelinesrcgetmedialength-method"></a><span data-ttu-id="b1f85-103">Método IAMTimelineSrc:: GetMediaLength</span><span class="sxs-lookup"><span data-stu-id="b1f85-103">IAMTimelineSrc::GetMediaLength method</span></span>

> [!Note]  
> <span data-ttu-id="b1f85-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b1f85-104">\[Deprecated.</span></span> <span data-ttu-id="b1f85-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b1f85-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b1f85-106">O `GetMediaLength` método recupera o tamanho da mídia desse objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="b1f85-106">The `GetMediaLength` method retrieves the media length of this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f85-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1f85-107">Syntax</span></span>


```C++
HRESULT GetMediaLength(
   REFERENCE_TIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="b1f85-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b1f85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1f85-109">*pLength*</span><span class="sxs-lookup"><span data-stu-id="b1f85-109">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="b1f85-110">Recebe o comprimento da mídia em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b1f85-110">Receives the media length in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1f85-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b1f85-111">Return value</span></span>

<span data-ttu-id="b1f85-112">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="b1f85-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b1f85-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b1f85-113">Return code</span></span>                                                                                     | <span data-ttu-id="b1f85-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1f85-114">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="b1f85-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1f85-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="b1f85-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b1f85-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="b1f85-117"><dt>**E não \_ determinado**</dt></span><span class="sxs-lookup"><span data-stu-id="b1f85-117"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="b1f85-118">Os horários de mídia não estão definidos neste objeto.</span><span class="sxs-lookup"><span data-stu-id="b1f85-118">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="b1f85-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b1f85-119"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="b1f85-120">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b1f85-120">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="b1f85-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1f85-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1f85-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b1f85-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b1f85-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b1f85-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b1f85-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b1f85-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1f85-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1f85-125">Requirements</span></span>



| <span data-ttu-id="b1f85-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1f85-126">Requirement</span></span> | <span data-ttu-id="b1f85-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f85-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f85-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b1f85-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b1f85-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f85-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b1f85-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1f85-130">Library</span></span><br/> | <dl> <span data-ttu-id="b1f85-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1f85-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1f85-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b1f85-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f85-133">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="b1f85-133">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="b1f85-134">**IAMTimelineSrc::SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="b1f85-134">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> <dt>

[<span data-ttu-id="b1f85-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="b1f85-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




