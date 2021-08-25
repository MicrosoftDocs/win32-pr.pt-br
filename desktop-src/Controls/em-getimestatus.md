---
title: EM_GETIMESTATUS mensagem (Winuser.h)
description: Obtém um conjunto de sinalizadores de status que indicam como o controle de edição interage com o IME (Editor de Método de Entrada).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01a8251a62aa9cf48bcc6476af27e4c3a5dbbb82dd0ce76ca21ae094225a3e46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048986"
---
# <a name="em_getimestatus-message"></a>Mensagem EM \_ GETIMESTATUS

Obtém um conjunto de sinalizadores de status que indicam como o controle de edição interage com o IME (Editor de Método de Entrada).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de status a ser recuperado. Esse parâmetro pode ser o valor a seguir.



| Valor                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Define o comportamento para lidar com a cadeia de caracteres de composição.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Dados específicos para o tipo de status a ser recuperado. Com o **valor EMSIS \_ COMPOSITIONSTRING** *para status*, esse valor de retorno é um ou mais dos valores a seguir.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Se esse sinalizador for definido, o controle de edição conectará a mensagem [**WM \_ IME \_ COMPOSITION**](/windows/desktop/Intl/wm-ime-composition) com *fFlags* definido como GCS RESULTSTR e retornará a cadeia de caracteres \_ de resultado imediatamente. Se esse sinalizador não estiver definido, o controle de edição passará a mensagem **WM \_ IME \_ COMPOSITION** para o procedimento de janela padrão e processa a cadeia de caracteres de resultado da mensagem [**WM \_ CHAR;**](/windows/desktop/inputdev/wm-char) esse é o comportamento padrão do controle de edição.<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Se esse sinalizador for definido, o controle de edição cancelará a cadeia de caracteres de composição quando receber a [**mensagem WM \_ SETFOCUS.**](/windows/desktop/inputdev/wm-setfocus) Se esse sinalizador não estiver definido, o controle de edição não cancelará a cadeia de caracteres de composição; esse é o comportamento padrão do controle de edição.<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Se esse sinalizador for definido, o controle de edição concluirá a cadeia de caracteres de composição ao receber a mensagem [**WM \_ KILLFOCUS.**](/windows/desktop/inputdev/wm-killfocus) Se esse sinalizador não estiver definido, o controle de edição não concluirá a cadeia de caracteres de composição; esse é o comportamento padrão do controle de edição.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

**Edição rica:** Não há suporte para a mensagem **EM \_ GETIMESTATUS.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETIMESTATUS**](em-setimestatus.md)
</dt> </dl>

 

