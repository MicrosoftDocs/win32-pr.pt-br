---
description: Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.
ms.assetid: 8962236d-4801-46a3-9944-a7c4ad762882
title: 'Método ID3DXRenderToSurface:: OnLostDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 18e759fb12cd13c30cf3318b7208f87f824ab9cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298815"
---
# <a name="id3dxrendertosurfaceonlostdevice-method"></a><span data-ttu-id="975f3-104">Método ID3DXRenderToSurface:: OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="975f3-104">ID3DXRenderToSurface::OnLostDevice method</span></span>

<span data-ttu-id="975f3-105">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="975f3-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="975f3-106">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="975f3-106">This method should be called whenever a device is lost or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="975f3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="975f3-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="975f3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="975f3-108">Parameters</span></span>

<span data-ttu-id="975f3-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="975f3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="975f3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="975f3-110">Return value</span></span>

<span data-ttu-id="975f3-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="975f3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="975f3-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="975f3-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="975f3-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="975f3-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="975f3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="975f3-114">Remarks</span></span>

<span data-ttu-id="975f3-115">Esse método deve ser chamado sempre que o dispositivo for perdido ou antes que o usuário chame [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span><span class="sxs-lookup"><span data-stu-id="975f3-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset).</span></span> <span data-ttu-id="975f3-116">Mesmo que o dispositivo não tenha sido realmente perdido, ID3DXRenderToSurface:: OnLostDevice é responsável por liberar stateblocks e outros recursos que talvez precisem ser liberados antes de redefinir o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="975f3-116">Even if the device was not actually lost, ID3DXRenderToSurface::OnLostDevice is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="975f3-117">Como resultado, o objeto Font não pode ser usado novamente antes de chamar **IDirect3DDevice9:: Reset** e, em seguida, ID3DXRenderToSurface:: OnResetDevice.</span><span class="sxs-lookup"><span data-stu-id="975f3-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then ID3DXRenderToSurface::OnResetDevice.</span></span>

## <a name="requirements"></a><span data-ttu-id="975f3-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="975f3-118">Requirements</span></span>



| <span data-ttu-id="975f3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="975f3-119">Requirement</span></span> | <span data-ttu-id="975f3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="975f3-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="975f3-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="975f3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="975f3-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="975f3-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="975f3-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="975f3-123">Library</span></span><br/> | <dl> <span data-ttu-id="975f3-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="975f3-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="975f3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="975f3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="975f3-126">ID3DXRenderToSurface</span><span class="sxs-lookup"><span data-stu-id="975f3-126">ID3DXRenderToSurface</span></span>](id3dxrendertosurface.md)
</dt> </dl>

 

 
