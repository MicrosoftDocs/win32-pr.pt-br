---
description: Confirme as alterações feitas em uma malha para o dispositivo para que as alterações possam ser processadas. Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados. Uma malha não pode ser renderizada a menos que seja confirmada no dispositivo. Consulte Observações.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'Método ID3DX10Mesh:: CommitToDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012104"
---
# <a name="id3dx10meshcommittodevice-method"></a><span data-ttu-id="44993-106">Método ID3DX10Mesh:: CommitToDevice</span><span class="sxs-lookup"><span data-stu-id="44993-106">ID3DX10Mesh::CommitToDevice method</span></span>

<span data-ttu-id="44993-107">Confirme as alterações feitas em uma malha para o dispositivo para que as alterações possam ser processadas.</span><span class="sxs-lookup"><span data-stu-id="44993-107">Commit any changes made to a mesh to the device so that the changes can be rendered.</span></span> <span data-ttu-id="44993-108">Isso deve ser chamado depois que os dados de uma malha são alterados e antes de serem renderizados.</span><span class="sxs-lookup"><span data-stu-id="44993-108">This should be called after a mesh's data is altered and before it is rendered.</span></span> <span data-ttu-id="44993-109">Uma malha não pode ser renderizada a menos que seja confirmada no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="44993-109">A mesh cannot be rendered unless it is committed to the device.</span></span> <span data-ttu-id="44993-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="44993-110">See remarks.</span></span>

## <a name="syntax"></a><span data-ttu-id="44993-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44993-111">Syntax</span></span>


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a><span data-ttu-id="44993-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44993-112">Parameters</span></span>

<span data-ttu-id="44993-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="44993-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44993-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44993-114">Return value</span></span>

<span data-ttu-id="44993-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44993-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44993-116">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="44993-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44993-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="44993-117">Remarks</span></span>

<span data-ttu-id="44993-118">Quando uma malha é carregada, os dados são carregados em recursos de preparo, o que significa que os dados podem ser alterados, mas não renderizados.</span><span class="sxs-lookup"><span data-stu-id="44993-118">When a mesh is loaded, it's data is loaded into staging resources, meaning the data can be altered but not rendered.</span></span> <span data-ttu-id="44993-119">Quando CommitToDevice é chamado, os dados dos recursos de preparo são copiados nos recursos do dispositivo para que possam ser renderizados.</span><span class="sxs-lookup"><span data-stu-id="44993-119">When CommitToDevice is called, the data from the staging resources are copied into device resources so that they can be rendered.</span></span> <span data-ttu-id="44993-120">Embora os dados sejam confirmados no dispositivo, os recursos de preparo permanecem e podem ser modificados.</span><span class="sxs-lookup"><span data-stu-id="44993-120">Although the data is committed to the device, the staging resources remain and can be modified.</span></span> <span data-ttu-id="44993-121">Se forem feitas modificações nos recursos de preparo, os recursos de preparo deverão ser confirmados no dispositivo novamente para que essas alterações sejam processadas na tela.</span><span class="sxs-lookup"><span data-stu-id="44993-121">If any modifications are made to the staging resources, the staging resources must be committed to the device again in order for those changes to be rendered on screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="44993-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44993-122">Requirements</span></span>



| <span data-ttu-id="44993-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="44993-123">Requirement</span></span> | <span data-ttu-id="44993-124">Valor</span><span class="sxs-lookup"><span data-stu-id="44993-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44993-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44993-125">Header</span></span><br/>  | <dl> <span data-ttu-id="44993-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="44993-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="44993-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44993-127">Library</span></span><br/> | <dl> <span data-ttu-id="44993-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44993-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44993-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="44993-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44993-130">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="44993-130">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="44993-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="44993-131">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




