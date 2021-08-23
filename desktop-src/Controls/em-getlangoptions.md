---
title: Mensagem de EM_GETLANGOPTIONS (RichEdit. h)
description: Obtém as configurações de opção do controle de edição rico para o editor de método de entrada (IME) e suporte a idiomas asiáticos.
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- controles de Windows de mensagem de EM_GETLANGOPTIONS
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3fa3602259ff0b754c79c69d91048c68c60b2703d4cd06a7da4630fcdf646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800196"
---
# <a name="em_getlangoptions-message"></a>\_Mensagem em GETlangoptions

Obtém as configurações de opção do controle de edição rico para o editor de método de entrada (IME) e suporte a idiomas asiáticos.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna as configurações do IME e do idioma asiático, que podem ser zero ou mais dos valores a seguir.



| Código de retorno                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**autofonte do IMF \_**</dt> </dl>                    | Se esse sinalizador for definido, o controle alterará automaticamente as fontes quando o usuário mudar explicitamente para um layout de teclado diferente. É útil desativar a **\_ autofonte do IMF** para fontes Unicode universal. Essa opção é ativada por padrão (1).<br/>                                                                                                                                                                     |
| <dl> <dt>**AUTOFONTSIZEADJUST do IMF \_**</dt> </dl>          | Se esse sinalizador for definido, o controle dimensionará os tamanhos de fonte associados à fonte do tamanho do ponto de inserção de acordo com o script. Por exemplo, as fontes asiáticas são ligeiramente maiores do que as ocidentais. Essa opção é ativada por padrão (1).<br/>                                                                                                                                                                                              |
| <dl> <dt>**autoteclado do IMF \_**</dt> </dl>                | Se esse sinalizador for definido, o controle alterará automaticamente o layout do teclado quando o usuário mudar explicitamente para uma fonte diferente ou quando o usuário alterar explicitamente o ponto de inserção para um novo local no texto. Será ativado automaticamente para controles bidirecionais. Para todos os outros controles, ele é desativado por padrão. Essa opção é desativada por padrão (0).<br/>                                 |
| <dl> <dt>**DISABLEAUTOBIDIAUTOKEYBOARD do IMF \_**</dt> </dl> | **Windows 8**: se esse sinalizador for definido, o controle usará a lógica neutra do idioma para a alternância automática de teclado. Essa opção é desativada por padrão (0).<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**DUALFONT do IMF \_**</dt> </dl>                    | Se esse sinalizador for definido, o controle usará o modo de fonte dupla. Usado para suporte a idiomas asiáticos. O controle usa uma fonte em inglês para texto ASCII e uma fonte asiática para texto asiático. Essa opção é ativada por padrão (1).<br/>                                                                                                                                                                                                   |
| <dl> <dt>**IMEALWAYSSENDNOTIFY do IMF \_**</dt> </dl>         | Esse sinalizador controla como o controle de edição rico notifica o cliente durante a composição do IME: <br/> 0: não há nenhuma notificação [en \_ Change](en-change.md) ou [en \_ SELCHANGE](en-selchange.md) durante o estado indeterminado. Enviar notificação quando a cadeia de caracteres final chegar. Esse é o padrão.<br/> 1: send [en \_ ](en-change.md) e [ \_ SELCHANGE](en-selchange.md) eventos de alteração e en durante o estado indeterminado.<br/> |
| <dl> <dt>**IMECANCELCOMPLETE do IMF \_**</dt> </dl>           | Esse sinalizador determina como o controle usará a cadeia de caracteres de composição de um IME se o usuário cancelá-lo. Se esse sinalizador estiver definido, o controle descartará a cadeia de caracteres de composição. Se este sinalizador não for definido, o controle usará a cadeia de caracteres de composição como a cadeia de caracteres de resultado. Essa opção é desativada por padrão (0).<br/>                                                                                                              |
| <dl> <dt>**NOIMPLICITLANG do IMF \_**</dt> </dl>              | **Windows 8**: se esse sinalizador estiver definido, desabilite a entrada de teclado de carimbo com o idioma do teclado e verifique se os IDss de idioma não leste asiático são compatíveis com o caractere repertório. Essa opção é desativada por padrão (0). <br/>                                                                                                                                                                             |
| <dl> <dt>**NOKBDLIDFIXUP do IMF \_**</dt> </dl>               | **Windows 8**: se esse sinalizador for definido, o controle de edição rico desabilitará o idioma do teclado de carimbo em um controle vazio. Essa opção é desativada por padrão (0).<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**\_verificação ortográfica do IMF**</dt> </dl>               | **Windows 8**: se esse sinalizador for definido, o controle de edição rico ativará a verificação ortográfica. Essa opção é desativada por padrão (0). <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**TKBAUTOCORRECTION do IMF \_**</dt> </dl>           | **Windows 8**: se esse sinalizador estiver definido, habilite a autocorreção do teclado de toque. Essa opção é desativada por padrão (0). <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**TKBPREDICTION do IMF \_**</dt> </dl>               | **Windows 10**: ignorado.<br/> **Windows 8**: se esse sinalizador for definido, o controle rich edit permitirá a previsão do teclado de toque. Essa opção é desativada por padrão (0). <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**UIFONTS do IMF \_**</dt> </dl>                     | Usar fontes padrão da interface do usuário. Essa opção é desativada por padrão (0).<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

O sinalizador de **\_ Autofonte do IMF** é definido por padrão. Os sinalizadores de **\_ teclado** **\_ IMECANCELCOMPLETE** do IMF e do IMF são apagados por padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETlangoptions**](em-setlangoptions.md)
</dt> <dt>

[**em \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





