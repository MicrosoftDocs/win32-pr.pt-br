---
title: Mensagem de CB_SETLOCALE (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETlocalização de CB para definir a localidade atual da caixa de combinação. Se a caixa de combinação tiver o \_ estilo de classificação CBS e as cadeias de caracteres forem adicionadas usando CB \_ AddString, a localidade de uma caixa de combinação afetará a forma como os itens de lista são classificados.
ms.assetid: 06f9c69d-1220-490f-bc67-6e125f696e87
keywords:
- controles de Windows de mensagem de CB_SETLOCALE
topic_type:
- apiref
api_name:
- CB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1647d8ff4c7a4625151a9ec099800549d831f6b55a7ef6cc6b5ead365e80e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063296"
---
# <a name="cb_setlocale-message"></a>\_Mensagem SETlocal do CB

Um aplicativo envia uma mensagem de **\_ setlocalização de CB** para definir a localidade atual da caixa de combinação. Se a caixa de combinação tiver o estilo de [**\_ classificação CBS**](combo-box-styles.md) e as cadeias de caracteres forem adicionadas usando [**CB \_ AddString**](cb-addstring.md), a localidade de uma caixa de combinação afetará a forma como os itens de lista são classificados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o identificador de localidade para a caixa de combinação a ser usada para classificação ao adicionar texto.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o identificador de localidade anterior. Se *wParam* especificar uma localidade não instalada no sistema, o valor de retorno será CB \_ Err e a localidade da caixa de combinação atual não será alterada.

## <a name="remarks"></a>Comentários

Use a macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir um identificador de localidade e a macro [**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid) para construir um identificador de idioma. O identificador de idioma é composto por um identificador de idioma primário e um identificador de subidioma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**AddString CB \_**](cb-addstring.md)
</dt> <dt>

[**\_ISlocalização CB**](cb-getlocale.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/winnt/nf-winnt-makelangid)
</dt> <dt>

[**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid)
</dt> </dl>

 

