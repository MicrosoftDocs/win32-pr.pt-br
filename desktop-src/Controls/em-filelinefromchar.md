---
title: Mensagem de EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- controles de Windows de mensagem de EM_FILELINEFROMCHAR
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d238117a9f2ba18ae838eec32d7dc2fa12ba0833f9cdee54ce2d1a2c998944
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915626"
---
# <a name="em_filelinefromchar-message"></a>\_Mensagem em FILELINEFROMCHAR

Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela. Um índice de caracteres é o índice de base zero do caractere do início do controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de caracteres do caractere contido na linha cujo número deve ser recuperado. Se esse parâmetro for-1, **em \_ FILELINEFROMCHAR** recuperará o número de linha da linha atual (a linha que contém o cursor) ou, se houver uma seleção, o número de linha da linha que contém o início da seleção.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o número de linha com base em zero da linha que contém o índice de caracteres especificado por *wParam*, independentemente de como as linhas são exibidas na tela.

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

[**em \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





