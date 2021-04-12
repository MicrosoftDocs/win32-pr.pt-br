---
title: Mensagem de EM_POSFROMCHAR (WinUser. h)
description: Recupera as coordenadas da área do cliente de um caractere especificado em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Controles de EM_POSFROMCHAR de mensagens do Windows
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
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499442"
---
# <a name="em_posfromchar-message"></a>\_Mensagem em POSFROMCHAR

Recupera as coordenadas da área do cliente de um caractere especificado em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Edição avançada 1,0 e 3,0:** Um ponteiro para uma estrutura [**pontual**](/previous-versions//dd162807(v=vs.85)) que recebe as coordenadas da área de cliente do caractere. As coordenadas estão em unidades de tela e são relativas ao canto superior esquerdo da área do cliente do controle.

**Editar controles e edição avançada 2,0:** O índice de base zero do caractere.

</dd> <dt>

*lParam* 
</dt> <dd>

**Edição avançada 1,0 e 3,0:** O índice de base zero do caractere.

**Editar controles e edição avançada 2,0:** Esse parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**Edição avançada 1,0 e 3,0:** O valor de retorno não é usado.

**Editar controles e edição avançada 2,0:** O valor de retorno contém as coordenadas da área do cliente do caractere. O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém a coordenada horizontal e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém a coordenada vertical.

## <a name="remarks"></a>Comentários

Uma coordenada retornada pode ser um valor negativo se o caractere especificado não for exibido na área do cliente do controle de edição. As coordenadas são truncadas para valores inteiros.

Se o caractere for um delimitador de linha, as coordenadas retornadas indicarão um ponto apenas além do último caractere visível na linha. Se o índice especificado for maior que o índice do último caractere no controle, o controle retornará-1.

**Edição avançada 3,0 e posterior:** Para compatibilidade com versões anteriores, o Microsoft Rich Edit 3,0 dá suporte à sintaxe usada pelo Microsoft rich edit 2,0. Se o Microsoft Rich Edit 3,0 detectar que *wParam* não é um ponteiro [**pointal**](/previous-versions//dd162807(v=vs.85)) válido, ele assumirá que a mensagem foi enviada usando a sintaxe Microsoft rich edit 2,0. Nesse caso, ele usa o valor de retorno para retornar as coordenadas.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ CHARFROMPOS**](em-charfrompos.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**PONTO**](/previous-versions//dd162807(v=vs.85))
</dt> </dl>

 

