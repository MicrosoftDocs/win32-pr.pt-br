---
description: Use este método para readquirir recursos e salvar o estado inicial.
ms.assetid: beca7a51-e799-4e03-81a3-218552231428
title: 'Método ID3DXLine:: OnResetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.OnResetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c85a93084e3a4f3d8308e5111338d0c5127e22c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810622"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="15d6a-103">Método ID3DXLine:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="15d6a-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="15d6a-104">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="15d6a-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d6a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15d6a-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="15d6a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15d6a-106">Parameters</span></span>

<span data-ttu-id="15d6a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15d6a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15d6a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15d6a-108">Return value</span></span>

<span data-ttu-id="15d6a-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15d6a-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15d6a-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15d6a-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="15d6a-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="15d6a-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="15d6a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="15d6a-112">Remarks</span></span>

<span data-ttu-id="15d6a-113">**ID3DXLine:: OnResetDevice** deve ser chamado cada vez que o dispositivo for redefinido (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes que quaisquer outros métodos sejam chamados.</span><span class="sxs-lookup"><span data-stu-id="15d6a-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="15d6a-114">Este é um bom lugar para readquirir recursos de memória de vídeo e capturar blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="15d6a-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="15d6a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15d6a-115">Requirements</span></span>



| <span data-ttu-id="15d6a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d6a-116">Requirement</span></span> | <span data-ttu-id="15d6a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="15d6a-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="15d6a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15d6a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="15d6a-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="15d6a-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="15d6a-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="15d6a-120">Library</span></span><br/> | <dl> <span data-ttu-id="15d6a-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15d6a-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="15d6a-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="15d6a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d6a-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="15d6a-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
