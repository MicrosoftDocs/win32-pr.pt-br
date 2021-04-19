---
description: Crie um carregador de arquivo assíncrono.
ms.assetid: 1b79fba5-e7f0-4160-9cec-ffea94f84fde
title: Função D3DX10CreateAsyncFileLoader (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncFileLoader
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: e98bccf709fa4a6d921e266148b94fd8623429ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105814418"
---
# <a name="d3dx10createasyncfileloader-function"></a><span data-ttu-id="b0c20-103">Função D3DX10CreateAsyncFileLoader</span><span class="sxs-lookup"><span data-stu-id="b0c20-103">D3DX10CreateAsyncFileLoader function</span></span>

<span data-ttu-id="b0c20-104">Crie um carregador de arquivo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="b0c20-104">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0c20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0c20-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX10DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="b0c20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0c20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c20-107">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b0c20-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0c20-108">Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b0c20-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b0c20-109">O nome do arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="b0c20-109">The name of the file to load.</span></span> <span data-ttu-id="b0c20-110">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="b0c20-110">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="b0c20-111">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="b0c20-111">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="b0c20-112">*ppDataLoader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0c20-112">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0c20-113">Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="b0c20-113">Type: **[**ID3DX10DataLoader**](id3dx10dataloader.md)\*\***</span></span>

<span data-ttu-id="b0c20-114">Endereço de um ponteiro para o carregador de dados assíncronos (consulte a [**interface ID3DX10DataLoader**](id3dx10dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="b0c20-114">Address of a pointer to the asynchronous-data loader (see [**ID3DX10DataLoader Interface**](id3dx10dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0c20-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0c20-115">Return value</span></span>

<span data-ttu-id="b0c20-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b0c20-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b0c20-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="b0c20-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c20-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0c20-118">Requirements</span></span>



| <span data-ttu-id="b0c20-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0c20-119">Requirement</span></span> | <span data-ttu-id="b0c20-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b0c20-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c20-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0c20-121">Header</span></span><br/> | <dl> <span data-ttu-id="b0c20-122"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0c20-122"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c20-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0c20-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c20-124">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="b0c20-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
