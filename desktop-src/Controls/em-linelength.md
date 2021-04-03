---
title: Mensagem de EM_LINELENGTH (WinUser. h)
description: Recupera o comprimento, em caracteres, de uma linha em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- Controles de EM_LINELENGTH de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce3cbf59cbe31886e55c34bce9f7c2421e431012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824644"
---
# <a name="em_linelength-message"></a>\_Mensagem em LINELENGTH

Recupera o comprimento, em caracteres, de uma linha em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de caracteres de um caractere na linha cujo comprimento deve ser recuperado. Se esse parâmetro for maior que o número de caracteres no controle, o valor de retorno será zero.

Esse parâmetro pode ser-1. Nesse caso, a mensagem retorna o número de caracteres não selecionados em linhas que contêm os caracteres selecionados. Por exemplo, se a seleção estendida do quarto caractere de uma linha até o oitavo caractere do final da linha seguinte, o valor de retorno será 10 (três caracteres na primeira linha e sete no próximo).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para controles de edição de várias linhas, o valor de retorno é o comprimento, em **TCHAR** s, da linha especificada pelo parâmetro *wParam* . Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres. Ele não inclui o caractere de retorno de carro no final da linha.

Para controles de edição de linha única, o valor de retorno é o comprimento, em **TCHAR** s, do texto no controle de edição.

Se *wParam* for maior que o número de caracteres no controle, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Use a mensagem em [**\_ LINEINDEX**](em-lineindex.md) para recuperar um índice de caracteres para um determinado número de linha dentro de um controle de edição de várias linhas.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ LINEINDEX**](em-lineindex.md)
</dt> </dl>

 

 





