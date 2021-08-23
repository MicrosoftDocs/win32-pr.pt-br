---
description: Esses sinalizadores fornecem informações adicionais sobre parâmetros de efeito.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect.h)
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
ms.openlocfilehash: 5314ae0a13f6b9f4e246cc61c33ce626f217a4d654de2f582d18027c952bd2a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607806"
---
# <a name="d3dx_parameter"></a>PARÂMETRO \_ D3DX

Esses sinalizadores fornecem informações adicionais sobre parâmetros de efeito.

Constantes de parâmetro de efeito são usadas [**por D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).



| Constante                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**ANOTAÇÃO DE \_ PARÂMETRO D3DX \_**</dt> </dl> | Esse parâmetro é marcado como uma anotação. Consulte [Adicionar informações a parâmetros de efeito com anotações](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**LITERAL DE PARÂMETRO D3DX \_ \_**</dt> </dl>          | Esse parâmetro é marcado como um valor literal. Os parâmetros literais não podem ser alterados após a compilação, permitindo que o compilador otimize seu uso. Parâmetros compartilhados não podem ser marcados como um literal. Consulte [Usos e literais (Direct3D 9)](usages-and-literals.md). <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**PARÂMETRO D3DX \_ \_ COMPARTILHADO**</dt> </dl>             | O valor de um parâmetro será compartilhado por todos os efeitos no mesmo namespace. Alterar o valor em um efeito o alterará em todos os efeitos compartilhados. Consulte [Compartilhamento de parâmetros](cloning-and-sharing.md). **D3DX \_ PARAMETER \_ SHARED** não pode ser combinado com A ANOTAÇÃO DE PARÂMETRO **\_ D3DX \_ LITERAL** ou **D3DX \_ \_ PARAMETER**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de efeito](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




