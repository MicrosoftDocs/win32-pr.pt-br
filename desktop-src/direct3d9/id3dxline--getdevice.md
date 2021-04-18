---
description: Recupera o dispositivo Direct3D associado ao objeto line.
ms.assetid: 42459668-aa18-478d-82d9-b8b25dc4a898
title: 'Método ID3DXLine:: GetDevice (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a97edf37d14edce4982d62d76f9429091ad491ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759791"
---
# <a name="id3dxlinegetdevice-method"></a><span data-ttu-id="c48d0-103">Método ID3DXLine:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="c48d0-103">ID3DXLine::GetDevice method</span></span>

<span data-ttu-id="c48d0-104">Recupera o dispositivo Direct3D associado ao objeto line.</span><span class="sxs-lookup"><span data-stu-id="c48d0-104">Retrieves the Direct3D device associated with the line object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c48d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c48d0-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="c48d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c48d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c48d0-107">*ppDevice* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c48d0-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c48d0-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="c48d0-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="c48d0-109">Endereço de um ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , que representa o objeto de dispositivo Direct3D associado ao objeto line.</span><span class="sxs-lookup"><span data-stu-id="c48d0-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the line object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c48d0-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c48d0-110">Return value</span></span>

<span data-ttu-id="c48d0-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c48d0-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c48d0-112">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c48d0-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c48d0-113">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="c48d0-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="c48d0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c48d0-114">Requirements</span></span>



| <span data-ttu-id="c48d0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c48d0-115">Requirement</span></span> | <span data-ttu-id="c48d0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c48d0-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c48d0-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c48d0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c48d0-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c48d0-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c48d0-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c48d0-119">Library</span></span><br/> | <dl> <span data-ttu-id="c48d0-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c48d0-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c48d0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c48d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c48d0-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="c48d0-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
