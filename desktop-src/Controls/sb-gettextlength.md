---
title: Mensagem de SB_GETTEXTLENGTH (commctrl. h)
description: Recupera o comprimento, em caracteres, do texto da parte especificada de uma janela de status.
ms.assetid: 2cd43106-dd43-499e-b595-760e9ededab5
keywords:
- Controles de SB_GETTEXTLENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETTEXTLENGTH
- SB_GETTEXTLENGTHA
- SB_GETTEXTLENGTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b08dd3b870c3c59e5aafbeb9d53baef3816a726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918869"
---
# <a name="sb_gettextlength-message"></a>\_Mensagem de GETTEXTLENGTH SB

Recupera o comprimento, em caracteres, do texto da parte especificada de uma janela de status.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da parte da qual recuperar o texto.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 32 bits que consiste em valores de 2 16 bits. A palavra inferior Especifica o comprimento, em caracteres, do texto. A palavra alta especifica o tipo de operação usado para desenhar o texto. O tipo pode ser um dos seguintes valores:



| Código de retorno                                                                                    | Descrição                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | O texto é desenhado com uma borda para aparecer menor do que o plano da janela.<br/>          |
| <dl> <dt>**SBT \_ NObordas**</dt> </dl>  | O texto é desenhado sem bordas.<br/>                                                     |
| <dl> <dt>**SBT \_ OWNERDRAW**</dt> </dl>  | O texto é desenhado pela janela pai.<br/>                                                |
| <dl> <dt>**SBT \_ POPOUT**</dt> </dl>     | O texto é desenhado com uma borda para aparecer maior do que o plano da janela.<br/>         |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | O texto será exibido na direção oposta ao texto na janela pai.<br/> |



 

## <a name="remarks"></a>Comentários

Texto de exibição normal do Windows da esquerda para a direita (EPD). O Windows pode ser *espelhado* para exibir idiomas como hebraico ou árabe que são lidos da direita para a esquerda (RTL). Se SBT \_ RTLREADING for definido, o texto da janela de status especificado lerá na direção oposta do texto na janela pai.

Esta mensagem retorna um tamanho máximo de cadeia de caracteres de 65.535 caracteres. Se a cadeia de caracteres de texto real for maior que isso, a mensagem [**SB \_ gettext**](sb-gettext.md) truncará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **SB \_ GETTEXTLENGTHW** (Unicode) e **SB \_ GETTEXTLENGTHA** (ANSI)<br/>         |



 

 





