---
title: Mensagem de LB_INITSTORAGE (WinUser. h)
description: Aloca memória para armazenar itens da caixa de listagem. Essa mensagem é usada antes que um aplicativo adicione um grande número de itens a uma caixa de listagem.
ms.assetid: abc49049-3424-46c6-981a-b858afe88883
keywords:
- Controles de LB_INITSTORAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28216705dd0446aeb11adad9d45f9e604171e62c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455179"
---
# <a name="lb_initstorage-message"></a>INITSTORAGE de mensagens de LB \_

Aloca memória para armazenar itens da caixa de listagem. Essa mensagem é usada antes que um aplicativo adicione um grande número de itens a uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de itens a serem adicionados.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

A quantidade de memória, em bytes, a ser alocada para cadeias de caracteres de item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o valor de retorno será o número total de itens para os quais a memória foi alocada previamente, ou seja, o número total de itens adicionados por todas as mensagens **\_ INITSTORAGE de lb** bem-sucedidas.

Se a mensagem falhar, o valor de retorno será LB \_ ERRSPACE.

Microsoft Windows NT 4,0: esta mensagem não aloca a quantidade especificada de memória; no entanto, ele sempre retorna o valor especificado no parâmetro *wParam* .

## <a name="remarks"></a>Comentários

A **mensagem \_ INITSTORAGE de lb** ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens do [**lb \_ AddString**](lb-addstring.md), [**lb \_ InsertString**](lb-insertstring.md), [**lb \_ dir**](lb-dir.md)e [**lb \_ AddFile**](lb-addfile.md) tenham o menor tempo possível. Você pode usar estimativas para os parâmetros *wParam* e *lParam* . Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.

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

[**o \_ ADDfile do lb**](lb-addfile.md)
</dt> <dt>

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**Dir. de LB \_**](lb-dir.md)
</dt> <dt>

[**KG \_ InsertString**](lb-insertstring.md)
</dt> </dl>

 

 





