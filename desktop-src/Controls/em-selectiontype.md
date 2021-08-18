---
title: EM_SELECTIONTYPE mensagem (Richedit.h)
description: Determina o tipo de seleção para um controle de edição rico.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b79cb36759c857cea280b1c4beb5a476fa27a794f1f9985e1d259c345a9dc4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437836"
---
# <a name="em_selectiontype-message"></a>Mensagem EM \_ SELECTIONTYPE

Determina o tipo de seleção para um controle de edição rico.

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

Se a seleção estiver vazia, o valor de retorno será SEL \_ EMPTY.

Se a seleção não estiver vazia, o valor de retorno será um conjunto de sinalizadores que contém um ou mais dos valores a seguir.



| Código de retorno                                                                                     | Descrição                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**TEXTO \_ SEL**</dt> </dl>        | Text.<br/>                            |
| <dl> <dt>**OBJETO \_ SEL**</dt> </dl>      | Pelo menos um objeto COM.<br/>         |
| <dl> <dt>**SEL \_ MULTICHAR**</dt> </dl>   | Mais de um caractere de texto.<br/> |
| <dl> <dt>**SEL \_ MULTIOBJECT**</dt> </dl> | Mais de um objeto COM.<br/>        |



 

## <a name="remarks"></a>Comentários

Essa mensagem é útil durante o [**processamento do WM \_ SIZE**](/windows/desktop/winmsg/wm-size) para o pai de um controle de edição rico sem inferioridade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TAMANHO \_ DO WM**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

