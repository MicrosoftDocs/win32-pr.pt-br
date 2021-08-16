---
title: Mensagem de EM_GETLIMITTEXT (WinUser. h)
description: Obtém o limite de texto atual para um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 778967f0-c090-46a2-9f27-194b17bbb1be
keywords:
- controles de Windows de mensagem de EM_GETLIMITTEXT
topic_type:
- apiref
api_name:
- EM_GETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de2066bf03fd8ea05851a9cef58f4e308db49f82bdee94c2d503cadf1c20a2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831677"
---
# <a name="em_getlimittext-message"></a>\_Mensagem em GETLIMITTEXT

Obtém o limite de texto atual para um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o limite de texto.

## <a name="remarks"></a>Comentários

**Edite controles, edição avançada 2,0 e posterior:** O limite de texto é a quantidade máxima de texto, em **TCHAR** s, que o controle pode conter. Para texto ANSI, este é o número de bytes; para texto Unicode, este é o número de caracteres. Dois documentos com o mesmo limite de caracteres resultarão no mesmo limite de texto, mesmo se um for ANSI e o outro for Unicode.

**Edição avançada 1,0:** O limite de texto é a quantidade máxima de texto, em bytes, que o controle de edição rico pode conter.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 





