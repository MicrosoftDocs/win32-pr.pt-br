---
description: O \_ método obter KeyType recupera o tipo de chave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Método IDxtKey:: get_KeyType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778468"
---
# <a name="idxtkeyget_keytype-method"></a><span data-ttu-id="b8c53-103">Método IDxtKey:: get \_ KeyType</span><span class="sxs-lookup"><span data-stu-id="b8c53-103">IDxtKey::get\_KeyType method</span></span>

> [!Note]  
> <span data-ttu-id="b8c53-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b8c53-104">\[Deprecated.</span></span> <span data-ttu-id="b8c53-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b8c53-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b8c53-106">O `get_KeyType` método recupera o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="b8c53-106">The `get_KeyType` method retrieves the type of key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8c53-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8c53-107">Syntax</span></span>


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b8c53-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8c53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8c53-109">*PVal* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b8c53-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b8c53-110">Recebe um dos seguintes valores de enumeração.</span><span class="sxs-lookup"><span data-stu-id="b8c53-110">Receives one of the following enumeration values.</span></span>



| <span data-ttu-id="b8c53-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b8c53-111">Value</span></span>             | <span data-ttu-id="b8c53-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8c53-112">Description</span></span>                                           |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="b8c53-113">DXTKEY \_ RGB</span><span class="sxs-lookup"><span data-stu-id="b8c53-113">DXTKEY\_RGB</span></span>       | <span data-ttu-id="b8c53-114">Chave croma.</span><span class="sxs-lookup"><span data-stu-id="b8c53-114">Chroma key.</span></span> <span data-ttu-id="b8c53-115">(Chave no valor RGB.)</span><span class="sxs-lookup"><span data-stu-id="b8c53-115">(Key on RGB value.)</span></span>                       |
| <span data-ttu-id="b8c53-116">DXTKEY \_ NONRED</span><span class="sxs-lookup"><span data-stu-id="b8c53-116">DXTKEY\_NONRED</span></span>    | <span data-ttu-id="b8c53-117">Chave Nonred.</span><span class="sxs-lookup"><span data-stu-id="b8c53-117">Nonred key.</span></span> <span data-ttu-id="b8c53-118">(Torna as áreas azul e verde transparentes.)</span><span class="sxs-lookup"><span data-stu-id="b8c53-118">(Makes blue and green areas transparent.)</span></span> |
| <span data-ttu-id="b8c53-119">luminância de DXTKEY \_</span><span class="sxs-lookup"><span data-stu-id="b8c53-119">DXTKEY\_LUMINANCE</span></span> | <span data-ttu-id="b8c53-120">Chave de luminância.</span><span class="sxs-lookup"><span data-stu-id="b8c53-120">Luminance key.</span></span>                                        |
| <span data-ttu-id="b8c53-121">DXTKEY \_ alfa</span><span class="sxs-lookup"><span data-stu-id="b8c53-121">DXTKEY\_ALPHA</span></span>     | <span data-ttu-id="b8c53-122">Chave por valor alfa.</span><span class="sxs-lookup"><span data-stu-id="b8c53-122">Key by alpha value.</span></span>                                   |
| <span data-ttu-id="b8c53-123">\_matiz DXTKEY</span><span class="sxs-lookup"><span data-stu-id="b8c53-123">DXTKEY\_HUE</span></span>       | <span data-ttu-id="b8c53-124">Chave por matiz.</span><span class="sxs-lookup"><span data-stu-id="b8c53-124">Key by hue.</span></span>                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8c53-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8c53-125">Return value</span></span>

<span data-ttu-id="b8c53-126">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b8c53-126">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b8c53-127">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b8c53-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c53-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8c53-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8c53-129">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b8c53-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b8c53-130">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b8c53-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b8c53-131">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b8c53-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b8c53-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8c53-132">Requirements</span></span>



| <span data-ttu-id="b8c53-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8c53-133">Requirement</span></span> | <span data-ttu-id="b8c53-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b8c53-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8c53-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8c53-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b8c53-136"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8c53-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b8c53-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8c53-137">Library</span></span><br/> | <dl> <span data-ttu-id="b8c53-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8c53-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8c53-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8c53-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8c53-140">**Interface IDxtKey**</span><span class="sxs-lookup"><span data-stu-id="b8c53-140">**IDxtKey Interface**</span></span>](idxtkey.md)
</dt> </dl>

 

 




