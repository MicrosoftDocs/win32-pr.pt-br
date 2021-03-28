---
title: Função D3DX_R16G16_SINT_to_INT2
description: Desempacota \_ \_ os dados do sombreador do formato dxgi R16G16 \_ Santo para um XMINT2.
ms.assetid: 0aad1581-5fd8-43c0-828d-51ef9eb82a74
keywords:
- Função D3DX_R16G16_SINT_to_INT2 HLSL
topic_type:
- apiref
api_name:
- D3DX_R16G16_SINT_to_INT2
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9e14e935b49e1fa0c982551696e8d38a076a5bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989384"
---
# <a name="d3dx_r16g16_sint_to_int2-function"></a><span data-ttu-id="5358c-104">D3DX \_ R16G16 \_ Santo \_ a \_ Int2 function</span><span class="sxs-lookup"><span data-stu-id="5358c-104">D3DX\_R16G16\_SINT\_to\_INT2 function</span></span>

<span data-ttu-id="5358c-105">Desempacota \_ \_ os dados do sombreador do formato dxgi R16G16 \_ Santo para um XMINT2.</span><span class="sxs-lookup"><span data-stu-id="5358c-105">Unpacks DXGI\_FORMAT\_R16G16\_SINT shader data to an XMINT2.</span></span>

## <a name="syntax"></a><span data-ttu-id="5358c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5358c-106">Syntax</span></span>

``` syntax
XMINT2 D3DX_R16G16_SINT_to_INT2(
   UINT packedInput
);
```

## <a name="parameters"></a><span data-ttu-id="5358c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5358c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5358c-108">*packedInput*</span><span class="sxs-lookup"><span data-stu-id="5358c-108">*packedInput*</span></span> 
</dt> <dd>

<span data-ttu-id="5358c-109">Os dados do sombreador embalado.</span><span class="sxs-lookup"><span data-stu-id="5358c-109">The packed shader data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5358c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5358c-110">Return value</span></span>

<span data-ttu-id="5358c-111">Os dados do sombreador desempacotado.</span><span class="sxs-lookup"><span data-stu-id="5358c-111">The unpacked shader data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5358c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5358c-112">Requirements</span></span>



| <span data-ttu-id="5358c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5358c-113">Requirement</span></span> | <span data-ttu-id="5358c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5358c-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5358c-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5358c-115">Header</span></span><br/> | <dl> <span data-ttu-id="5358c-116"><dt>D3DX \_ DXGIFormatConvert. inl</dt></span><span class="sxs-lookup"><span data-stu-id="5358c-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5358c-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5358c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5358c-118">Funções</span><span class="sxs-lookup"><span data-stu-id="5358c-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5358c-119">Descompactando e empacotando o \_ formato dxgi para a edição de imagem In-Place</span><span class="sxs-lookup"><span data-stu-id="5358c-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





