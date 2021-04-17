---
description: Alterna a suavização de linha.
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'Método ID3DXLine:: SetAntialias (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813437"
---
# <a name="id3dxlinesetantialias-method"></a><span data-ttu-id="86eb4-103">Método ID3DXLine:: SetAntialias</span><span class="sxs-lookup"><span data-stu-id="86eb4-103">ID3DXLine::SetAntialias method</span></span>

<span data-ttu-id="86eb4-104">Alterna a suavização de linha.</span><span class="sxs-lookup"><span data-stu-id="86eb4-104">Toggles line antialiasing.</span></span>

## <a name="syntax"></a><span data-ttu-id="86eb4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86eb4-105">Syntax</span></span>


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a><span data-ttu-id="86eb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86eb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86eb4-107">*bAntiAlias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86eb4-107">*bAntiAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86eb4-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="86eb4-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="86eb4-109">Alterna para ativar e desativar a suavização.</span><span class="sxs-lookup"><span data-stu-id="86eb4-109">Toggles antialiasing on and off.</span></span> <span data-ttu-id="86eb4-110">**True** ativa a suavização e **false** desliga a desativação.</span><span class="sxs-lookup"><span data-stu-id="86eb4-110">**TRUE** turns antialiasing on, and **FALSE** turns antialiasing off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86eb4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86eb4-111">Return value</span></span>

<span data-ttu-id="86eb4-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="86eb4-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="86eb4-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="86eb4-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="86eb4-114">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="86eb4-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="86eb4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86eb4-115">Requirements</span></span>



| <span data-ttu-id="86eb4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="86eb4-116">Requirement</span></span> | <span data-ttu-id="86eb4-117">Valor</span><span class="sxs-lookup"><span data-stu-id="86eb4-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86eb4-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86eb4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="86eb4-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="86eb4-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="86eb4-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86eb4-120">Library</span></span><br/> | <dl> <span data-ttu-id="86eb4-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86eb4-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86eb4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="86eb4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86eb4-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="86eb4-123">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="86eb4-124">**ID3DXLine::GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="86eb4-124">**ID3DXLine::GetAntialias**</span></span>](id3dxline--getantialias.md)
</dt> </dl>

 

 
