---
description: Use este método para readquirir recursos e salvar o estado inicial.
ms.assetid: 782f3537-f61c-4faa-a0b8-d60c516ba241
title: 'Método ID3DXEffect:: OnResetDevice (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.OnResetDevice
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d419ad456fcefbf0d6e4a201d4949556d6694e46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771514"
---
# <a name="id3dxeffectonresetdevice-method"></a><span data-ttu-id="8053b-103">Método ID3DXEffect:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="8053b-103">ID3DXEffect::OnResetDevice method</span></span>

<span data-ttu-id="8053b-104">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="8053b-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8053b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8053b-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="8053b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8053b-106">Parameters</span></span>

<span data-ttu-id="8053b-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8053b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8053b-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8053b-108">Return value</span></span>

<span data-ttu-id="8053b-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8053b-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8053b-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8053b-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8053b-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8053b-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8053b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8053b-112">Remarks</span></span>

<span data-ttu-id="8053b-113">**ID3DXEffect:: OnResetDevice** deve ser chamado cada vez que o dispositivo for redefinido (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes que quaisquer outros métodos sejam chamados.</span><span class="sxs-lookup"><span data-stu-id="8053b-113">**ID3DXEffect::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="8053b-114">Este é um bom lugar para readquirir recursos de memória de vídeo e capturar blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="8053b-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="8053b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8053b-115">Requirements</span></span>



| <span data-ttu-id="8053b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8053b-116">Requirement</span></span> | <span data-ttu-id="8053b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8053b-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8053b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8053b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8053b-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="8053b-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="8053b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8053b-120">Library</span></span><br/> | <dl> <span data-ttu-id="8053b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8053b-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8053b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8053b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8053b-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="8053b-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
