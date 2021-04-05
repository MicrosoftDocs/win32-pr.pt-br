---
title: Mensagem de EM_SETLANGOPTIONS (RichEdit. h)
description: Define opções para o IME (editor de método de entrada) e suporte a idiomas asiáticos em um controle de edição rico.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Controles de EM_SETLANGOPTIONS de mensagens do Windows
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
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918347"
---
# <a name="em_setlangoptions-message"></a>\_Mensagem em SETlangoptions

Define opções para o IME (editor de método de entrada) e suporte a idiomas asiáticos em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica as opções de idioma. Para obter uma lista de valores possíveis, consulte em [**\_ getlangoptions**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna um valor de 1.

## <a name="remarks"></a>Comentários

A mensagem em **\_ setlangoptions** controla o seguinte:

-   Associação de fonte automática.
-   Alternância automática de teclado.
-   Ajuste de tamanho de fonte automático.
-   Uso de fontes padrão de interface do usuário em vez de fontes padrão de documento.
-   Notificações ao cliente durante a composição do IME.
-   Como o IME anula o modo de composição.
-   Verificação ortográfica, AutoCorreção e previsão de teclado de toque.

Essa mensagem define os valores de todos os sinalizadores de opção de idioma. Para alterar um subconjunto dos sinalizadores, envie a mensagem em [**\_ getlangoptions**](em-getlangoptions.md) para obter os sinalizadores de opção atuais, altere os sinalizadores que você precisa alterar e, em seguida, envie a mensagem em **\_ setlangoptions** com o resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETlangoptions**](em-getlangoptions.md)
</dt> </dl>

 

 





