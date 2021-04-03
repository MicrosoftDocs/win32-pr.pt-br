---
description: Aplica um padrão Stipple à linha.
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'Método ID3DXLine:: setpattern (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091991"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="2e07a-103">Método ID3DXLine:: setpattern</span><span class="sxs-lookup"><span data-stu-id="2e07a-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="2e07a-104">Aplica um padrão Stipple à linha.</span><span class="sxs-lookup"><span data-stu-id="2e07a-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e07a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e07a-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="2e07a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e07a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e07a-107">*dwPattern* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2e07a-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e07a-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e07a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e07a-109">Descreve o padrão Stipple: 1 é opaco, 0 é transparente.</span><span class="sxs-lookup"><span data-stu-id="2e07a-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e07a-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e07a-110">Return value</span></span>

<span data-ttu-id="2e07a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2e07a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2e07a-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2e07a-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2e07a-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2e07a-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e07a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e07a-114">Requirements</span></span>



| <span data-ttu-id="2e07a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e07a-115">Requirement</span></span> | <span data-ttu-id="2e07a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2e07a-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e07a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e07a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2e07a-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e07a-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2e07a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e07a-119">Library</span></span><br/> | <dl> <span data-ttu-id="2e07a-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e07a-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e07a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e07a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e07a-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="2e07a-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
