---
title: Mensagem de EM_TAKEFOCUS (commctrl. h)
description: Força um controle de edição de linha única a receber o foco do teclado. Você pode enviar essa mensagem explicitamente ou usando a macro Edit \_ TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- controles de Windows de mensagem de EM_TAKEFOCUS
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8283f2f9ea033439ef9ad7ec0ce40b08bb6396db8f5ebc7a9b1d513f29c209a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437136"
---
# <a name="em_takefocus-message"></a>\_Mensagem em TAKEFOCUS

\[Destinado ao uso interno; Não recomendado para uso em aplicativos. Essa mensagem pode não ter suporte em versões futuras do Windows.\]

Força um controle de edição de linha única a receber o foco do teclado. Você pode enviar essa mensagem explicitamente ou usando a macro [**Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .

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

O valor de retorno não é usado.

## <a name="security-considerations"></a>Considerações de segurança

O uso dessa mensagem pode comprometer a segurança do seu programa.

## <a name="remarks"></a>Comentários

Essa mensagem será ignorada se o controle de edição não for um controle de edição de linha única.

Se o controle de edição tiver recebido anteriormente uma mensagem em [**\_ nosetfocus**](em-nosetfocus.md) , o controle de edição parecerá ter o foco sem realmente tê-lo; caso contrário, o controle de edição receberá o foco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Editar \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[**em \_ NOsetfocus**](em-nosetfocus.md)
</dt> </dl>

 

 





