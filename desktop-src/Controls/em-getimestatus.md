---
title: Mensagem de EM_GETIMESTATUS (WinUser. h)
description: Obtém um conjunto de sinalizadores de status que indicam como o controle de edição interage com o IME (editor de método de entrada).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- Controles de EM_GETIMESTATUS de mensagens do Windows
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
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086036"
---
# <a name="em_getimestatus-message"></a>\_Mensagem em GETIMESTATUS

Obtém um conjunto de sinalizadores de status que indicam como o controle de edição interage com o IME (editor de método de entrada).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de status a ser recuperado. Esse parâmetro pode ser o valor a seguir.



| Valor                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**\_COMposicionastring EMSIS**</dt> </dl> | Define o comportamento para manipular a cadeia de caracteres de composição.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Dados específicos do tipo de status a recuperar. Com o valor **EMSIS \_ CompositionString** para *status*, esse valor de retorno é um ou mais dos valores a seguir.



| Código de retorno                                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Se esse sinalizador for definido, o controle de edição acoplará a mensagem de [**\_ \_ composição IME do WM**](/windows/desktop/Intl/wm-ime-composition) com *fFlags* definido como GCS \_ RESULTSTR e retornará a cadeia de caracteres de resultado imediatamente. Se esse sinalizador não for definido, o controle de edição passará a mensagem de **\_ \_ composição IME do WM** para o procedimento de janela padrão e processará a cadeia de caracteres de resultado da mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) ; esse é o comportamento padrão do controle de edição.<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Se esse sinalizador for definido, o controle de edição cancelará a cadeia de caracteres de composição quando receber a mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) . Se esse sinalizador não for definido, o controle de edição não cancelará a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Se esse sinalizador for definido, o controle de edição concluirá a cadeia de caracteres de composição após receber a mensagem [**\_ KILLFOCUS do WM**](/windows/desktop/inputdev/wm-killfocus) . Se esse sinalizador não for definido, o controle de edição não concluirá a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

**Edição avançada:** Não há suporte para a mensagem em **\_ GETIMESTATUS** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETIMESTATUS**](em-setimestatus.md)
</dt> </dl>

 

