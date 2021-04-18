---
description: Usado para descompactar dados codificados. Normalmente, isso seria usado para carregar recursos de sistemas de arquivos, como arquivos ZIP. Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: 'ID3DX10DataLoader: método ecompress de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781144"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="43a5d-105">ID3DX10DataLoader: método ecompress de:D</span><span class="sxs-lookup"><span data-stu-id="43a5d-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="43a5d-106">Usado para descompactar dados codificados.</span><span class="sxs-lookup"><span data-stu-id="43a5d-106">Used to decompress encoded data.</span></span> <span data-ttu-id="43a5d-107">Normalmente, isso seria usado para carregar recursos de sistemas de arquivos, como arquivos ZIP.</span><span class="sxs-lookup"><span data-stu-id="43a5d-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="43a5d-108">Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="43a5d-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a5d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43a5d-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="43a5d-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43a5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a5d-111">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43a5d-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a5d-112">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="43a5d-112">Type: **void\*\***</span></span>

<span data-ttu-id="43a5d-113">Ponteiro para os dados brutos a serem descompactados.</span><span class="sxs-lookup"><span data-stu-id="43a5d-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="43a5d-114">*pcBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="43a5d-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a5d-115">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="43a5d-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="43a5d-116">O tamanho dos dados apontados por ppData.</span><span class="sxs-lookup"><span data-stu-id="43a5d-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a5d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43a5d-117">Return value</span></span>

<span data-ttu-id="43a5d-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43a5d-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43a5d-119">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="43a5d-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43a5d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="43a5d-120">Remarks</span></span>

<span data-ttu-id="43a5d-121">A [**interface ID3DX10DataLoader**](id3dx10dataloader.md) pode ser herdada e seus membros redefinidos.</span><span class="sxs-lookup"><span data-stu-id="43a5d-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="43a5d-122">A descompactação pode ser redefinida para dar suporte aos seus próprios formatos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="43a5d-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a5d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a5d-123">Requirements</span></span>



| <span data-ttu-id="43a5d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a5d-124">Requirement</span></span> | <span data-ttu-id="43a5d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="43a5d-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a5d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43a5d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="43a5d-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a5d-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="43a5d-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43a5d-128">Library</span></span><br/> | <dl> <span data-ttu-id="43a5d-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43a5d-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a5d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a5d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a5d-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="43a5d-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="43a5d-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="43a5d-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
