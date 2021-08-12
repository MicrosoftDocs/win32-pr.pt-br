---
title: Métodos SetTransform de IDCompositionVisual3 (DCOMP. h)
description: Define a propriedade Transform deste visual. A propriedade Transform especifica uma transformação 3D usada para modificar o sistema de coordenadas deste visual. A propriedade pode especificar uma matriz de transformação 4 por 4 ou um objeto de transformação.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
keywords:
- Métodos SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 08b243704c3eabae528d475c92b924f6aecfba92f923b7190c085e3e89bd1f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281233"
---
# <a name="idcompositionvisual3settransform-methods"></a>Métodos IDCompositionVisual3:: SetTransform

Define a propriedade Transform deste visual. A propriedade Transform especifica uma transformação 3D usada para modificar o sistema de coordenadas deste visual. A propriedade pode especificar uma matriz de transformação 4 por 4 ou um objeto de transformação.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                  | Descrição                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform (D2D \_ Matrix \_ 4X4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | Define a propriedade Transform para a matriz de transformação especificada.<br/>      |
| [**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | Define a propriedade Transform para o objeto de transformação especificado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[apenas aplicativos de área de trabalho Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>DCOMP. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>DCOMP. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDCompositionVisual3**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**IDCompositionSkewTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**IDCompositionTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**IDCompositionVisual::SetOffsetX**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**IDCompositionVisual:: setdeslocy**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
