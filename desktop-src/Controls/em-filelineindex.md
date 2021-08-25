---
title: EM_FILELINEINDEX mensagem (CommCtrl.h)
description: Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição multilinha, independentemente de como as linhas são exibidas na tela.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX controles Windows mensagem
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
ms.openlocfilehash: df7c4bd1f21ee6bcdf7bec56828ea9c2996c837def614c0c537ef83ee053ebfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915606"
---
# <a name="em_filelineindex-message-commctrlh"></a>EM_FILELINEINDEX mensagem (CommCtrl.h)

Obtém o índice de caracteres do primeiro caractere de uma linha especificada em um controle de edição multilinha, independentemente de como as linhas são exibidas na tela.. Um índice de caracteres é o índice baseado em zero do caractere desde o início do controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de linha baseado em zero. Um valor de -1 especifica o número de linha atual (a linha que contém o aro).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice de caracteres da linha especificada no parâmetro *wParam,* independentemente de como as linhas são exibidas na tela ou é -1 se o número de linha especificado for maior que o número de linhas no controle de edição.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, somente 1809 \[ aplicativos da área de trabalho\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2019 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ FILELINEFROMCHAR**](em-filelinefromchar.md)
</dt> </dl>

 

 





