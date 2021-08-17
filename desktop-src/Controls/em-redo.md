---
title: Mensagem de EM_REDO (RichEdit. h)
description: Envia uma \_ mensagem em em um controle de edição rico para refazer a próxima ação na fila de restauração do controle.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- controles de Windows de mensagem de EM_REDO
topic_type:
- apiref
api_name:
- EM_REDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39b679e8bf7e78cf7ce028d0bb440438770d0d0123516313fb418b2136ebc11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437856"
---
# <a name="em_redo-message"></a>\_Mensagem em restauração

Envia uma **mensagem \_ em em um controle** de edição rico para refazer a próxima ação na fila de restauração do controle.

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

Se a operação de **refazer** for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação de **refazer** falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Para determinar se há alguma ação na fila de restauração do controle, envie a mensagem [**em \_ refazer**](em-canredo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ refazer**](em-canredo.md)
</dt> <dt>

[**em \_ refazer**](em-getredoname.md)
</dt> <dt>

[**em \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> </dl>

 

 





