---
description: Crie um carregador de recurso assíncrono.
ms.assetid: 1b3eb21c-4ba6-4910-b2f0-2ffa4ae50e47
title: Função D3DX10CreateAsyncResourceLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncResourceLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: 0539817ffff75c28af41289fc5197f6440a915bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105782642"
---
# <a name="d3dx10createasyncresourceloader-function"></a><span data-ttu-id="48130-103">Função D3DX10CreateAsyncResourceLoader</span><span class="sxs-lookup"><span data-stu-id="48130-103">D3DX10CreateAsyncResourceLoader function</span></span>

<span data-ttu-id="48130-104">Crie um carregador de recurso assíncrono.</span><span class="sxs-lookup"><span data-stu-id="48130-104">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="48130-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="48130-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="48130-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48130-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48130-107">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48130-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48130-108">Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48130-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48130-109">Identificador para o módulo de recurso.</span><span class="sxs-lookup"><span data-stu-id="48130-109">Handle to the resource module.</span></span> <span data-ttu-id="48130-110">Use a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obter o identificador.</span><span class="sxs-lookup"><span data-stu-id="48130-110">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="48130-111">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="48130-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48130-112">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="48130-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="48130-113">Nome do recurso no hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="48130-113">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="48130-114">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="48130-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="48130-115">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="48130-115">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="48130-116">*ppDataLoader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="48130-116">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48130-117">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="48130-117">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="48130-118">O endereço de um ponteiro para o processador de dados assíncronos (consulte a [**interface ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="48130-118">The address of a pointer to the asynchronous-data processor (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48130-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="48130-119">Return value</span></span>

<span data-ttu-id="48130-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48130-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48130-121">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="48130-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48130-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48130-122">Requirements</span></span>



| <span data-ttu-id="48130-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="48130-123">Requirement</span></span> | <span data-ttu-id="48130-124">Valor</span><span class="sxs-lookup"><span data-stu-id="48130-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48130-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48130-125">Header</span></span><br/> | <dl> <span data-ttu-id="48130-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="48130-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48130-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="48130-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48130-128">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="48130-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
