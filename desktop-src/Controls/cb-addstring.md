---
title: Mensagem de CB_ADDSTRING (WinUser. h)
description: Adiciona uma cadeia de caracteres à caixa de listagem de uma caixa de combinação. Se a caixa de combinação não tiver o \_ estilo de classificação CBS, a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.
ms.assetid: 201bcb7b-e7d1-41e6-8eb7-a5864b659a52
keywords:
- Controles de CB_ADDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda16367ec24e869f6cb664e89751d7a13efec3c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918990"
---
# <a name="cb_addstring-message"></a>\_Mensagem ADDSTRING CB

Adiciona uma cadeia de caracteres à caixa de listagem de uma caixa de combinação. Se a caixa de combinação não tiver o estilo de [**\_ classificação CBS**](combo-box-styles.md) , a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro **LPCTSTR** para a cadeia de caracteres terminada em nulo a ser adicionado. Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o valor do parâmetro *lParam* será armazenado como dados de item, e não a cadeia de caracteres que, de outra forma, apontaria para. Os dados do item podem ser recuperados ou modificados enviando a mensagem [**CB \_ GETITEMDATA**](cb-getitemdata.md) ou [**CB \_ SETITEMDATA**](cb-setitemdata.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de base zero para a cadeia de caracteres na caixa de listagem da caixa de combinação. Se ocorrer um erro, o valor de retorno será CB \_ Err. Se o espaço insuficiente estiver disponível para armazenar a nova cadeia de caracteres, ele será CB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

Se você criar uma caixa de combinação desenhada pelo proprietário com o estilo de [**\_ classificação CBS**](combo-box-styles.md) , mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , a mensagem do [**WM \_ COMPAREITEM**](wm-compareitem.md) será enviada uma ou mais vezes ao proprietário da caixa de combinação para que o novo item possa ser colocado corretamente na lista.

Para inserir uma cadeia de caracteres em um local específico dentro da lista, use a mensagem de [**\_ inserção de CB**](cb-insertstring.md) .

Se a caixa de combinação tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você adicionar uma cadeia de caracteres mais larga do que a caixa de combinação, envie uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.

**Comclt32.dll versão 5,0 ou posterior:** Se a configuração de [**\_ maiúsculas**](combo-box-styles.md) e [**\_ minúsculas**](combo-box-styles.md) do CBS for definida, a versão Unicode do **CB \_ AddString** alterará a cadeia de caracteres. Se estiver usando memória global somente leitura, isso fará com que o aplicativo falhe.

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

[**\_pasta CB**](cb-dir.md)
</dt> <dt>

[**inserção de CB \_**](cb-insertstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**COMPAREITEM do WM \_**](wm-compareitem.md)
</dt> </dl>

 

