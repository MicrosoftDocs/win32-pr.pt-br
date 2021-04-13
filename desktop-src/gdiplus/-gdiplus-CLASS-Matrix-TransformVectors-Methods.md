---
description: Este tópico lista os métodos TransformVectors da classe Matrix. Para obter uma lista completa de métodos para a classe Matrix, consulte métodos de matriz.
ms.assetid: 6a2ed6a7-825a-422b-b035-b88746f3ab5d
title: Métodos Matrix. TransformVectors (Gdiplusmatrix. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3bdb67d839163ffe2d26623a01fc186f8e885ca2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968778"
---
# <a name="matrixtransformvectors-methods"></a><span data-ttu-id="45ecc-104">Métodos Matrix. TransformVectors</span><span class="sxs-lookup"><span data-stu-id="45ecc-104">Matrix.TransformVectors methods</span></span>

<span data-ttu-id="45ecc-105">Este tópico lista os métodos TransformVectors da classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="45ecc-105">This topic lists the TransformVectors methods of the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="45ecc-106">Para obter uma lista completa de métodos para a classe **Matrix** , consulte [métodos de matriz](-gdiplus-class-matrix-methods.md).</span><span class="sxs-lookup"><span data-stu-id="45ecc-106">For a complete list of methods for the **Matrix** class, see [Matrix Methods](-gdiplus-class-matrix-methods.md).</span></span>

### <a name="overload-list"></a><span data-ttu-id="45ecc-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="45ecc-107">Overload list</span></span>



| <span data-ttu-id="45ecc-108">Método</span><span class="sxs-lookup"><span data-stu-id="45ecc-108">Method</span></span>                                                                                                 | <span data-ttu-id="45ecc-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="45ecc-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ecc-110">[**TransformVectors (ponto \* , int)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span><span class="sxs-lookup"><span data-stu-id="45ecc-110">[**TransformVectors(Point\*,INT)**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint))</span></span>   | <span data-ttu-id="45ecc-111">O método [**Matrix:: TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) multiplica cada vetor em uma matriz por essa matriz.</span><span class="sxs-lookup"><span data-stu-id="45ecc-111">The [**Matrix::TransformVectors**](/windows/win32/api/gdiplusmatrix/nf-gdiplusmatrix-matrix-transformvectors(inoutpoint_inint)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="45ecc-112">Os elementos de translação da matriz (terceira linha) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="45ecc-112">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="45ecc-113">Cada vetor é tratado como uma matriz de linhas.</span><span class="sxs-lookup"><span data-stu-id="45ecc-113">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="45ecc-114">A multiplicação é executada com a matriz de linhas à esquerda e essa matriz à direita.</span><span class="sxs-lookup"><span data-stu-id="45ecc-114">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/>  |
| <span data-ttu-id="45ecc-115">[**TransformVectors (PointF \* , int)**](/previous-versions//ms535319(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="45ecc-115">[**TransformVectors(PointF\*,INT)**](/previous-versions//ms535319(v=vs.85))</span></span> | <span data-ttu-id="45ecc-116">O método [**Matrix:: TransformVectors**](/previous-versions//ms535319(v=vs.85)) multiplica cada vetor em uma matriz por essa matriz.</span><span class="sxs-lookup"><span data-stu-id="45ecc-116">The [**Matrix::TransformVectors**](/previous-versions//ms535319(v=vs.85)) method multiplies each vector in an array by this matrix.</span></span> <span data-ttu-id="45ecc-117">Os elementos de translação da matriz (terceira linha) são ignorados.</span><span class="sxs-lookup"><span data-stu-id="45ecc-117">The translation elements of this matrix (third row) are ignored.</span></span> <span data-ttu-id="45ecc-118">Cada vetor é tratado como uma matriz de linhas.</span><span class="sxs-lookup"><span data-stu-id="45ecc-118">Each vector is treated as a row matrix.</span></span> <span data-ttu-id="45ecc-119">A multiplicação é executada com a matriz de linhas à esquerda e essa matriz à direita.</span><span class="sxs-lookup"><span data-stu-id="45ecc-119">The multiplication is performed with the row matrix on the left and this matrix on the right.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="45ecc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45ecc-120">Requirements</span></span>



| <span data-ttu-id="45ecc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="45ecc-121">Requirement</span></span> | <span data-ttu-id="45ecc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="45ecc-122">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="45ecc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45ecc-123">Header</span></span><br/> | <dl> <span data-ttu-id="45ecc-124"><dt>Gdiplusmatrix. h</dt></span><span class="sxs-lookup"><span data-stu-id="45ecc-124"><dt>Gdiplusmatrix.h</dt></span></span> </dl> |



 

 
