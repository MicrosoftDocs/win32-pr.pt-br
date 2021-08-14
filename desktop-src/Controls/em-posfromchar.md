---
title: EM_POSFROMCHAR mensagem (Winuser.h)
description: Recupera as coordenadas de área do cliente de um caractere especificado em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- EM_POSFROMCHAR controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1d9d2dccb6ccf1bd80b44b2221f8628f13e595ee514074956e7869447d513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437876"
---
# <a name="em_posfromchar-message"></a>Mensagem \_ EM POSFROMCHAR

Recupera as coordenadas de área do cliente de um caractere especificado em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edição Rich 1.0 e 3.0:** Um ponteiro para uma [**estrutura POINTL**](/previous-versions//dd162807(v=vs.85)) que recebe as coordenadas de área do cliente do caractere. As coordenadas estão em unidades de tela e são relativas ao canto superior esquerdo da área de cliente do controle.

**Editar controles e Edição 2.0 rich:** O índice baseado em zero do caractere.

</dd> <dt>

*lParam* 
</dt> <dd>

**Edição Rich 1.0 e 3.0:** O índice baseado em zero do caractere.

**Editar controles e Edição 2.0 rich:** Esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**Edição Rich 1.0 e 3.0:** O valor de retorno não é usado.

**Editar controles e Edição 2.0 rich:** O valor de retorno contém as coordenadas de área do cliente do caractere. A [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém a coordenada horizontal e [**a HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém a coordenada vertical.

## <a name="remarks"></a>Comentários

Uma coordenada retornada poderá ser um valor negativo se o caractere especificado não for exibido na área de cliente do controle de edição. As coordenadas são truncadas para valores inteiros.

Se o caractere for um caractere de linha, as coordenadas retornadas indicarão um ponto logo após o último caractere visível na linha. Se o índice especificado for maior que o índice do último caractere no controle, o controle retornará -1.

**Edição Rich 3.0 e posterior:** Para compatibilidade com backward, o Microsoft Rich Edit 3.0 dá suporte à sintaxe usada pelo Microsoft Rich Edit 2.0. Se o Microsoft Rich Edit 3.0 detectar que *wParam* não é um ponteiro [**POINTL**](/previous-versions//dd162807(v=vs.85)) válido, ele assumirá que a mensagem foi enviada usando a sintaxe Microsoft Rich Edit 2.0. Nesse caso, ele usa o valor de retorno para retornar as coordenadas.

**Edição rica:** Com suporte no Microsoft Rich Edit 1.0 e posterior. Para obter informações sobre a compatibilidade de versões de edição rich com as várias versões do sistema, consulte [Sobre controles de edição rich](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ CHARFROMPOS**](em-charfrompos.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**POINTL**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

