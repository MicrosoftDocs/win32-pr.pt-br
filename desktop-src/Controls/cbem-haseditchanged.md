---
title: Mensagem de CBEM_HASEDITCHANGED (commctrl. h)
description: Determina se o usuário alterou o texto de um controle de edição ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Controles de CBEM_HASEDITCHANGED de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919173"
---
# <a name="cbem_haseditchanged-message"></a>\_Mensagem CBEM HASEDITCHANGED

Determina se o usuário alterou o texto de um controle de edição ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se o texto na caixa de edição do controle tiver sido alterado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Um controle ComboBoxEx usa um controle de caixa de edição quando ele é definido como o estilo [**\_ suspenso CBS**](combo-box-styles.md) . Você pode recuperar o identificador de janela do controle caixa de edição enviando uma mensagem [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .

Quando o usuário começar a editar, você receberá uma notificação [CBEN \_ BEGINEDIT](cben-beginedit.md) . Quando a edição for concluída ou o foco for alterado, você receberá uma notificação [CBEN \_ ENDEDIT](cben-endedit.md) . A mensagem **CBEM \_ HASEDITCHANGED** só é útil para determinar se o texto foi alterado, caso seja enviado antes da notificação de CBEN \_ ENDEDIT. Se a mensagem for enviada posteriormente, retornará **false**. Por exemplo, suponha que o usuário comece a editar o texto na caixa de edição, mas altera o foco, gerando uma \_ notificação CBEN ENDEDIT. Se você enviar uma mensagem **CBEM \_ HASEDITCHANGED** , ela retornará **false**, embora o texto tenha sido alterado.

O [**estilo \_ simples do CBS**](combo-box-styles.md) não funciona corretamente com **CBEM \_ HASEDITCHANGED**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





