---
description: 'O método GetMediaLength2 recupera o tamanho da mídia desse objeto de origem. Esse método é equivalente a IAMTimelineSrc:: GetMediaLength, mas usa os valores de REFTIME.'
ms.assetid: 96685e00-4e16-4205-a6ad-8b83cf2f8c29
title: 'Método IAMTimelineSrc:: GetMediaLength2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaLength2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: caee510db9ddeda1923327176a634a9011601e4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810940"
---
# <a name="iamtimelinesrcgetmedialength2-method"></a><span data-ttu-id="d8501-104">Método IAMTimelineSrc:: GetMediaLength2</span><span class="sxs-lookup"><span data-stu-id="d8501-104">IAMTimelineSrc::GetMediaLength2 method</span></span>

> [!Note]  
> <span data-ttu-id="d8501-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d8501-105">\[Deprecated.</span></span> <span data-ttu-id="d8501-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8501-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d8501-107">O `GetMediaLength2` método recupera o tamanho da mídia desse objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="d8501-107">The `GetMediaLength2` method retrieves the media length of this source object.</span></span> <span data-ttu-id="d8501-108">Esse método é equivalente a [**IAMTimelineSrc:: GetMediaLength**](iamtimelinesrc-getmedialength.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="d8501-108">This method is equivalent to [**IAMTimelineSrc::GetMediaLength**](iamtimelinesrc-getmedialength.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8501-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8501-109">Syntax</span></span>


```C++
HRESULT GetMediaLength2(
   REFTIME *pLength
);
```



## <a name="parameters"></a><span data-ttu-id="d8501-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8501-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8501-111">*pLength*</span><span class="sxs-lookup"><span data-stu-id="d8501-111">*pLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d8501-112">Recebe o comprimento da mídia em segundos.</span><span class="sxs-lookup"><span data-stu-id="d8501-112">Receives the media length in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8501-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8501-113">Return value</span></span>

<span data-ttu-id="d8501-114">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="d8501-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="d8501-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8501-115">Return code</span></span>                                                                                     | <span data-ttu-id="d8501-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8501-116">Description</span></span>                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="d8501-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8501-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="d8501-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="d8501-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="d8501-119"><dt>**E não \_ determinado**</dt></span><span class="sxs-lookup"><span data-stu-id="d8501-119"><dt>**E\_NOTDETERMINED**</dt></span></span> </dl> | <span data-ttu-id="d8501-120">Os horários de mídia não estão definidos neste objeto.</span><span class="sxs-lookup"><span data-stu-id="d8501-120">Media times are not set on this object.</span></span><br/> |
| <dl> <span data-ttu-id="d8501-121"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d8501-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="d8501-122">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="d8501-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="d8501-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8501-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d8501-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d8501-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d8501-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d8501-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d8501-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d8501-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d8501-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8501-127">Requirements</span></span>



| <span data-ttu-id="d8501-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8501-128">Requirement</span></span> | <span data-ttu-id="d8501-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d8501-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8501-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8501-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d8501-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8501-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d8501-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8501-132">Library</span></span><br/> | <dl> <span data-ttu-id="d8501-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8501-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8501-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8501-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8501-135">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="d8501-135">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d8501-136">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d8501-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




