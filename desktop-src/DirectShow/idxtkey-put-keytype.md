---
description: O \_ método Put KeyType especifica o tipo de chave.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: 'IDxtKey: método de ut_KeyType de:p (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778467"
---
# <a name="idxtkeyput_keytype-method"></a><span data-ttu-id="2de0e-103">Método IDxtKey::p UT \_ KeyType</span><span class="sxs-lookup"><span data-stu-id="2de0e-103">IDxtKey::put\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="2de0e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="2de0e-104">\[Deprecated.</span></span> <span data-ttu-id="2de0e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2de0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2de0e-106">O `put_KeyType` método especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="2de0e-106">The `put_KeyType` method specifies the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de0e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de0e-107">Syntax</span></span>


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a><span data-ttu-id="2de0e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2de0e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de0e-109">*newVal* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2de0e-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2de0e-110">Especifica o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="2de0e-110">Specifies the key type.</span></span> <span data-ttu-id="2de0e-111">Esse parâmetro deve ser um dos seguintes valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="2de0e-111">This parameter must be one of the following enumeration values.</span></span>



| <span data-ttu-id="2de0e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2de0e-112">Value</span></span>             | <span data-ttu-id="2de0e-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2de0e-113">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="2de0e-114">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="2de0e-114">DXTKEY\_RGB</span></span>       | <span data-ttu-id="2de0e-115">Chave croma.</span><span class="sxs-lookup"><span data-stu-id="2de0e-115">Chroma key.</span></span> <span data-ttu-id="2de0e-116">(Chave no valor RGB.)</span><span class="sxs-lookup"><span data-stu-id="2de0e-116">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="2de0e-117">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="2de0e-117">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="2de0e-118">Chave Nonred.</span><span class="sxs-lookup"><span data-stu-id="2de0e-118">Nonred key.</span></span> <span data-ttu-id="2de0e-119">(Torna as áreas azul e verde transparentes.)</span><span class="sxs-lookup"><span data-stu-id="2de0e-119">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="2de0e-120">luminância de DXTKEY \_</span><span class="sxs-lookup"><span data-stu-id="2de0e-120">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="2de0e-121">Chave de luminância.</span><span class="sxs-lookup"><span data-stu-id="2de0e-121">Luminance key.</span></span>                                        |
| <span data-ttu-id="2de0e-122">DXTKEY \_ alfa</span><span class="sxs-lookup"><span data-stu-id="2de0e-122">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="2de0e-123">Chave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="2de0e-123">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="2de0e-124">\_matiz DXTKEY</span><span class="sxs-lookup"><span data-stu-id="2de0e-124">DXTKEY\_HUE</span></span>       | <span data-ttu-id="2de0e-125">Chave por matiz.</span><span class="sxs-lookup"><span data-stu-id="2de0e-125">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de0e-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2de0e-126">Return value</span></span>

<span data-ttu-id="2de0e-127">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2de0e-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2de0e-128">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2de0e-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de0e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="2de0e-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2de0e-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="2de0e-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2de0e-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2de0e-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2de0e-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2de0e-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2de0e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de0e-133">Requirements</span></span>



| <span data-ttu-id="2de0e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de0e-134">Requirement</span></span> | <span data-ttu-id="2de0e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="2de0e-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2de0e-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2de0e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="2de0e-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de0e-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2de0e-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2de0e-138">Library</span></span><br/> | <dl> <span data-ttu-id="2de0e-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2de0e-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de0e-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de0e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de0e-141">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="2de0e-141">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




