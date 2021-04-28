---
description: 'Método ID3DXLine:: OnResetDevice – Use este método para adquirir novamente os recursos e salvar o estado inicial.'
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
ms.openlocfilehash: f7e1275e7a7ec894601dc67503e25e1fa82545f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093654"
---
# <a name="id3dxlineonresetdevice-method"></a><span data-ttu-id="cc925-103">Método ID3DXLine:: OnResetDevice</span><span class="sxs-lookup"><span data-stu-id="cc925-103">ID3DXLine::OnResetDevice method</span></span>

<span data-ttu-id="cc925-104">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="cc925-104">Use this method to re-acquire resources and save initial state.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc925-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc925-105">Syntax</span></span>


```C++
HRESULT OnResetDevice();
```



## <a name="parameters"></a><span data-ttu-id="cc925-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc925-106">Parameters</span></span>

<span data-ttu-id="cc925-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cc925-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc925-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="cc925-108">Return value</span></span>

<span data-ttu-id="cc925-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc925-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc925-110">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc925-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cc925-111">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="cc925-111">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc925-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc925-112">Remarks</span></span>

<span data-ttu-id="cc925-113">**ID3DXLine:: OnResetDevice** deve ser chamado cada vez que o dispositivo for redefinido (usando [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), antes que quaisquer outros métodos sejam chamados.</span><span class="sxs-lookup"><span data-stu-id="cc925-113">**ID3DXLine::OnResetDevice** should be called each time the device is reset (using [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)), before any other methods are called.</span></span> <span data-ttu-id="cc925-114">Este é um bom lugar para readquirir recursos de memória de vídeo e capturar blocos de estado.</span><span class="sxs-lookup"><span data-stu-id="cc925-114">This is a good place to re-acquire video-memory resources and capture state blocks.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc925-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc925-115">Requirements</span></span>



| <span data-ttu-id="cc925-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc925-116">Requirement</span></span> | <span data-ttu-id="cc925-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cc925-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc925-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc925-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc925-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc925-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cc925-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc925-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc925-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc925-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc925-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cc925-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc925-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="cc925-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
