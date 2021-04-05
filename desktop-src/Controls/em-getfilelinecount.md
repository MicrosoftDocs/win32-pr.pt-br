---
title: Mensagem de EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtém o número de linhas em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controles de EM_GETFILELINECOUNT de mensagens do Windows
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
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085940"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é um inteiro que especifica o número total de linhas de texto no controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela. Se o controle não tiver texto, o valor de retorno será 1. O valor de retorno nunca será menor que 1.

## <a name="remarks"></a>Comentários

A mensagem em **\_ GETFILELINECOUNT** recupera o número total de linhas de texto, independentemente de como as linhas são exibidas na tela, e não apenas o número de linhas que estão visíveis no momento.

A quebra automática de linha não altera o número de linhas que essa mensagem retorna, pois essa mensagem funciona independentemente de como as linhas são exibidas na tela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



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

 

 





