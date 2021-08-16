---
title: EM_SETLANGOPTIONS mensagem (Richedit.h)
description: Define opções para o IME (Editor de Método de Entrada) e o suporte a idiomas asiáticos em um controle de edição rico.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5984c20273d2daa0a2e39fc6caf6dde88c8b274502a50e1a5e5eb3cca2b6f94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831187"
---
# <a name="em_setlangoptions-message"></a>Mensagem EM \_ SETLANGOPTIONS

Define opções para o IME (Editor de Método de Entrada) e o suporte a idiomas asiáticos em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica as opções de idioma. Para obter uma lista de valores possíveis, consulte [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna um valor de 1.

## <a name="remarks"></a>Comentários

A **mensagem EM \_ SETLANGOPTIONS** controla o seguinte:

-   Associação automática de fonte.
-   Alternamento automático de teclado.
-   Ajuste automático de tamanho da fonte.
-   Uso de fontes padrão da interface do usuário em vez de fontes padrão do documento.
-   Notificações ao cliente durante a composição do IME.
-   Como o IME anula o modo de composição.
-   Verificação ortografia, correção automática e previsão de teclado por toque.

Essa mensagem define os valores de todos os sinalizadores de opção de idioma. Para alterar um subconjunto dos sinalizadores, envie a mensagem [**EM \_ GETLANGOPTIONS**](em-getlangoptions.md) para obter os sinalizadores de opção atuais, altere os sinalizadores que você precisa alterar e, em seguida, envie a mensagem **EM \_ SETLANGOPTIONS** com o resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETLANGOPTIONS**](em-getlangoptions.md)
</dt> </dl>

 

 





