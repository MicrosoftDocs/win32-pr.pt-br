---
title: Método de processo ID3DX11DataProcessor (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Processa dados.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Método de processo Direct3D 11
- Método de processo Direct3D 11, interface ID3DX11DataProcessor
- Interface ID3DX11DataProcessor Direct3D 11, método de processo
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104506493"
---
# <a name="id3dx11dataprocessorprocess-method"></a><span data-ttu-id="b5f82-107">ID3DX11DataProcessor: método modelos de:P</span><span class="sxs-lookup"><span data-stu-id="b5f82-107">ID3DX11DataProcessor::Process method</span></span>

> [!Note]  
> <span data-ttu-id="b5f82-108">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b5f82-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="b5f82-109">Processa dados.</span><span class="sxs-lookup"><span data-stu-id="b5f82-109">Processes data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f82-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5f82-110">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="b5f82-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5f82-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f82-112">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5f82-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f82-113">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="b5f82-113">Type: **void\***</span></span>

<span data-ttu-id="b5f82-114">Ponteiro para os dados a serem processados.</span><span class="sxs-lookup"><span data-stu-id="b5f82-114">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="b5f82-115">*cBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5f82-115">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5f82-116">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b5f82-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b5f82-117">Tamanho dos dados a serem processados.</span><span class="sxs-lookup"><span data-stu-id="b5f82-117">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f82-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5f82-118">Return value</span></span>

<span data-ttu-id="b5f82-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5f82-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5f82-120">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b5f82-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b5f82-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5f82-121">Remarks</span></span>

<span data-ttu-id="b5f82-122">Esse método é usado por uma [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="b5f82-122">This method is used by an [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f82-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f82-123">Requirements</span></span>



| <span data-ttu-id="b5f82-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f82-124">Requirement</span></span> | <span data-ttu-id="b5f82-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f82-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f82-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5f82-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b5f82-127"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5f82-127"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="b5f82-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5f82-128">Library</span></span><br/> | <dl> <span data-ttu-id="b5f82-129"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5f82-129"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5f82-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5f82-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f82-131">ID3DX11DataProcessor</span><span class="sxs-lookup"><span data-stu-id="b5f82-131">ID3DX11DataProcessor</span></span>](id3dx11dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="b5f82-132">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="b5f82-132">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

