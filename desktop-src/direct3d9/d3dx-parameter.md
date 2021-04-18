---
description: Esses sinalizadores fornecem informações adicionais sobre os parâmetros de efeito.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780676"
---
# <a name="d3dx_parameter"></a>\_Parâmetro D3DX

Esses sinalizadores fornecem informações adicionais sobre os parâmetros de efeito.

Constantes de parâmetro de efeito são usadas por [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).



| Constante                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**\_Anotação de parâmetro D3DX \_**</dt> </dl> | Esse parâmetro é marcado como uma anotação. Consulte [adicionar informações para parâmetros de efeito com anotações](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**\_Literal de parâmetro D3DX \_**</dt> </dl>          | Esse parâmetro é marcado como um valor literal. Os parâmetros literais não podem ser alterados após a compilação, permitindo que o compilador Otimize seu uso. Os parâmetros compartilhados não podem ser marcados como um literal. Consulte [usos e literais (Direct3D 9)](usages-and-literals.md). <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**\_Parâmetro D3DX \_ compartilhado**</dt> </dl>             | O valor de um parâmetro será compartilhado por todos os efeitos no mesmo namespace. Alterar o valor em um efeito irá alterá-lo em todos os efeitos compartilhados. Consulte [compartilhando parâmetros](cloning-and-sharing.md). **D3DX \_ O parâmetro \_ compartilhado** não pode ser combinado com o **\_ parâmetro D3DX \_ literal** ou a **\_ \_ anotação de parâmetro D3DX**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de efeito](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




