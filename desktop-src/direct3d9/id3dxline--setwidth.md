---
description: Especifica a espessura da linha.
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'Método ID3DXLine:: SetWidth (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012162"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="9e323-103">Método ID3DXLine:: SetWidth</span><span class="sxs-lookup"><span data-stu-id="9e323-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="9e323-104">Especifica a espessura da linha.</span><span class="sxs-lookup"><span data-stu-id="9e323-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e323-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e323-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="9e323-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e323-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e323-107">*fWidth* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e323-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e323-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e323-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e323-109">Descreve a largura da linha.</span><span class="sxs-lookup"><span data-stu-id="9e323-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e323-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e323-110">Return value</span></span>

<span data-ttu-id="9e323-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e323-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e323-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e323-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9e323-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9e323-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e323-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e323-114">Requirements</span></span>



| <span data-ttu-id="9e323-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e323-115">Requirement</span></span> | <span data-ttu-id="9e323-116">Valor</span><span class="sxs-lookup"><span data-stu-id="9e323-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e323-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e323-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9e323-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e323-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="9e323-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e323-119">Library</span></span><br/> | <dl> <span data-ttu-id="9e323-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e323-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e323-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e323-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e323-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="9e323-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
