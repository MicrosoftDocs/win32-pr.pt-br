---
title: SB_GETTEXT mensagem (Commctrl.h)
description: Recupera o texto da parte especificada de uma janela de status.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT controles de Windows mensagem
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05967d41d86ad039e39259c8179a9e768e8fbbf76e5112b531048ac0ed7b56bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168722"
---
# <a name="sb_gettext-message"></a>Mensagem \_ GETTEXT SB

Recupera o texto da parte especificada de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da parte da qual recuperar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o buffer que recebe o texto como uma cadeia de caracteres terminada em nulo. Use a [**mensagem SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para determinar o tamanho necessário do buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 32 bits que consiste em dois valores de 16 bits. A palavra baixa especifica o comprimento, em caracteres, do texto. A palavra alta especifica o tipo de operação usada para desenhar o texto. O tipo pode ser um dos valores a seguir.



| Código de retorno                                                                                    | Descrição                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | O texto é desenhado com uma borda a ser exibida abaixo do plano da janela.<br/>  |
| <dl> <dt>**SBT \_ NOBORDERS**</dt> </dl>  | O texto é desenhado sem bordas.<br/>                                             |
| <dl> <dt>**POPOUT do SBT \_**</dt> </dl>     | O texto é desenhado com uma borda para aparecer acima do plano da janela.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | O texto é exibido na direção oposta do texto na janela pai.<br/>  |



 

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do programa. Essa mensagem não fornece uma maneira de saber o tamanho do buffer. Se você usar essa mensagem, primeiro chame [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o número de caracteres necessários e, em seguida, chame a mensagem para recuperar a cadeia de caracteres. Se você aguardar antes de chamar **SB \_ GETTEXT,** o texto poderá ser alterado, invalidando assim o valor de retorno **de SB \_ GETTEXTLENGTH.** Você deve revisar as [Considerações sobre segurança: Controles Windows Microsoft antes](sec-comctls.md) de continuar.

Essa mensagem retorna um máximo de 65.535 caracteres. Se a cadeia de caracteres de texto for maior que isso, ela será truncada.

Se o texto tiver o tipo de desenho SBT OWNERDRAW, essa mensagem retornará o valor de 32 bits associado ao texto em vez do tamanho e do tipo \_ de operação.

Janelas normais exibem o texto da esquerda para a direita (LTR). Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que leem a RTL (direita para esquerda). Se SBT RTLREADING estiver definido, a cadeia de \_ caracteres *lParam* será lida na direção oposta do texto na janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) e **SB \_ GETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SB \_ SETTEXT**](sb-settext.md)
</dt> </dl>

 

 





