---
title: Métodos SetTransform ID2D1RenderTarget
description: Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente. Todas as operações de desenho subsequentes ocorrem no espaço transformado.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Métodos SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756003"
---
# <a name="id2d1rendertargetsettransform-methods"></a>Métodos ID2D1RenderTarget:: SetTransform

Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente. Todas as operações de desenho subsequentes ocorrem no espaço transformado.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                              | Descrição                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente. Todas as operações de desenho subsequentes ocorrem no espaço transformado. <br/> |
| [**SetTransform ( \_ matriz d2d1 \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente. Todas as operações de desenho subsequentes ocorrem no espaço transformado.<br/>  |



## <a name="examples"></a>Exemplos

O exemplo a seguir usa o método **SetTransform** para aplicar uma rotação ao destino de renderização. Para obter o exemplo completo, consulte [como girar um objeto](how-to-rotate.md).


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



Para obter exemplos adicionais mostrando como transformar um destino de renderização, consulte [como dimensionar um objeto](how-to-scale.md), [como distorcer um objeto](how-to-skew.md)e [como converter um objeto](how-to-translate.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Visão geral das transformações](direct2d-transforms-overview.md)
</dt> <dt>

[Como girar um objeto](how-to-rotate.md)
</dt> <dt>

[Como dimensionar um objeto](how-to-scale.md)
</dt> <dt>

[Como distorcer um objeto](how-to-skew.md)
</dt> <dt>

[Como converter um objeto](how-to-translate.md)
</dt> <dt>

[Como aplicar várias transformações a um objeto](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

