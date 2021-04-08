---
title: Mensagem de LB_GETITEMDATA (WinUser. h)
description: Obtém o valor definido pelo aplicativo associado ao item da caixa de listagem especificado.
ms.assetid: 3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6
keywords:
- Controles de LB_GETITEMDATA de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETITEMDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80da838828cad7354aaa244f2218e8f9a8346755
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086326"
---
# <a name="lb_getitemdata-message"></a>GETITEMDATA de mensagens de LB \_

Obtém o valor definido pelo aplicativo associado ao item da caixa de listagem especificado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o valor associado ao item, ou erro de LB \_ se ocorrer um erro. Se o item estiver em uma caixa de listagem desenhada pelo proprietário e tiver sido criado sem o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , esse valor estará no parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lb \_ InsertString**](lb-insertstring.md) que adicionou o item à caixa de listagem. Caso contrário, é o valor no *lParam* da mensagem [**\_ SETITEMDATA de lb**](lb-setitemdata.md) .

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

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**KG \_ InsertString**](lb-insertstring.md)
</dt> <dt>

[**\_SETITEMDATA lb**](lb-setitemdata.md)
</dt> </dl>

 

 





