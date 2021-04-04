---
description: Alterna o modo para desenhar linhas no estilo OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'Método ID3DXLine:: SetGLLines (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103837982"
---
# <a name="id3dxlinesetgllines-method"></a><span data-ttu-id="4652c-103">Método ID3DXLine:: SetGLLines</span><span class="sxs-lookup"><span data-stu-id="4652c-103">ID3DXLine::SetGLLines method</span></span>

<span data-ttu-id="4652c-104">Alterna o modo para desenhar linhas no estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4652c-104">Toggles the mode to draw OpenGL-style lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="4652c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4652c-105">Syntax</span></span>


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a><span data-ttu-id="4652c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4652c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4652c-107">*bGLLines* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4652c-107">*bGLLines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4652c-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4652c-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4652c-109">Alterna o desenho de linha em estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4652c-109">Toggles OpenGL-style line drawing.</span></span> <span data-ttu-id="4652c-110">**True** habilita linhas em estilo OpenGL e **false** habilita linhas em estilo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4652c-110">**TRUE** enables OpenGL-style lines, and **FALSE** enables Direct3D-style lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4652c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4652c-111">Return value</span></span>

<span data-ttu-id="4652c-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4652c-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4652c-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4652c-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="4652c-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="4652c-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="4652c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4652c-115">Requirements</span></span>



| <span data-ttu-id="4652c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4652c-116">Requirement</span></span> | <span data-ttu-id="4652c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4652c-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4652c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4652c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4652c-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4652c-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="4652c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4652c-120">Library</span></span><br/> | <dl> <span data-ttu-id="4652c-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4652c-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4652c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4652c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4652c-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="4652c-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
