---
description: Prepara um dispositivo para linhas de desenho.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'Método ID3DXLine:: Begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105788849"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="06929-103">Método ID3DXLine:: Begin</span><span class="sxs-lookup"><span data-stu-id="06929-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="06929-104">Prepara um dispositivo para linhas de desenho.</span><span class="sxs-lookup"><span data-stu-id="06929-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="06929-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="06929-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="06929-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="06929-106">Parameters</span></span>

<span data-ttu-id="06929-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="06929-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06929-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="06929-108">Return value</span></span>

<span data-ttu-id="06929-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06929-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06929-110">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06929-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="06929-111">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="06929-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="06929-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="06929-112">Remarks</span></span>

<span data-ttu-id="06929-113">Chamar **ID3DXLine:: Begin** é opcional.</span><span class="sxs-lookup"><span data-stu-id="06929-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="06929-114">Se chamado fora de uma sequência ID3DXLine:: Begin/ID3DXLine:: end, as funções de desenho chamarão internamente ID3DXLine:: Begin e ID3DXLine:: end.</span><span class="sxs-lookup"><span data-stu-id="06929-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="06929-115">Para evitar sobrecarga extra, esse método deve ser usado se mais de uma função de desenho for chamada sucessivamente.</span><span class="sxs-lookup"><span data-stu-id="06929-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="06929-116">Esse método deve ser chamado de dentro de uma sequência [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9:: endcena**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="06929-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="06929-117">ID3DXLine:: Begin não pode ser usado como um substituto para [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) ou [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="06929-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="06929-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06929-118">Requirements</span></span>



| <span data-ttu-id="06929-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06929-119">Requirement</span></span> | <span data-ttu-id="06929-120">Valor</span><span class="sxs-lookup"><span data-stu-id="06929-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06929-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06929-121">Header</span></span><br/>  | <dl> <span data-ttu-id="06929-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="06929-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="06929-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="06929-123">Library</span></span><br/> | <dl> <span data-ttu-id="06929-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06929-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06929-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="06929-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06929-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="06929-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
