---
description: Define as constantes para seus valores padrão. Os valores padrão são declarados nas declarações de variável no sombreador.
ms.assetid: 593a3a1b-cf96-4d46-9917-21068def0988
title: 'Método ID3DXConstantTable:: SetDefaults (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetDefaults
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed49e626c979f7146b42078cf1f65fdd6716efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664013"
---
# <a name="id3dxconstanttablesetdefaults-method"></a><span data-ttu-id="2f465-104">Método ID3DXConstantTable:: SetDefaults</span><span class="sxs-lookup"><span data-stu-id="2f465-104">ID3DXConstantTable::SetDefaults method</span></span>

<span data-ttu-id="2f465-105">Define as constantes para seus valores padrão.</span><span class="sxs-lookup"><span data-stu-id="2f465-105">Sets the constants to their default values.</span></span> <span data-ttu-id="2f465-106">Os valores padrão são declarados nas declarações de variável no sombreador.</span><span class="sxs-lookup"><span data-stu-id="2f465-106">The default values are declared in the variable declarations in the shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f465-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f465-107">Syntax</span></span>


```C++
HRESULT SetDefaults(
  [in] LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="2f465-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f465-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f465-109">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f465-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f465-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2f465-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2f465-111">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à tabela constante.</span><span class="sxs-lookup"><span data-stu-id="2f465-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f465-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f465-112">Return value</span></span>

<span data-ttu-id="2f465-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f465-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f465-114">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f465-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2f465-115">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="2f465-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f465-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f465-116">Requirements</span></span>



| <span data-ttu-id="2f465-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f465-117">Requirement</span></span> | <span data-ttu-id="2f465-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2f465-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f465-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f465-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2f465-120"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f465-120"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2f465-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f465-121">Library</span></span><br/> | <dl> <span data-ttu-id="2f465-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f465-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2f465-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f465-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f465-124">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2f465-124">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
