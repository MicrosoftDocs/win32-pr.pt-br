---
title: Mensagem de EM_FORMATRANGE (RichEdit. h)
description: Formata um intervalo de texto em um controle de edição rico para um dispositivo específico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- Controles de EM_FORMATRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FORMATRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8f235fb054643623510ea23e73001aaeb070be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824478"
---
# <a name="em_formatrange-message"></a>\_Mensagem em FORMATRANGE

Formata um intervalo de texto em um controle de edição rico para um dispositivo específico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se o texto deve ser renderizado. Se esse parâmetro não for zero, o texto será renderizado. Caso contrário, o texto é apenas medido.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que contém informações sobre o dispositivo de saída ou **NULL** para liberar informações armazenadas em cache pelo controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna o índice do último caractere que se ajusta à região, mais 1.

## <a name="remarks"></a>Comentários

Essa mensagem é normalmente usada para formatar o conteúdo do controle de edição rico para um dispositivo de saída, como uma impressora.

Depois de usar essa mensagem para formatar um intervalo de texto, é importante que você libere informações armazenadas em cache enviando **em \_ FORMATRANGE** novamente, mas com *lParam* definido como **NULL**; caso contrário, ocorrerá um vazamento de memória. Além disso, depois de usar essa mensagem para um dispositivo, você deve liberar as informações em cache antes de usá-las novamente para um dispositivo diferente.

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

[**em \_ DISPLAYBAND**](em-displayband.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Imprimindo controles de edição avançada](printing-rich-edit-controls.md)
</dt> </dl>

 

 





