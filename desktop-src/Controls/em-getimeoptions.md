---
title: EM_GETIMEOPTIONS mensagem (Richedit.h)
description: Recupera as opções atuais do IME (Editor de Método de Entrada).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- EM_GETIMEOPTIONS controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4513189014969dbfdf69a0ad257cbfde6a4ff99c2499f478c4865100a23c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049056"
---
# <a name="em_getimeoptions-message"></a>Mensagem EM \_ GETIMEOPTIONS

Recupera as opções atuais do IME (Editor de Método de Entrada).

> [!Note]  
> Essa mensagem só tem suporte em versões de idioma asiático do Microsoft Rich Edit 1.0. Não há suporte para ele em nenhuma versão posterior do Rich Edit.

 

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

Essa mensagem retorna um ou mais dos valores de sinalizador de opção IME descritos na [**mensagem EM \_ SETIMEOPTIONS.**](em-setimeoptions.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ SETIMEOPTIONS**](em-setimeoptions.md)
</dt> </dl>

 

 





