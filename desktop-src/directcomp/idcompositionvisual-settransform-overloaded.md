---
title: Métodos SetTransform de IDCompositionVisual (DCOMP. h)
description: Define a propriedade Transform deste visual. A propriedade Transform especifica uma transformação 2D usada para modificar o sistema de coordenadas deste visual. A propriedade pode especificar uma matriz de transformação 3-by-2 ou um objeto de transformação.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295881"
---
# <a name="idcompositionvisualsettransform-methods"></a>Métodos IDCompositionVisual:: SetTransform

Define a propriedade Transform deste visual. A propriedade Transform especifica uma transformação 2D usada para modificar o sistema de coordenadas deste visual. A propriedade pode especificar uma matriz de transformação 3-by-2 ou um objeto de transformação.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                                    | Descrição                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform (D2D \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | Define a propriedade Transform para a matriz de transformação especificada.<br/>      |
| [**SetTransform (IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | Define a propriedade Transform para o objeto de transformação especificado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>DCOMP. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>DCOMP. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

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
