---
description: A interface ID3DXLine implementa o desenho de linha usando triângulos texturizados.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interface ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012186"
---
# <a name="id3dxline-interface"></a><span data-ttu-id="802b7-103">Interface ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="802b7-103">ID3DXLine interface</span></span>

<span data-ttu-id="802b7-104">A interface ID3DXLine implementa o desenho de linha usando triângulos texturizados.</span><span class="sxs-lookup"><span data-stu-id="802b7-104">The ID3DXLine interface implements line drawing using textured triangles.</span></span>

## <a name="members"></a><span data-ttu-id="802b7-105">Membros</span><span class="sxs-lookup"><span data-stu-id="802b7-105">Members</span></span>

<span data-ttu-id="802b7-106">A interface **ID3DXLine** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="802b7-106">The **ID3DXLine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="802b7-107">**ID3DXLine** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="802b7-107">**ID3DXLine** also has these types of members:</span></span>

-   [<span data-ttu-id="802b7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="802b7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="802b7-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="802b7-109">Methods</span></span>

<span data-ttu-id="802b7-110">A interface **ID3DXLine** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="802b7-110">The **ID3DXLine** interface has these methods.</span></span>



| <span data-ttu-id="802b7-111">Método</span><span class="sxs-lookup"><span data-stu-id="802b7-111">Method</span></span>                                                | <span data-ttu-id="802b7-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="802b7-112">Description</span></span>                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="802b7-113">**Começar**</span><span class="sxs-lookup"><span data-stu-id="802b7-113">**Begin**</span></span>](id3dxline--begin.md)                     | <span data-ttu-id="802b7-114">Prepara um dispositivo para linhas de desenho.</span><span class="sxs-lookup"><span data-stu-id="802b7-114">Prepares a device for drawing lines.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="802b7-115">**Draw**</span><span class="sxs-lookup"><span data-stu-id="802b7-115">**Draw**</span></span>](id3dxline--draw.md)                       | <span data-ttu-id="802b7-116">Desenha uma faixa de linha no espaço da tela.</span><span class="sxs-lookup"><span data-stu-id="802b7-116">Draws a line strip in screen space.</span></span> <span data-ttu-id="802b7-117">A entrada está na forma de uma matriz que define pontos (de [**D3DXVECTOR2**](d3dxvector2.md)) na faixa de linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-117">Input is in the form of an array that defines points (of [**D3DXVECTOR2**](d3dxvector2.md)) on the line strip.</span></span><br/>                                   |
| [<span data-ttu-id="802b7-118">**DrawTransform**</span><span class="sxs-lookup"><span data-stu-id="802b7-118">**DrawTransform**</span></span>](id3dxline--drawtransform.md)     | <span data-ttu-id="802b7-119">Desenha uma faixa de linha no espaço da tela com uma matriz de transformação de entrada especificada.</span><span class="sxs-lookup"><span data-stu-id="802b7-119">Draws a line strip in screen space with a specified input transformation matrix.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="802b7-120">**Completo**</span><span class="sxs-lookup"><span data-stu-id="802b7-120">**End**</span></span>](id3dxline--end.md)                         | <span data-ttu-id="802b7-121">Restaura o estado do dispositivo para como ele era quando [**ID3DXLine:: Begin**](id3dxline--begin.md) foi chamado.</span><span class="sxs-lookup"><span data-stu-id="802b7-121">Restores the device state to how it was when [**ID3DXLine::Begin**](id3dxline--begin.md) was called.</span></span><br/>                                                                                 |
| [<span data-ttu-id="802b7-122">**GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="802b7-122">**GetAntialias**</span></span>](id3dxline--getantialias.md)       | <span data-ttu-id="802b7-123">Obtém o estado de anti-aliasing da linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-123">Gets the line antialiasing state.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="802b7-124">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="802b7-124">**GetDevice**</span></span>](id3dxline--getdevice.md)             | <span data-ttu-id="802b7-125">Recupera o dispositivo Direct3D associado ao objeto line.</span><span class="sxs-lookup"><span data-stu-id="802b7-125">Retrieves the Direct3D device associated with the line object.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="802b7-126">**GetGLLines**</span><span class="sxs-lookup"><span data-stu-id="802b7-126">**GetGLLines**</span></span>](id3dxline--getgllines.md)           | <span data-ttu-id="802b7-127">Obtém o modo de desenho de linha no estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="802b7-127">Gets the OpenGL-style line-drawing mode.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="802b7-128">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="802b7-128">**GetPattern**</span></span>](id3dxline--getpattern.md)           | <span data-ttu-id="802b7-129">Obtém o padrão de Stipple de linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-129">Gets the line stipple pattern.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="802b7-130">**GetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="802b7-130">**GetPatternScale**</span></span>](id3dxline--getpatternscale.md) | <span data-ttu-id="802b7-131">Obtém o valor de escala Stipple-Pattern.</span><span class="sxs-lookup"><span data-stu-id="802b7-131">Gets the stipple-pattern scale value.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="802b7-132">**GetWidth**</span><span class="sxs-lookup"><span data-stu-id="802b7-132">**GetWidth**</span></span>](id3dxline--getwidth.md)               | <span data-ttu-id="802b7-133">Obtém a espessura da linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-133">Gets the thickness of the line.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="802b7-134">**OnLostDevice**</span><span class="sxs-lookup"><span data-stu-id="802b7-134">**OnLostDevice**</span></span>](id3dxline--onlostdevice.md)       | <span data-ttu-id="802b7-135">Use este método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks.</span><span class="sxs-lookup"><span data-stu-id="802b7-135">Use this method to release all references to video memory resources and delete all stateblocks.</span></span> <span data-ttu-id="802b7-136">Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="802b7-136">This method should be called whenever a device is lost, or before resetting a device.</span></span><br/> |
| [<span data-ttu-id="802b7-137">**OnResetDevice**</span><span class="sxs-lookup"><span data-stu-id="802b7-137">**OnResetDevice**</span></span>](id3dxline--onresetdevice.md)     | <span data-ttu-id="802b7-138">Use este método para readquirir recursos e salvar o estado inicial.</span><span class="sxs-lookup"><span data-stu-id="802b7-138">Use this method to re-acquire resources and save initial state.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="802b7-139">**SetAntialias**</span><span class="sxs-lookup"><span data-stu-id="802b7-139">**SetAntialias**</span></span>](id3dxline--setantialias.md)       | <span data-ttu-id="802b7-140">Alterna a suavização de linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-140">Toggles line antialiasing.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="802b7-141">**SetGLLines**</span><span class="sxs-lookup"><span data-stu-id="802b7-141">**SetGLLines**</span></span>](id3dxline--setgllines.md)           | <span data-ttu-id="802b7-142">Alterna o modo para desenhar linhas no estilo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="802b7-142">Toggles the mode to draw OpenGL-style lines.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="802b7-143">**Setpattern**</span><span class="sxs-lookup"><span data-stu-id="802b7-143">**SetPattern**</span></span>](id3dxline--setpattern.md)           | <span data-ttu-id="802b7-144">Aplica um padrão Stipple à linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-144">Applies a stipple pattern to the line.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="802b7-145">**SetPatternScale**</span><span class="sxs-lookup"><span data-stu-id="802b7-145">**SetPatternScale**</span></span>](id3dxline--setpatternscale.md) | <span data-ttu-id="802b7-146">Amplia o padrão Stipple ao longo da direção da linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-146">Stretches the stipple pattern along the line direction.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="802b7-147">**SetWidth**</span><span class="sxs-lookup"><span data-stu-id="802b7-147">**SetWidth**</span></span>](id3dxline--setwidth.md)               | <span data-ttu-id="802b7-148">Especifica a espessura da linha.</span><span class="sxs-lookup"><span data-stu-id="802b7-148">Specifies the thickness of the line.</span></span><br/>                                                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="802b7-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="802b7-149">Remarks</span></span>

<span data-ttu-id="802b7-150">Crie um objeto de desenho de linha com [**D3DXCreateLine**](d3dxcreateline.md).</span><span class="sxs-lookup"><span data-stu-id="802b7-150">Create a line drawing object with [**D3DXCreateLine**](d3dxcreateline.md).</span></span>

<span data-ttu-id="802b7-151">O tipo LPD3DXLINE é definido como um ponteiro para a interface **ID3DXLine** .</span><span class="sxs-lookup"><span data-stu-id="802b7-151">The LPD3DXLINE type is defined as a pointer to the **ID3DXLine** interface.</span></span>


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a><span data-ttu-id="802b7-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="802b7-152">Requirements</span></span>



| <span data-ttu-id="802b7-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="802b7-153">Requirement</span></span> | <span data-ttu-id="802b7-154">Valor</span><span class="sxs-lookup"><span data-stu-id="802b7-154">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="802b7-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="802b7-155">Header</span></span><br/>  | <dl> <span data-ttu-id="802b7-156"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="802b7-156"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="802b7-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="802b7-157">Library</span></span><br/> | <dl> <span data-ttu-id="802b7-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="802b7-158"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="802b7-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="802b7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="802b7-160">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="802b7-160">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
