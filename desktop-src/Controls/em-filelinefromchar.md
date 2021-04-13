---
title: Mensagem de EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtém o índice da linha que contém o índice de caracteres especificado em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- Controles de EM_FILELINEFROMCHAR de mensagens do Windows
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
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455351"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de linha com base em zero da linha que contém o índice de caracteres especificado por *wParam*, independentemente de como as linhas são exibidas na tela.

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

[**em \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





