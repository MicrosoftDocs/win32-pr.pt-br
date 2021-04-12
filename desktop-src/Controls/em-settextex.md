---
title: Mensagem de EM_SETTEXTEX (RichEdit. h)
description: Combina a funcionalidade das mensagens do WM \_ SetText e em \_ REPLACESEL e adiciona a capacidade de definir texto usando uma página de código e usar Rich Text ou texto sem formatação.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Controles de EM_SETTEXTEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455344"
---
# <a name="em_settextex-message"></a>\_Mensagem em SETTEXTEX

Combina a funcionalidade das mensagens do [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext) e em [**\_ REPLACESEL**](em-replacesel.md) e adiciona a capacidade de definir texto usando uma página de código e usar Rich Text ou texto sem formatação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) que especifica sinalizadores e uma página de código opcional a ser usada na tradução para Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o texto terminado em nulo a ser inserido. Esse texto é uma cadeia de caracteres ANSI, a menos que a página de código seja 1200 (Unicode). Se *lParam* começar com uma sequência ASCII de RTF válida, por exemplo, "{ \\ RTF" ou "{urtf", o texto será lido usando o leitor de RTF.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação estiver definindo todo o texto e for bem sucedido, o valor de retorno será 1.

Se a operação estiver definindo a seleção e tiver sucesso, o valor de retorno será o número de bytes ou caracteres copiados.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETTEXTEX**](em-gettextex.md)
</dt> <dt>

[**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

