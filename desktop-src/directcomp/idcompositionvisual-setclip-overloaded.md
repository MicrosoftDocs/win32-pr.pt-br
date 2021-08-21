---
title: Métodos SetClip IDCompositionVisual (DCOMP. h)
description: Define a propriedade Clip deste visual como a região retangular ou o objeto de clipe especificado.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Métodos SetClip DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 1cc1d0f24c30e6ec11ecaa40b0317109eddaf432ee311a5b9545f34f7afa8582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043054"
---
# <a name="idcompositionvisualsetclip-methods"></a>Métodos IDCompositionVisual:: SetClip

Define a propriedade Clip deste visual como a região retangular ou o objeto de clipe especificado. A propriedade Clip restringe a renderização da subárvore visual que é enraizada neste visual para uma região retangular.

### <a name="overload-list"></a>Lista de sobrecargas



| Método                                                                                | Descrição                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SetClip (const D2D \_ Rect \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | Define a propriedade Clip como a região retangular especificada.<br/> |
| [**SetClip (IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | Define a propriedade de clipe para o objeto de clipe especificado.<br/>        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[apenas aplicativos de área de trabalho Windows 8\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2012\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>DCOMP. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>DCOMP. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Recortando](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
