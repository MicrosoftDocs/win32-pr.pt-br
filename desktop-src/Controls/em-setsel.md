---
title: Mensagem de EM_SETSEL (WinUser. h)
description: Seleciona um intervalo de caracteres em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- controles de Windows de mensagem de EM_SETSEL
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 190d8a62b874d3449e0a9bf5d334a515000fb0436ba73753a8657936363071b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062886"
---
# <a name="em_setsel-message"></a>\_Mensagem em SETSEL

Seleciona um intervalo de caracteres em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A posição do caractere inicial da seleção.

</dd> <dt>

*lParam* 
</dt> <dd>

A posição do caractere final da seleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O valor inicial pode ser maior que o valor final. O menor dos dois valores especifica a posição do primeiro caractere na seleção. O valor mais alto especifica a posição do primeiro caractere além da seleção.

O valor inicial é o ponto de ancoragem da seleção e o valor final é a extremidade ativa. Se o usuário usar a tecla SHIFT para ajustar o tamanho da seleção, a extremidade ativa poderá ser movida, mas o ponto de ancoragem permanecerá o mesmo.

Se o início for 0 e o final for-1, todo o texto no controle de edição será selecionado. Se o início for-1, qualquer seleção atual será desmarcada.

**Controles de edição:** O controle exibe um cursor piscando na posição final, independentemente dos valores relativos de Start e end.

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

Se o controle de edição tiver o estilo [**es \_ NOHIDESEL**](edit-control-styles.md) , o texto selecionado será realçado, independentemente de o controle estar em foco. Sem o estilo **es \_ NOHIDESEL** , o texto selecionado só é realçado quando o controle de edição tem o foco.

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

[**em \_ GETSEL**](em-getsel.md)
</dt> <dt>

[**em \_ REPLACESEL**](em-replacesel.md)
</dt> <dt>

[**em \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**em \_ EXSETSEL**](em-exsetsel.md)
</dt> </dl>

 

 





