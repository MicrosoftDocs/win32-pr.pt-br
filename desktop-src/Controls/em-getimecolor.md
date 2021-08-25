---
title: EM_GETIMECOLOR mensagem (Richedit.h)
description: Recupera a cor de composição do IME (Editor de Método de Entrada).
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ac9d49f4fe178bdda45359da8aabd40badcd68aceadc4a57890279fc9fda01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049096"
---
# <a name="em_getimecolor-message"></a>Mensagem EM \_ GETIMECOLOR

Recupera a cor de composição do IME (Editor de Método de Entrada).

> [!Note]  
> Essa mensagem só tem suporte em versões de idioma asiático do Microsoft Rich Edit 1.0. Não há suporte para ele em nenhuma versão posterior do Rich Edit.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma matriz de quatro elementos de [**estruturas COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) que recebe a cor da composição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for bem-sucedida, o valor de retorno será um valor não zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





