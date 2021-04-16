---
title: Mensagem de EM_GETWORDWRAPMODE (RichEdit. h)
description: Obtém as opções de quebra automática de palavra e de quebra de palavras para o controle de edição rico.
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- Controles de EM_GETWORDWRAPMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454763"
---
# <a name="em_getwordwrapmode-message"></a>\_Mensagem em GETwordwrapmode

Obtém as opções de quebra automática de palavra e de quebra de palavras para o controle de edição rico.

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

A mensagem retorna as opções de quebra automática de texto e de quebra de palavra atual.

## <a name="remarks"></a>Comentários

Essa mensagem não deve ser enviada pelo procedimento de quebra de palavra definido pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





