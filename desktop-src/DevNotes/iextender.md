---
description: A interface IExtender fornece um conjunto de propriedades básicas que são adicionadas à interface de um controle. Os programadores podem usar essas propriedades como se fossem parte do controle.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Interface IExtender
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: fd600de816889e1c644a0e6074d9b8a97e0ec80c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749653"
---
# <a name="iextender-interface"></a><span data-ttu-id="0786a-104">Interface IExtender</span><span class="sxs-lookup"><span data-stu-id="0786a-104">IExtender interface</span></span>

<span data-ttu-id="0786a-105">A interface **IExtender** fornece um conjunto de propriedades básicas que são adicionadas à interface de um controle.</span><span class="sxs-lookup"><span data-stu-id="0786a-105">The **IExtender** interface provides a set of basic properties that are added to the interface of a control.</span></span> <span data-ttu-id="0786a-106">Os programadores podem usar essas propriedades como se fossem parte do controle.</span><span class="sxs-lookup"><span data-stu-id="0786a-106">Programmers can use these properties as if they were part of the control.</span></span>

## <a name="members"></a><span data-ttu-id="0786a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="0786a-107">Members</span></span>

<span data-ttu-id="0786a-108">A interface **IExtender** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0786a-108">The **IExtender** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0786a-109">**IExtender** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0786a-109">**IExtender** also has these types of members:</span></span>

-   [<span data-ttu-id="0786a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0786a-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0786a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0786a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0786a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0786a-112">Methods</span></span>

<span data-ttu-id="0786a-113">A interface **IExtender** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0786a-113">The **IExtender** interface has these methods.</span></span>



| <span data-ttu-id="0786a-114">Método</span><span class="sxs-lookup"><span data-stu-id="0786a-114">Method</span></span>                         | <span data-ttu-id="0786a-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="0786a-115">Description</span></span>                                    |
|:-------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="0786a-116">**Mover**</span><span class="sxs-lookup"><span data-stu-id="0786a-116">**Move**</span></span>](iextender-move.md) | <span data-ttu-id="0786a-117">Move um MDIForm, formulário ou controle.</span><span class="sxs-lookup"><span data-stu-id="0786a-117">Moves an MDIForm, form, or control.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0786a-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0786a-118">Properties</span></span>

<span data-ttu-id="0786a-119">A interface **IExtender** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0786a-119">The **IExtender** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0786a-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="0786a-120">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0786a-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="0786a-121">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0786a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="0786a-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0786a-123">Alinhar</span><span class="sxs-lookup"><span data-stu-id="0786a-123">Align</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0786a-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-124">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="0786a-125">Retorna ou define um valor que determina se um objeto é exibido em qualquer tamanho em qualquer lugar em um formulário ou se é exibido na parte superior, inferior, esquerda ou direita do formulário e é dimensionado automaticamente para se ajustar à largura do formulário.</span><span class="sxs-lookup"><span data-stu-id="0786a-125">Returns or sets a value that determines whether an object is displayed in any size anywhere on a form or whether it is displayed at the top, bottom, left, or right of the form and is automatically sized to fit the width of the form.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0786a-126">Constante</span><span class="sxs-lookup"><span data-stu-id="0786a-126">Constant</span></span></th>
<th><span data-ttu-id="0786a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="0786a-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0786a-128">vbAlignNone 0</span><span class="sxs-lookup"><span data-stu-id="0786a-128">vbAlignNone 0</span></span></td>
<td><span data-ttu-id="0786a-129">(Padrão em um formulário não MDI) Nenhum — o tamanho e o local podem ser definidos em tempo de design ou em código.</span><span class="sxs-lookup"><span data-stu-id="0786a-129">(Default in a non-MDI form) None—size and location can be set at design time or in code.</span></span> <span data-ttu-id="0786a-130">A configuração será ignorada se o objeto estiver em um formulário MDI.</span><span class="sxs-lookup"><span data-stu-id="0786a-130">The setting is ignored if the object is on an MDI form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0786a-131">vbAlignTop 1</span><span class="sxs-lookup"><span data-stu-id="0786a-131">vbAlignTop 1</span></span></td>
<td><span data-ttu-id="0786a-132">(Padrão em um formulário MDI) Top — o objeto está na parte superior do formulário e sua largura é igual à configuração da propriedade LarguraDaEscala do formulário.</span><span class="sxs-lookup"><span data-stu-id="0786a-132">(Default in an MDI form) Top—the object is at the top of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0786a-133">vbAlignBottom 2</span><span class="sxs-lookup"><span data-stu-id="0786a-133">vbAlignBottom 2</span></span></td>
<td><span data-ttu-id="0786a-134">Inferior – o objeto está na parte inferior do formulário e sua largura é igual à configuração da propriedade LarguraDaEscala do formulário.</span><span class="sxs-lookup"><span data-stu-id="0786a-134">Bottom—the object is at the bottom of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0786a-135">vbAlignLeft 3</span><span class="sxs-lookup"><span data-stu-id="0786a-135">vbAlignLeft 3</span></span></td>
<td><span data-ttu-id="0786a-136">Esquerda — o objeto está à esquerda do formulário e sua largura é igual à configuração da propriedade LarguraDaEscala do formulário.</span><span class="sxs-lookup"><span data-stu-id="0786a-136">Left—the object is at the left of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0786a-137">vbAlignRight 4</span><span class="sxs-lookup"><span data-stu-id="0786a-137">vbAlignRight 4</span></span></td>
<td><span data-ttu-id="0786a-138">Direita — o objeto está à direita do formulário e sua largura é igual à configuração da propriedade LarguraDaEscala do formulário.</span><span class="sxs-lookup"><span data-stu-id="0786a-138">Right—the object is at the right of the form, and its width is equal to the ScaleWidth property setting of the form.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="0786a-139">Contêiner</span><span class="sxs-lookup"><span data-stu-id="0786a-139">Container</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-140">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0786a-140">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-141">Retorna o contêiner de um controle em um formulário.</span><span class="sxs-lookup"><span data-stu-id="0786a-141">Returns the container of a control on a form.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="0786a-142">habilitado</span><span class="sxs-lookup"><span data-stu-id="0786a-142">Enabled</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-143">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-144">Retorna ou define um valor que determina se um formulário ou controle pode responder a eventos gerados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0786a-144">Returns or sets a value that determines whether a form or control can respond to user-generated events.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="0786a-145">Altura</span><span class="sxs-lookup"><span data-stu-id="0786a-145">Height</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-146">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-147">Retorna ou define a altura de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0786a-147">Returns or sets the height of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="0786a-148">HWND</span><span class="sxs-lookup"><span data-stu-id="0786a-148">Hwnd</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-149">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0786a-149">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-150">Retorna um identificador para um formulário ou controle.</span><span class="sxs-lookup"><span data-stu-id="0786a-150">Returns a handle to a form or control.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="0786a-151">Esquerda</span><span class="sxs-lookup"><span data-stu-id="0786a-151">Left</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-152">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-152">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-153">Retorna ou define a distância entre a borda esquerda interna de um objeto e a borda esquerda de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="0786a-153">Returns or sets the distance between the internal left edge of an object and the left edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="0786a-154">Nome</span><span class="sxs-lookup"><span data-stu-id="0786a-154">Name</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-155">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0786a-155">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-156">Retorna o nome usado no código para identificar um formulário, controle ou objeto de acesso a dados.</span><span class="sxs-lookup"><span data-stu-id="0786a-156">Returns the name used in code to identify a form, control, or data access object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="0786a-157">Pai</span><span class="sxs-lookup"><span data-stu-id="0786a-157">Parent</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-158">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0786a-158">Read-only</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-159">Retorna o formulário, o objeto ou a coleção que contém um controle ou outro objeto ou coleção.</span><span class="sxs-lookup"><span data-stu-id="0786a-159">Returns the form, object, or collection that contains a control or another object or collection.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="0786a-160">TabStop</span><span class="sxs-lookup"><span data-stu-id="0786a-160">TabStop</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-161">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-161">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-162">Retorna ou define um valor que indica se um usuário pode usar a tecla <strong>Tab</strong> para dar o foco a um objeto.</span><span class="sxs-lookup"><span data-stu-id="0786a-162">Returns or sets a value that indicates whether a user can use the <strong>Tab</strong> key to give the focus to an object.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="0786a-163">Parte superior</span><span class="sxs-lookup"><span data-stu-id="0786a-163">Top</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-164">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-164">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-165">Retorna ou define a distância entre a borda superior interna de um objeto e a borda superior de seu contêiner.</span><span class="sxs-lookup"><span data-stu-id="0786a-165">Returns or sets the distance between the internal top edge of an object and the top edge of its container.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><p><span data-ttu-id="0786a-166">Visible</span><span class="sxs-lookup"><span data-stu-id="0786a-166">Visible</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-167">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-167">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-168">Retorna ou define um valor que indica se um objeto está visível ou oculto.</span><span class="sxs-lookup"><span data-stu-id="0786a-168">Returns or sets a value that indicates whether an object is visible or hidden.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><p><span data-ttu-id="0786a-169">Largura</span><span class="sxs-lookup"><span data-stu-id="0786a-169">Width</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-170">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="0786a-170">Read/write</span></span></p></td>
<td style="text-align: left;"><p><span data-ttu-id="0786a-171">Retorna ou define a largura de um objeto.</span><span class="sxs-lookup"><span data-stu-id="0786a-171">Returns or sets the width of an object.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="0786a-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0786a-172">Requirements</span></span>



| <span data-ttu-id="0786a-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="0786a-173">Requirement</span></span> | <span data-ttu-id="0786a-174">Valor</span><span class="sxs-lookup"><span data-stu-id="0786a-174">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0786a-175">DLL</span><span class="sxs-lookup"><span data-stu-id="0786a-175">DLL</span></span><br/> | <dl> <span data-ttu-id="0786a-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0786a-176"><dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt></span></span> </dl> |



 

 
