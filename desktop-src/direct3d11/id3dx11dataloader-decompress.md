---
title: Método decompactar ID3DX11DataLoader (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Descompacta dados codificados.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Método de descompactação do Direct3D 11
- Método descompactar o Direct3D 11, interface ID3DX11DataLoader
- Interface ID3DX11DataLoader Direct3D 11, método decompactar
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930752"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="def19-107">ID3DX11DataLoader: método ecompress de:D</span><span class="sxs-lookup"><span data-stu-id="def19-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="def19-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="def19-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="def19-109">Descompacta dados codificados.</span><span class="sxs-lookup"><span data-stu-id="def19-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="def19-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="def19-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="def19-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="def19-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def19-112">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="def19-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="def19-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="def19-113">Type: **void\*\***</span></span>

<span data-ttu-id="def19-114">Ponteiro para os dados brutos a serem descompactados.</span><span class="sxs-lookup"><span data-stu-id="def19-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="def19-115">*pcBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="def19-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def19-116">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="def19-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="def19-117">O tamanho dos dados apontados por ppData.</span><span class="sxs-lookup"><span data-stu-id="def19-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def19-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="def19-118">Return value</span></span>

<span data-ttu-id="def19-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="def19-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="def19-120">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="def19-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="def19-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="def19-121">Remarks</span></span>

<span data-ttu-id="def19-122">Use esse método para carregar recursos de sistemas de arquivos, como arquivos ZIP.</span><span class="sxs-lookup"><span data-stu-id="def19-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="def19-123">Ao carregar de um recurso descompactado, o estágio de descompactação não precisa fazer nenhum trabalho.</span><span class="sxs-lookup"><span data-stu-id="def19-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="def19-124">A [**interface ID3DX11DataLoader**](id3dx11dataloader.md) pode ser herdada e seus membros redefinidos para dar suporte a formatos de arquivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="def19-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="def19-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def19-125">Requirements</span></span>



| <span data-ttu-id="def19-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="def19-126">Requirement</span></span> | <span data-ttu-id="def19-127">Valor</span><span class="sxs-lookup"><span data-stu-id="def19-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="def19-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="def19-128">Header</span></span><br/>  | <dl> <span data-ttu-id="def19-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="def19-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="def19-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="def19-130">Library</span></span><br/> | <dl> <span data-ttu-id="def19-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="def19-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="def19-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="def19-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def19-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="def19-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="def19-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="def19-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

