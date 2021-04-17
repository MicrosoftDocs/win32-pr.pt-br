---
description: Representa uma matriz 3x3 que, por sua vez, representa uma transformação afim.
ms.assetid: 79abff2e-d1d3-4a32-9ac2-f46c1b21f742
title: Classe InkTransform (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkTransform
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 61641f0fed8ec98321e155f82ff9a35150e7fdcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771295"
---
# <a name="inktransform-class"></a><span data-ttu-id="3781a-103">Classe InkTransform</span><span class="sxs-lookup"><span data-stu-id="3781a-103">InkTransform class</span></span>

<span data-ttu-id="3781a-104">Representa uma matriz 3x3 que, por sua vez, representa uma transformação afim.</span><span class="sxs-lookup"><span data-stu-id="3781a-104">Represents a 3x3 matrix that, in turn, represents an affine transformation.</span></span>

<span data-ttu-id="3781a-105">**InkTransform** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3781a-105">**InkTransform** has these types of members:</span></span>

-   [<span data-ttu-id="3781a-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="3781a-106">Methods</span></span>](#methods)
-   [<span data-ttu-id="3781a-107">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3781a-107">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3781a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="3781a-108">Methods</span></span>

<span data-ttu-id="3781a-109">A classe **InkTransform** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3781a-109">The **InkTransform** class has these methods.</span></span>



| <span data-ttu-id="3781a-110">Método</span><span class="sxs-lookup"><span data-stu-id="3781a-110">Method</span></span>                                                  | <span data-ttu-id="3781a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3781a-111">Description</span></span>                                                                                                                 |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3781a-112">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="3781a-112">**GetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform)       | <span data-ttu-id="3781a-113">Recupera o **InkTransform** como 6 floats.</span><span class="sxs-lookup"><span data-stu-id="3781a-113">Retrieves the **InkTransform** as 6 floats.</span></span><br/>                                                                      |
| [<span data-ttu-id="3781a-114">**Reflexão**</span><span class="sxs-lookup"><span data-stu-id="3781a-114">**Reflect**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect)                 | <span data-ttu-id="3781a-115">Reflete a transformação nas direções horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="3781a-115">Reflects the transform in either the horizontal or vertical directions.</span></span><br/>                                          |
| [<span data-ttu-id="3781a-116">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="3781a-116">**Reset**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset)                     | <span data-ttu-id="3781a-117">Redefine a transformação para seu estado original.</span><span class="sxs-lookup"><span data-stu-id="3781a-117">Resets the transform to its original state.</span></span><br/>                                                                      |
| [<span data-ttu-id="3781a-118">**Girar**</span><span class="sxs-lookup"><span data-stu-id="3781a-118">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate)                   | <span data-ttu-id="3781a-119">Gira a transformação por um ângulo medido em graus e, opcionalmente, especifica um ponto central para a rotação.</span><span class="sxs-lookup"><span data-stu-id="3781a-119">Rotates the transform by an angle measured in degrees, and optionally specifies a center point for the rotation.</span></span><br/> |
| [<span data-ttu-id="3781a-120">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="3781a-120">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-scaletransform) | <span data-ttu-id="3781a-121">Dimensiona a transformação por fatores X e Y.</span><span class="sxs-lookup"><span data-stu-id="3781a-121">Scales the transform by X and Y factors.</span></span><br/>                                                                         |
| [<span data-ttu-id="3781a-122">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="3781a-122">**SetTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform)       | <span data-ttu-id="3781a-123">Modifica o **InkTransform** usando 6 floats.</span><span class="sxs-lookup"><span data-stu-id="3781a-123">Modifies the **InkTransform** using 6 floats.</span></span><br/>                                                                    |
| [<span data-ttu-id="3781a-124">**Quantidade**</span><span class="sxs-lookup"><span data-stu-id="3781a-124">**Shear**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear)                     | <span data-ttu-id="3781a-125">Aplica uma distorção com os fatores horizontais e verticais especificados.</span><span class="sxs-lookup"><span data-stu-id="3781a-125">Applies a shear with the specified horizontal and vertical factors.</span></span><br/>                                              |
| [<span data-ttu-id="3781a-126">**Traduzir**</span><span class="sxs-lookup"><span data-stu-id="3781a-126">**Translate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate)             | <span data-ttu-id="3781a-127">Move a transformação pelos componentes horizontal e vertical especificados.</span><span class="sxs-lookup"><span data-stu-id="3781a-127">Moves the transform by the specified horizontal and vertical components.</span></span><br/>                                         |



 

### <a name="properties"></a><span data-ttu-id="3781a-128">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3781a-128">Properties</span></span>

<span data-ttu-id="3781a-129">A classe **InkTransform** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3781a-129">The **InkTransform** class has these properties.</span></span>



| <span data-ttu-id="3781a-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3781a-130">Property</span></span>                                     | <span data-ttu-id="3781a-131">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="3781a-131">Access type</span></span>           | <span data-ttu-id="3781a-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="3781a-132">Description</span></span>                                                                                          |
|:---------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3781a-133">**Dados**</span><span class="sxs-lookup"><span data-stu-id="3781a-133">**Data**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data)<br/> | <span data-ttu-id="3781a-134">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-134">Read/write</span></span><br/> | <span data-ttu-id="3781a-135">Obtém ou define a versão de automação do struct do XFORM do WIN32.</span><span class="sxs-lookup"><span data-stu-id="3781a-135">Gets or sets the Automation version of the WIN32 XFORM struct.</span></span><br/>                            |
| [<span data-ttu-id="3781a-136">**eDx**</span><span class="sxs-lookup"><span data-stu-id="3781a-136">**eDx**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx)<br/>   | <span data-ttu-id="3781a-137">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-137">Read/write</span></span><br/> | <span data-ttu-id="3781a-138">Obtém ou define o número real que especifica o elemento na terceira linha, primeira coluna.</span><span class="sxs-lookup"><span data-stu-id="3781a-138">Gets or sets the real number that specifies the element in the third row, first column.</span></span><br/>   |
| [<span data-ttu-id="3781a-139">**eDy**</span><span class="sxs-lookup"><span data-stu-id="3781a-139">**eDy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy)<br/>   | <span data-ttu-id="3781a-140">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-140">Read/write</span></span><br/> | <span data-ttu-id="3781a-141">Obtém ou define o número real que especifica o elemento na terceira linha, segunda coluna.</span><span class="sxs-lookup"><span data-stu-id="3781a-141">Gets or sets the real number that specifies the element in the third row, second column.</span></span><br/>  |
| [<span data-ttu-id="3781a-142">**eM11**</span><span class="sxs-lookup"><span data-stu-id="3781a-142">**eM11**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11)<br/> | <span data-ttu-id="3781a-143">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-143">Read/write</span></span><br/> | <span data-ttu-id="3781a-144">Obtém ou define o número real que especifica o elemento na primeira linha, primeira coluna.</span><span class="sxs-lookup"><span data-stu-id="3781a-144">Gets or sets the real number that specifies the element in the first row, first column.</span></span><br/>   |
| [<span data-ttu-id="3781a-145">**eM12**</span><span class="sxs-lookup"><span data-stu-id="3781a-145">**eM12**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12)<br/> | <span data-ttu-id="3781a-146">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-146">Read/write</span></span><br/> | <span data-ttu-id="3781a-147">Obtém ou define o número real que especifica o elemento na primeira linha, segunda coluna.</span><span class="sxs-lookup"><span data-stu-id="3781a-147">Gets or sets the real number that specifies the element in the first row, second column.</span></span><br/>  |
| [<span data-ttu-id="3781a-148">**eM21**</span><span class="sxs-lookup"><span data-stu-id="3781a-148">**eM21**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21)<br/> | <span data-ttu-id="3781a-149">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-149">Read/write</span></span><br/> | <span data-ttu-id="3781a-150">Obtém ou define o número real que especifica o elemento na segunda linha, primeira coluna.</span><span class="sxs-lookup"><span data-stu-id="3781a-150">Gets or sets the real number that specifies the element in the second row, first column.</span></span><br/>  |
| [<span data-ttu-id="3781a-151">**eM22**</span><span class="sxs-lookup"><span data-stu-id="3781a-151">**eM22**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22)<br/> | <span data-ttu-id="3781a-152">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3781a-152">Read/write</span></span><br/> | <span data-ttu-id="3781a-153">Obtém ou define o número real que especifica o elemento na segunda linha, segunda coluna.</span><span class="sxs-lookup"><span data-stu-id="3781a-153">Gets or sets the real number that specifies the element in the second row, second column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3781a-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="3781a-154">Remarks</span></span>

<span data-ttu-id="3781a-155">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="3781a-155">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="3781a-156">O objeto armazena apenas seis dos nove números em uma matriz de 3x3 porque todas as matrizes de 3x3 que representam as transformações de afinidade têm a mesma terceira coluna (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="3781a-156">The object stores only six of the nine numbers in a 3x3 matrix because all 3x3 matrices that represent affine transformations have the same third column (0, 0, 1).</span></span> <span data-ttu-id="3781a-157">Esse objeto, por sua vez, é usado para descrever as operações de transformação, como mover, distorcer, dimensionar ou girar em um objeto [**InkRenderer**](inkrenderer-class.md) , objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) ou coleção [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3781a-157">This object in turn is used to describe transformation operations such as moving, shearing, scaling, or rotating in an [**InkRenderer**](inkrenderer-class.md) object, [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object, or [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

> [!Note]  
> <span data-ttu-id="3781a-158">O objeto **InkTransform** se correlaciona com a estrutura [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) .</span><span class="sxs-lookup"><span data-stu-id="3781a-158">The **InkTransform** object correlates to the [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3781a-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3781a-159">Requirements</span></span>



| <span data-ttu-id="3781a-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="3781a-160">Requirement</span></span> | <span data-ttu-id="3781a-161">Valor</span><span class="sxs-lookup"><span data-stu-id="3781a-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3781a-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3781a-162">Minimum supported client</span></span><br/> | <span data-ttu-id="3781a-163">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3781a-163">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3781a-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3781a-164">Minimum supported server</span></span><br/> | <span data-ttu-id="3781a-165">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3781a-165">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3781a-166">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3781a-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="3781a-167"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3781a-167"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3781a-168">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3781a-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="3781a-169"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3781a-169"><dt>InkObj.dll</dt></span></span> </dl>                               |



 

