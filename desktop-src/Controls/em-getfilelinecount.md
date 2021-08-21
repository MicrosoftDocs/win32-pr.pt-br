---
title: Mensagem de EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtém o número de linhas em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- controles de Windows de mensagem de EM_GETFILELINECOUNT
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 28539af32212a699e12d2cf1d1787fa2e7aaa224f374eb6a63717279fcad16b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019674"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>Mensagem de EM_GETFILELINECOUNT (CommCtrl. h)

Obtém o número de linhas em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.

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

O valor de retorno é um inteiro que especifica o número total de linhas de texto no controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela. Se o controle não tiver texto, o valor de retorno será 1. O valor de retorno nunca será menor que 1.

## <a name="remarks"></a>Comentários

A mensagem em **\_ GETFILELINECOUNT** recupera o número total de linhas de texto, independentemente de como as linhas são exibidas na tela, e não apenas o número de linhas que estão visíveis no momento.

A quebra automática de linha não altera o número de linhas que essa mensagem retorna, pois essa mensagem funciona independentemente de como as linhas são exibidas na tela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, 1809 \[ aplicativos de área de trabalho apenas\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2019\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETfilee**](em-getfileline.md)
</dt> <dt>

[**em \_ FILELINELENGTH**](em-filelinelength.md)
</dt> <dt>

[**Editar \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





