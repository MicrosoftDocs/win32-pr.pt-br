---
description: Processar alguns dados.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: 'ID3DX10DataProcessor: método modelos de:P (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173213"
---
# <a name="id3dx10dataprocessorprocess-method"></a><span data-ttu-id="f6654-103">ID3DX10DataProcessor: método modelos de:P</span><span class="sxs-lookup"><span data-stu-id="f6654-103">ID3DX10DataProcessor::Process method</span></span>

<span data-ttu-id="f6654-104">Processar alguns dados.</span><span class="sxs-lookup"><span data-stu-id="f6654-104">Process some data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6654-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6654-105">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="f6654-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6654-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6654-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6654-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6654-108">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="f6654-108">Type: **void\***</span></span>

<span data-ttu-id="f6654-109">Ponteiro para os dados a serem processados.</span><span class="sxs-lookup"><span data-stu-id="f6654-109">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="f6654-110">*cBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f6654-110">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6654-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f6654-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f6654-112">Tamanho dos dados a serem processados.</span><span class="sxs-lookup"><span data-stu-id="f6654-112">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6654-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6654-113">Return value</span></span>

<span data-ttu-id="f6654-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f6654-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f6654-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f6654-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6654-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6654-116">Requirements</span></span>



| <span data-ttu-id="f6654-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6654-117">Requirement</span></span> | <span data-ttu-id="f6654-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f6654-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6654-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6654-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f6654-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6654-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6654-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6654-121">Library</span></span><br/> | <dl> <span data-ttu-id="f6654-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6654-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6654-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6654-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6654-124">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="f6654-124">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="f6654-125">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f6654-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
