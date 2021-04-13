---
title: Mensagem de EM_SELECTIONTYPE (RichEdit. h)
description: Determina o tipo de seleção para um controle de edição rico.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Controles de EM_SELECTIONTYPE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499676"
---
# <a name="em_selectiontype-message"></a>\_Mensagem de SelectionType em

Determina o tipo de seleção para um controle de edição rico.

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

## <a name="return-value"></a>Retornar valor

Se a seleção estiver vazia, o valor de retorno será \_ vazio.

Se a seleção não estiver vazia, o valor de retorno será um conjunto de sinalizadores contendo um ou mais dos valores a seguir.



| Código de retorno                                                                                     | Descrição                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**texto do SEL \_**</dt> </dl>        | Text.<br/>                            |
| <dl> <dt>**\_objeto SEL**</dt> </dl>      | Pelo menos um objeto COM.<br/>         |
| <dl> <dt>**multichar de SEL \_**</dt> </dl>   | Mais de um caractere de texto.<br/> |
| <dl> <dt>**multiobjeto SEL \_**</dt> </dl> | Mais de um objeto COM.<br/>        |



 

## <a name="remarks"></a>Comentários

Essa mensagem é útil durante o processamento de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para o pai de um controle de edição com formatação inferior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**tamanho do WM \_**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

