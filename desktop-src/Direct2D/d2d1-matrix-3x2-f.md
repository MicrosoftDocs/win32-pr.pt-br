---
title: D2D1_MATRIX_3X2_F (D2d1. h)
description: Representa uma matriz 3 por 2.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759153"
---
# <a name="d2d1_matrix_3x2_f"></a><span data-ttu-id="29b92-104">D2D1 \_ matriz \_ 3x2 \_ F</span><span class="sxs-lookup"><span data-stu-id="29b92-104">D2D1\_MATRIX\_3X2\_F</span></span>

<span data-ttu-id="29b92-105">Representa uma matriz 3 por 2.</span><span class="sxs-lookup"><span data-stu-id="29b92-105">Represents a 3-by-2 matrix.</span></span>


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a><span data-ttu-id="29b92-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="29b92-106">Remarks</span></span>

<span data-ttu-id="29b92-107">**D2d1 \_ MATRIZ \_ 3x2** é um novo nome para a estrutura [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="29b92-107">**D2D1\_MATRIX\_3X2** is a new name for the [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="29b92-108">Para obter uma lista de campos fornecidos pela matriz, consulte [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span><span class="sxs-lookup"><span data-stu-id="29b92-108">For a list of fields provided by the matrix, see [**D2D\_MATRIX\_3X2\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).</span></span>

<span data-ttu-id="29b92-109">Para simplificar as operações comuns de matriz, o Direct2D fornece a classe [**d2d1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) , que é derivada da estrutura [**\_ \_ 3x2 da matriz d2d1**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) .</span><span class="sxs-lookup"><span data-stu-id="29b92-109">To simplify common matrix operations, Direct2D provides the [**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) class, which is derived from the [**D2D1\_MATRIX\_3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) structure.</span></span> <span data-ttu-id="29b92-110">A classe **Matrix3x2F** fornece um conjunto de métodos auxiliares para executar tarefas comuns, como a criação de uma translação ou matriz de distorção.</span><span class="sxs-lookup"><span data-stu-id="29b92-110">The **Matrix3x2F** class provides a set of helper methods for performing common tasks, such as creating a translation or skew matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="29b92-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29b92-111">Examples</span></span>

<span data-ttu-id="29b92-112">O exemplo a seguir usa o método [**d2d1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) para criar uma matriz de rotação que gira um quadrado no sentido horário 45 graus sobre o centro do quadrado e passa a matriz para o método [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) do destino render (*m \_ pRenderTarget*).</span><span class="sxs-lookup"><span data-stu-id="29b92-112">The following example uses the [**D2D1::Matrix3x2F::Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) method to create a rotation matrix that rotates a square clockwise 45 degrees about the center of the square and passes the matrix to the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) method of the render target (*m\_pRenderTarget*).</span></span>

<span data-ttu-id="29b92-113">A ilustração a seguir mostra o efeito de aplicar a transformação de rotação anterior ao quadrado.</span><span class="sxs-lookup"><span data-stu-id="29b92-113">The following illustration shows the effect of applying the preceding rotation transformation to the square.</span></span> <span data-ttu-id="29b92-114">O quadrado original é um contorno pontilhado e o quadrado girado é uma estrutura de tópicos sólida.</span><span class="sxs-lookup"><span data-stu-id="29b92-114">The original square is a dotted outline, and the rotated square is a solid outline.</span></span>

![ilustração de um quadrado girado no sentido horário 45 graus sobre o centro do quadrado original](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



<span data-ttu-id="29b92-116">O código foi omitido neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="29b92-116">Code has been omitted from this example.</span></span> <span data-ttu-id="29b92-117">Para obter mais informações sobre transformações, consulte a [Visão geral das transformações](direct2d-transforms-overview.md).</span><span class="sxs-lookup"><span data-stu-id="29b92-117">For more information about transforms, see the [Transforms Overview](direct2d-transforms-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29b92-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29b92-118">Requirements</span></span>



| <span data-ttu-id="29b92-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="29b92-119">Requirement</span></span> | <span data-ttu-id="29b92-120">Valor</span><span class="sxs-lookup"><span data-stu-id="29b92-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b92-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29b92-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29b92-122">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="29b92-122">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="29b92-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29b92-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29b92-124">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="29b92-124">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="29b92-125">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="29b92-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="29b92-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="29b92-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="29b92-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29b92-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="29b92-128"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="29b92-128"><dt>D2d1.h</dt></span></span> </dl>                                                        |



## <a name="see-also"></a><span data-ttu-id="29b92-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="29b92-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b92-130">**D2D1::Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="29b92-130">**D2D1::Matrix3x2F**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[<span data-ttu-id="29b92-131">Visão geral das transformações</span><span class="sxs-lookup"><span data-stu-id="29b92-131">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="29b92-132">Como girar um objeto</span><span class="sxs-lookup"><span data-stu-id="29b92-132">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="29b92-133">Como dimensionar um objeto</span><span class="sxs-lookup"><span data-stu-id="29b92-133">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="29b92-134">Como distorcer um objeto</span><span class="sxs-lookup"><span data-stu-id="29b92-134">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="29b92-135">Como converter um objeto</span><span class="sxs-lookup"><span data-stu-id="29b92-135">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="29b92-136">**D2D \_ matriz \_ 3x2 \_ F**</span><span class="sxs-lookup"><span data-stu-id="29b92-136">**D2D\_MATRIX\_3X2\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

