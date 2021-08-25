---
title: EM_FORMATRANGE mensagem (Richedit.h)
description: Formatar um intervalo de texto em um controle de edição rico para um dispositivo específico.
ms.assetid: 6d1e562b-d741-4d4a-a395-554083cb0dbb
keywords:
- EM_FORMATRANGE controles de Windows mensagem
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
ms.openlocfilehash: 941aceb8c8f91657c7f78aba3d83a627fc413ed20d71217c933c6fba9b6f39e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049346"
---
# <a name="em_formatrange-message"></a>Mensagem EM \_ FORMATRANGE

Formatar um intervalo de texto em um controle de edição rico para um dispositivo específico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se o texto deve ser renderizar. Se esse parâmetro não for zero, o texto será renderizado. Caso contrário, o texto será apenas medido.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura FORMATRANGE**](/windows/desktop/api/Richedit/ns-richedit-formatrange) que contém informações sobre o dispositivo de saída ou **NULL** para liberar informações armazenadas em cache pelo controle .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna o índice do último caractere que se encaixa na região, mais 1.

## <a name="remarks"></a>Comentários

Normalmente, essa mensagem é usada para formatar o conteúdo do controle de edição rich para um dispositivo de saída, como uma impressora.

Depois de usar essa mensagem para formatar um intervalo de texto, é importante liberar informações armazenadas em cache enviando **EM \_ FORMATRANGE** novamente, mas com *lParam definido* como **NULL;** caso contrário, ocorrerá um vazamento de memória. Além disso, depois de usar essa mensagem para um dispositivo, você deve liberar informações armazenadas em cache antes de usá-la novamente para um dispositivo diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ DISPLAYBAND**](em-displayband.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Imprimindo controles de edição rich](printing-rich-edit-controls.md)
</dt> </dl>

 

 





