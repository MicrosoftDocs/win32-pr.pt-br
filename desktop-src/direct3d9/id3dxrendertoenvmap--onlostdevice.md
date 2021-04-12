---
description: Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.
ms.assetid: 76dcf5f3-0d2f-4388-9b75-c4dbd1c74982
title: 'Método ID3DXRenderToEnvMap:: OnLostDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.OnLostDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b644ab595fd8bc6ebdfa544cc004598f5570d262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298554"
---
# <a name="id3dxrendertoenvmaponlostdevice-method"></a><span data-ttu-id="354ab-104">Método ID3DXRenderToEnvMap:: OnLostDevice</span><span class="sxs-lookup"><span data-stu-id="354ab-104">ID3DXRenderToEnvMap::OnLostDevice method</span></span>

<span data-ttu-id="354ab-105">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="354ab-105">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="354ab-106">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="354ab-106">This method should be called whenever a device is lost, or before resetting a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="354ab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="354ab-107">Syntax</span></span>


```C++
HRESULT OnLostDevice();
```



## <a name="parameters"></a><span data-ttu-id="354ab-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="354ab-108">Parameters</span></span>

<span data-ttu-id="354ab-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="354ab-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="354ab-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="354ab-110">Return value</span></span>

<span data-ttu-id="354ab-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="354ab-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="354ab-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="354ab-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="354ab-113">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="354ab-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="354ab-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="354ab-114">Remarks</span></span>

<span data-ttu-id="354ab-115">Esse método deve ser chamado sempre que o dispositivo for perdido ou antes que o usuário chame [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="354ab-115">This method should be called whenever the device is lost or before the user calls [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="354ab-116">Mesmo que o dispositivo não tenha sido realmente perdido, **ID3DXRenderToEnvMap:: OnLostDevice** é responsável por liberar stateblocks e outros recursos que talvez precisem ser liberados antes de redefinir o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="354ab-116">Even if the device was not actually lost, **ID3DXRenderToEnvMap::OnLostDevice** is responsible for freeing stateblocks and other resources that may need to be released before resetting the device.</span></span> <span data-ttu-id="354ab-117">Como resultado, o objeto Font não pode ser usado novamente antes de chamar **IDirect3DDevice9:: Reset** e, em seguida, [**ID3DXRenderToEnvMap:: OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span><span class="sxs-lookup"><span data-stu-id="354ab-117">As a result, the font object cannot be used again before calling **IDirect3DDevice9::Reset** and then [**ID3DXRenderToEnvMap::OnResetDevice**](id3dxrendertoenvmap--onresetdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="354ab-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="354ab-118">Requirements</span></span>



| <span data-ttu-id="354ab-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="354ab-119">Requirement</span></span> | <span data-ttu-id="354ab-120">Valor</span><span class="sxs-lookup"><span data-stu-id="354ab-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="354ab-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="354ab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="354ab-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="354ab-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="354ab-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="354ab-123">Library</span></span><br/> | <dl> <span data-ttu-id="354ab-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="354ab-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="354ab-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="354ab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354ab-126">ID3DXRenderToEnvMap</span><span class="sxs-lookup"><span data-stu-id="354ab-126">ID3DXRenderToEnvMap</span></span>](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




