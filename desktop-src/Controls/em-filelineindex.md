---
title: Mensagem de EM_FILELINEINDEX (CommCtrl. h)
description: Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- Controles de EM_FILELINEINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085738"
---
# <a name="em_filelineindex-message-commctrlh"></a>Mensagem de EM_FILELINEINDEX (CommCtrl. h)

Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela. Um índice de caracteres é o índice de base zero do caractere do início do controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de linha com base em zero. Um valor de-1 especifica o número de linha atual (a linha que contém o cursor).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de caracteres da linha especificada no parâmetro *wParam* , independentemente de como as linhas são exibidas na tela, ou é-1 se o número de linha especificado for maior que o número de linhas no controle de edição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 10, 1809\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2019\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ FILELINEFROMCHAR**](em-filelinefromchar.md)
</dt> </dl>

 

 





