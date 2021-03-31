---
title: Mensagem de EM_SETIMESTATUS (WinUser. h)
description: Define os sinalizadores de status que determinam como um controle de edição interage com o IME (editor de método de entrada).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- Controles de EM_SETIMESTATUS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644777"
---
# <a name="em_setimestatus-message"></a>\_Mensagem em SETIMESTATUS

Define os sinalizadores de status que determinam como um controle de edição interage com o IME (editor de método de entrada).

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de status a ser definido. Esse parâmetro pode ser o valor a seguir.



| Valor                                                                                                                                                                                       | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**\_COMposicionastring EMSIS**</dt> </dl> | Define o comportamento para a cadeia de caracteres de composição de manipulação.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dados específicos para o tipo de status. Se *wParam* for **EMSIS \_ CompositionString**, esse parâmetro poderá ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Se esse sinalizador for definido, o controle de edição acoplará a mensagem de [**\_ \_ composição do IME do WM**](/windows/desktop/Intl/wm-ime-composition) com *lParam* definido como GCS \_ RESULTSTR e retornará a cadeia de caracteres de resultado imediatamente. Se esse sinalizador não for definido, o controle de edição passará a mensagem de **\_ \_ composição IME do WM** para o procedimento de janela padrão e manipulará a cadeia de caracteres de resultado da mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) ; esse é o comportamento padrão do controle de edição.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | Se esse sinalizador for definido, o controle de edição cancelará a cadeia de caracteres de composição quando receber a mensagem do [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) . Se esse sinalizador não for definido, o controle de edição não cancelará a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Se esse sinalizador for definido, o controle de edição concluirá a cadeia de caracteres de composição após receber a mensagem [**\_ KILLFOCUS do WM**](/windows/desktop/inputdev/wm-killfocus) . Se esse sinalizador não for definido, o controle de edição não concluirá a cadeia de caracteres de composição; Esse é o comportamento padrão do controle de edição.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor anterior do parâmetro *lParam* .

## <a name="remarks"></a>Comentários

**Edição avançada:** Não há suporte para a mensagem em **\_ SETIMESTATUS** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETIMESTATUS**](em-getimestatus.md)
</dt> </dl>

 

