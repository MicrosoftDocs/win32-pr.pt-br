---
description: Obtém uma descrição do objeto de fonte atual. GetDescW e getdescum são idênticos a esse método, exceto que um ponteiro é retornado para uma \_ estrutura D3DXFONT DESCW ou D3DXFONT \_ desca, respectivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'Método ID3DXFont:: GetDesc (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798542"
---
# <a name="id3dxfontgetdesc-method"></a><span data-ttu-id="ea17d-104">Método ID3DXFont:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="ea17d-104">ID3DXFont::GetDesc method</span></span>

<span data-ttu-id="ea17d-105">Obtém uma descrição do objeto de fonte atual.</span><span class="sxs-lookup"><span data-stu-id="ea17d-105">Gets a description of the current font object.</span></span> <span data-ttu-id="ea17d-106">GetDescW e getdescum são idênticos a esse método, exceto que um ponteiro é retornado para uma estrutura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) ou **D3DXFONT \_ desca** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ea17d-106">GetDescW and GetDescA are identical to this method, except that a pointer is returned to a [**D3DXFONT\_DESCW**](d3dxfont-desc.md) or **D3DXFONT\_DESCA** structure, respectively.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea17d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea17d-107">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ea17d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea17d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea17d-109">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ea17d-109">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea17d-110">Tipo: **[ **D3DXFONT \_ desc**](d3dxfont-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea17d-110">Type: **[**D3DXFONT\_DESC**](d3dxfont-desc.md)\***</span></span>

<span data-ttu-id="ea17d-111">Ponteiro para uma [**estrutura \_ desc de D3DXFONT**](d3dxfont-desc.md) que descreve o objeto Font.</span><span class="sxs-lookup"><span data-stu-id="ea17d-111">Pointer to a [**D3DXFONT\_DESC**](d3dxfont-desc.md) structure that describes the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea17d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea17d-112">Return value</span></span>

<span data-ttu-id="ea17d-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea17d-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea17d-114">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea17d-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ea17d-115">Se o método falhar, o seguinte valor será retornado: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ea17d-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea17d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea17d-116">Remarks</span></span>

<span data-ttu-id="ea17d-117">Esse método descreverá os objetos de fonte Unicode se o UNICODE estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ea17d-117">This method describes Unicode font objects if UNICODE is defined.</span></span> <span data-ttu-id="ea17d-118">Caso contrário, getdesca é chamado, que retorna um ponteiro para a estrutura [**\_ desca D3DXFONT**](d3dxfont-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="ea17d-118">Otherwise GetDescA is called, which returns a pointer to the [**D3DXFONT\_DESCA**](d3dxfont-desc.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea17d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea17d-119">Requirements</span></span>



| <span data-ttu-id="ea17d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea17d-120">Requirement</span></span> | <span data-ttu-id="ea17d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ea17d-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ea17d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea17d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ea17d-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="ea17d-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea17d-124">Library</span></span><br/> | <dl> <span data-ttu-id="ea17d-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea17d-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ea17d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea17d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea17d-127">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="ea17d-127">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 




