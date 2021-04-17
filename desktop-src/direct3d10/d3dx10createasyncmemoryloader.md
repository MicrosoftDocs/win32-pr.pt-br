---
description: Crie um carregador de memória assíncrona.
ms.assetid: 92177390-cb09-445e-9828-806a23ef91b5
title: Função D3DX10CreateAsyncMemoryLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncMemoryLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0219026eabfcff6dfcec0df4721716302f09f5e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798060"
---
# <a name="d3dx10createasyncmemoryloader-function"></a><span data-ttu-id="95ed4-103">Função D3DX10CreateAsyncMemoryLoader</span><span class="sxs-lookup"><span data-stu-id="95ed4-103">D3DX10CreateAsyncMemoryLoader function</span></span>

<span data-ttu-id="95ed4-104">Crie um carregador de memória assíncrona.</span><span class="sxs-lookup"><span data-stu-id="95ed4-104">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ed4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95ed4-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="95ed4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95ed4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ed4-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95ed4-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ed4-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95ed4-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95ed4-109">Ponteiro para os dados.</span><span class="sxs-lookup"><span data-stu-id="95ed4-109">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="95ed4-110">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="95ed4-110">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95ed4-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95ed4-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95ed4-112">Tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="95ed4-112">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="95ed4-113">*ppDataLoader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="95ed4-113">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="95ed4-114">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="95ed4-114">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="95ed4-115">O endereço de um ponteiro para o processador de dados assíncronos (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="95ed4-115">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ed4-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95ed4-116">Return value</span></span>

<span data-ttu-id="95ed4-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95ed4-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95ed4-118">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="95ed4-118">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95ed4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95ed4-119">Requirements</span></span>



| <span data-ttu-id="95ed4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="95ed4-120">Requirement</span></span> | <span data-ttu-id="95ed4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="95ed4-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95ed4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95ed4-122">Header</span></span><br/> | <dl> <span data-ttu-id="95ed4-123"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="95ed4-123"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95ed4-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="95ed4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ed4-125">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="95ed4-125">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
