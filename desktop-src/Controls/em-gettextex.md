---
title: Mensagem de EM_GETTEXTEX (RichEdit. h)
description: Obtém o texto de um controle de edição rico.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Controles de EM_GETTEXTEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455067"
---
# <a name="em_gettextex-message"></a>\_Mensagem em GETTEXTEX

Obtém o texto de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ponteiro para uma estrutura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , que indica como converter o texto antes de colocá-lo no buffer de saída.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para o buffer para receber o texto. O tamanho desse buffer, em bytes, é especificado pelo membro **CB** da estrutura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) . Use a mensagem em [**\_ GETTEXTLENGTHEX**](em-gettextlengthex.md) para obter o tamanho necessário do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o número de **TCHAR** s copiadas no buffer de saída, incluindo o terminador nulo.

## <a name="remarks"></a>Comentários

Se o tamanho do buffer de saída for menor que o tamanho do texto no controle, o controle de edição copiará o texto do seu início e o posicionará no buffer até que o buffer esteja cheio. Um caractere nulo de terminação ainda será colocado no final do buffer.

Se o texto ANSI for solicitado, em **\_ GETTEXTEX** usará a função [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para converter os caracteres Unicode em ANSI. Ele permite que você vá de Unicode para ANSI usando uma página de código específica. A estrutura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contém membros (**lpDefaultChar** e **lpUsedDefChar**) que são usados na conversão de Unicode para ANSI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETTEXTEX**](em-settextex.md)
</dt> <dt>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**SetText do WM \_**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

