---
title: Função D3DX_R8G8B8A8_SINT_to_INT4
description: Desempacota \_ \_ os dados do sombreador do formato dxgi R8G8B8A8 \_ Santo para um XMINT4.
ms.assetid: 144bd296-02b5-4307-b785-860680db2d52
keywords:
- Função D3DX_R8G8B8A8_SINT_to_INT4 HLSL
topic_type:
- apiref
api_name:
- D3DX_R8G8B8A8_SINT_to_INT4
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d129982db5535d91b38dc9d3630f78192c4b1fbc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091977"
---
# <a name="d3dx_r8g8b8a8_sint_to_int4-function"></a><span data-ttu-id="56fb7-104">D3DX \_ R8G8B8A8 \_ Santo \_ a \_ INT4 function</span><span class="sxs-lookup"><span data-stu-id="56fb7-104">D3DX\_R8G8B8A8\_SINT\_to\_INT4 function</span></span>

<span data-ttu-id="56fb7-105">Desempacota \_ \_ os dados do sombreador do formato dxgi R8G8B8A8 \_ Santo para um XMINT4.</span><span class="sxs-lookup"><span data-stu-id="56fb7-105">Unpacks DXGI\_FORMAT\_R8G8B8A8\_SINT shader data to an XMINT4.</span></span>

## <a name="syntax"></a><span data-ttu-id="56fb7-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56fb7-106">Syntax</span></span>

``` syntax
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="56fb7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56fb7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56fb7-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="56fb7-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="56fb7-109">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="56fb7-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56fb7-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56fb7-110">Return value</span></span>

<span data-ttu-id="56fb7-111">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="56fb7-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="56fb7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56fb7-112">Requirements</span></span>



| <span data-ttu-id="56fb7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="56fb7-113">Requirement</span></span> | <span data-ttu-id="56fb7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="56fb7-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56fb7-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56fb7-115">Header</span></span><br/> | <dl> <span data-ttu-id="56fb7-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="56fb7-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56fb7-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="56fb7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56fb7-118">Funções</span><span class="sxs-lookup"><span data-stu-id="56fb7-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="56fb7-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="56fb7-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





