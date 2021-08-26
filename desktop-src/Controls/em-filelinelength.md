---
title: EM_FILELINELENGTH mensagem (CommCtrl.h)
description: Recupera o comprimento, em caracteres, de uma linha em um controle de edição, independentemente de como as linhas são exibidas na tela.
ms.assetid: cfb0632c-9ba9-4864-939a-dbbaed6c177e
keywords:
- EM_FILELINELENGTH controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_FILELINELENGTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cb05b0e2acbfb5049eddefab1dad42ecd7b6db234fa4a3c34d4877ed52b007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915536"
---
# <a name="em_filelinelength-message"></a>Mensagem EM \_ FILELINELENGTH

Recupera o comprimento, em caracteres, de uma linha em um controle de edição, independentemente de como as linhas são exibidas na tela.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de caracteres de um caractere na linha cujo comprimento deve ser recuperado. Se esse parâmetro for maior que o número de caracteres no controle , o valor de retorno será zero.

Esse parâmetro pode ser -1. Nesse caso, a mensagem retorna o número de caracteres não selecionados em linhas que contêm caracteres selecionados. Por exemplo, se a seleção se estendeu do quarto caractere de uma linha até o oitavo caractere do final da próxima linha, o valor de retorno seria 10 (três caracteres na primeira linha e sete na próxima).

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para controles de edição multilinha, o valor de retorno é o comprimento, em **TCHAR** s, da linha especificada pelo *parâmetro wParam,* independentemente de como as linhas são exibidas na tela. Ele não inclui o caractere de retorno de carro ou de linha no final da linha.

Para controles de edição de linha única, o valor de retorno é o comprimento, em **TCHAR** s, do texto no controle de edição.

Se *wParam* for maior que o número de caracteres no controle, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Use a [**mensagem EM \_ FILELINEINDEX**](em-lineindex.md) para recuperar um índice de caracteres para um determinado número de linha dentro de um controle de edição multilinha, independentemente de como as linhas são exibidas na tela.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, somente 1809 \[ aplicativos da área de trabalho\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2019 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>CommCtrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ FILELINEINDEX**](em-filelineindex.md)
</dt> </dl>

 

 





