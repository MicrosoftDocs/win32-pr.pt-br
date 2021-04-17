---
description: Um método implementado pelo usuário para fechar um arquivo de inclusão de sombreador \# .
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'Método ID3DXInclude:: Close (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813513"
---
# <a name="id3dxincludeclose-method"></a><span data-ttu-id="ce631-103">Método ID3DXInclude:: Close</span><span class="sxs-lookup"><span data-stu-id="ce631-103">ID3DXInclude::Close method</span></span>

<span data-ttu-id="ce631-104">Um método implementado pelo usuário para fechar um arquivo de inclusão de sombreador \# .</span><span class="sxs-lookup"><span data-stu-id="ce631-104">A user-implemented method for closing a shader \#include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce631-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ce631-105">Syntax</span></span>


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a><span data-ttu-id="ce631-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce631-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce631-107">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ce631-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce631-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ce631-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ce631-109">Ponteiro para o buffer retornado que contém as diretivas include.</span><span class="sxs-lookup"><span data-stu-id="ce631-109">Pointer to the returned buffer that contains the include directives.</span></span> <span data-ttu-id="ce631-110">Esse é o ponteiro retornado pela chamada [**ID3DXInclude:: Open**](id3dxinclude--open.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="ce631-110">This is the pointer that was returned by the corresponding [**ID3DXInclude::Open**](id3dxinclude--open.md) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce631-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce631-111">Return value</span></span>

<span data-ttu-id="ce631-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce631-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce631-113">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ce631-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="ce631-114">Se o retorno de chamada falhar ao ler o \# arquivo de inclusão, a API que causou o retorno de chamada será reprovada.</span><span class="sxs-lookup"><span data-stu-id="ce631-114">If the callback fails when reading the \#include file, the API that caused the callback to be called will fail.</span></span> <span data-ttu-id="ce631-115">Ele é um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="ce631-115">This is one of the following:</span></span>

-   <span data-ttu-id="ce631-116">O sombreador HLSL falhará em uma das funções do D3DXCompileShader \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="ce631-116">The HLSL shader will fail one of the D3DXCompileShader\*\*\* functions.</span></span>
-   <span data-ttu-id="ce631-117">O sombreador de assembly falhará em uma das \* \* \* funções D3DXAssembleShader.</span><span class="sxs-lookup"><span data-stu-id="ce631-117">The assembly shader will fail one of the D3DXAssembleShader\*\*\* functions.</span></span>
-   <span data-ttu-id="ce631-118">O efeito falhará em uma das \* \* \* funções D3DXCreateEffect ou D3DXCreateEffectCompiler \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="ce631-118">The effect will fail one of the D3DXCreateEffect\*\*\* or D3DXCreateEffectCompiler\*\*\* functions.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce631-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce631-119">Remarks</span></span>

<span data-ttu-id="ce631-120">Se [**ID3DXInclude:: Open**](id3dxinclude--open.md) tiver sido bem-sucedido, **ID3DXInclude:: Close** terá a garantia de ser chamado antes que a API que usa essa interface retorne.</span><span class="sxs-lookup"><span data-stu-id="ce631-120">If [**ID3DXInclude::Open**](id3dxinclude--open.md) was successful, **ID3DXInclude::Close** is guaranteed to be called before the API using this interface returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce631-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce631-121">Requirements</span></span>



| <span data-ttu-id="ce631-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce631-122">Requirement</span></span> | <span data-ttu-id="ce631-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ce631-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce631-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce631-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ce631-125"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce631-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ce631-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ce631-126">Library</span></span><br/> | <dl> <span data-ttu-id="ce631-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce631-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ce631-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce631-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce631-129">ID3DXInclude</span><span class="sxs-lookup"><span data-stu-id="ce631-129">ID3DXInclude</span></span>](id3dxinclude.md)
</dt> <dt>

[<span data-ttu-id="ce631-130">**ID3DXInclude:: abrir**</span><span class="sxs-lookup"><span data-stu-id="ce631-130">**ID3DXInclude::Open**</span></span>](id3dxinclude--open.md)
</dt> </dl>

 

 
