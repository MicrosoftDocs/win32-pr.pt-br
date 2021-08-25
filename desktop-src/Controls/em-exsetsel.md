---
title: EM_EXSETSEL mensagem (Richedit.h)
description: Seleciona um intervalo de caracteres ou objetos COMPONENT OBJECT MODEL (COM) em um controle Microsoft Rich Edit.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL controles de Windows mensagem
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e35840e404f295b7d3ed6ddd5dddf4c77076c236eb3260f6f719b152cef207
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915646"
---
# <a name="em_exsetsel-message"></a>Mensagem EM \_ EXSETSEL

Seleciona um intervalo de caracteres ou objetos COMPONENT OBJECT MODEL (COM) em um controle Microsoft Rich Edit.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado; ele deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Uma [**estrutura CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) que especifica o intervalo de seleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é a seleção que está realmente definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





