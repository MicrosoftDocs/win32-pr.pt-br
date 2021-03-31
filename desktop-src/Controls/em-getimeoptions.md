---
title: Mensagem de EM_GETIMEOPTIONS (RichEdit. h)
description: Recupera as opções atuais do IME (editor de método de entrada).
ms.assetid: 81ec89b9-dabd-487e-805e-e3c2e58e3068
keywords:
- Controles de EM_GETIMEOPTIONS de mensagens do Windows
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
ms.openlocfilehash: 7bd805f2407fbe9e055df3d9174f106d33991aca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085936"
---
# <a name="em_getimeoptions-message"></a>\_Mensagem em GETIMEOPTIONS

Recupera as opções atuais do IME (editor de método de entrada).

> [!Note]  
> Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Não há suporte para ele em versões posteriores do rich edit.

 

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

Essa mensagem retorna um ou mais dos valores de sinalizador de opção do IME descritos na mensagem em [**\_ SETIMEOPTIONS**](em-setimeoptions.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETIMEOPTIONS**](em-setimeoptions.md)
</dt> </dl>

 

 





