---
title: Mensagem de SB_GETTEXT (commctrl. h)
description: Recupera o texto da parte especificada de uma janela de status.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- Controles de SB_GETTEXT de mensagens do Windows
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
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009605"
---
# <a name="sb_gettext-message"></a>\_Mensagem GETTEXT SB

Recupera o texto da parte especificada de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da parte da qual recuperar o texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o buffer que recebe o texto como uma cadeia de caracteres terminada em nulo. Use a [**mensagem \_ GETTEXTLENGTH do SB**](sb-gettextlength.md) para determinar o tamanho necessário do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 32 bits que consiste em valores de 2 16 bits. A palavra inferior Especifica o comprimento, em caracteres, do texto. A palavra alta especifica o tipo de operação usado para desenhar o texto. O tipo pode ser um dos valores a seguir.



| Código de retorno                                                                                    | Descrição                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | O texto é desenhado com uma borda para aparecer menor do que o plano da janela.<br/>  |
| <dl> <dt>**SBT \_ NObordas**</dt> </dl>  | O texto é desenhado sem bordas.<br/>                                             |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | O texto é desenhado com uma borda para aparecer maior do que o plano da janela.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | O texto é exibido na direção oposta do texto na janela pai.<br/>  |



 

## <a name="remarks"></a>Comentários

**Aviso de segurança:** Usar essa mensagem incorretamente pode comprometer a segurança do seu programa. Essa mensagem não fornece uma maneira de saber o tamanho do buffer. Se você usar essa mensagem, primeiro chame [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o número de caracteres necessários e, em seguida, chame a mensagem para recuperar a cadeia de caracteres. Se você aguardar antes de chamar **SB \_ gettext** , o texto poderá ser alterado, invalidando o valor de retorno de **SB \_ GETTEXTLENGTH**. Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.

Essa mensagem retorna um máximo de 65.535 caracteres. Se a cadeia de texto for maior que isso, ela será truncada.

Se o texto tiver o \_ tipo de desenho SBT OWNERDRAW, essa mensagem retornará o valor de 32 bits associado ao texto em vez do comprimento e do tipo de operação.

Texto de exibição normal do Windows da esquerda para a direita (EPD). O Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que são lidos da direita para a esquerda (RTL). Se SBT \_ RTLREADING for definido, a cadeia de caracteres *lParam* lerá na direção oposta do texto na janela pai.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) e **SB \_ gettexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SB \_ SETtext**](sb-settext.md)
</dt> </dl>

 

 





