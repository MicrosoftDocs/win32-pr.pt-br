---
title: Estados do botão da barra de ferramentas (CommCtrl. h)
description: Esta seção lista os Estados que um botão de barra de ferramentas pode ter.
ms.assetid: 422e0d81-bd80-45dc-b843-82fc5d5c2a9a
topic_type:
- apiref
api_name:
- TBSTATE_CHECKED
- TBSTATE_ELLIPSES
- TBSTATE_ENABLED
- TBSTATE_HIDDEN
- TBSTATE_INDETERMINATE
- TBSTATE_MARKED
- TBSTATE_PRESSED
- TBSTATE_WRAP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45262197c4432d9e3bb5c0884b3f76c986e4acfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749947"
---
# <a name="toolbar-button-states"></a>Estados de botão da barra de ferramentas

Esta seção lista os Estados que um botão de barra de ferramentas pode ter.



| Constante                                                                                                                                                                              | Descrição                                                                                                                                           |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBSTATE_CHECKED"></span><span id="tbstate_checked"></span><dl> <dt>**TBSTATE \_ verificados**</dt> </dl>                   | O botão tem o estilo de [**\_ verificação TBSTYLE**](toolbar-control-and-button-styles.md) e está sendo clicado.<br/>                   |
| <span id="TBSTATE_ELLIPSES"></span><span id="tbstate_ellipses"></span><dl> <dt>**\_reticências TBSTATE**</dt> </dl>                | [Versão 4,70](common-control-versions.md). O texto do botão é cortado e uma elipse é exibida.<br/>                                    |
| <span id="TBSTATE_ENABLED"></span><span id="tbstate_enabled"></span><dl> <dt>**TBSTATE \_ habilitado**</dt> </dl>                   | O botão aceita a entrada do usuário. Um botão que não tem esse estado é acinzentado.<br/>                                                           |
| <span id="TBSTATE_HIDDEN"></span><span id="tbstate_hidden"></span><dl> <dt>**TBSTATE \_ oculto**</dt> </dl>                      | O botão não está visível e não pode receber entrada do usuário.<br/>                                                                                   |
| <span id="TBSTATE_INDETERMINATE"></span><span id="tbstate_indeterminate"></span><dl> <dt>**TBSTATE \_ indeterminado**</dt> </dl> | O botão está acinzentado.<br/>                                                                                                                      |
| <span id="TBSTATE_MARKED"></span><span id="tbstate_marked"></span><dl> <dt>**TBSTATE \_ marcado**</dt> </dl>                      | [Versão 4,71](common-control-versions.md). O botão é marcado. A interpretação de um item marcado depende do aplicativo. <br/> |
| <span id="TBSTATE_PRESSED"></span><span id="tbstate_pressed"></span><dl> <dt>**TBSTATE \_ pressionado**</dt> </dl>                   | O botão está sendo clicado.<br/>                                                                                                               |
| <span id="TBSTATE_WRAP"></span><span id="tbstate_wrap"></span><dl> <dt>**\_encapsulamento de TBSTATE**</dt> </dl>                            | O botão é seguido por uma quebra de linha. O botão também deve ter o \_ estado habilitado TBSTATE.<br/>                                              |



## <a name="remarks"></a>Comentários

Uma barra de ferramentas pode ter uma combinação de Estados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





