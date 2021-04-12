---
title: Mensagem de EM_REDO (RichEdit. h)
description: Envia uma \_ mensagem em em um controle de edição rico para refazer a próxima ação na fila de restauração do controle.
ms.assetid: 28ec1ec2-a56d-442f-b3cb-9feeb92edaeb
keywords:
- Controles de EM_REDO de mensagens do Windows
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
ms.openlocfilehash: bba7a684db0d40ebcfeec4a540989c4dab4c5dd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455441"
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

## <a name="return-value"></a>Retornar valor

Se a operação de **refazer** for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação de **refazer** falhar, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

Para determinar se há alguma ação na fila de restauração do controle, envie a mensagem [**em \_ refazer**](em-canredo.md) .

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

[**em \_ refazer**](em-canredo.md)
</dt> <dt>

[**em \_ refazer**](em-getredoname.md)
</dt> <dt>

[**em \_ GETundoname**](em-getundoname.md)
</dt> <dt>

[**em \_ desfazer**](em-undo.md)
</dt> </dl>

 

 





