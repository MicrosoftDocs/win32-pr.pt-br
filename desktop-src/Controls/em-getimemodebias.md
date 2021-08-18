---
title: EM_GETIMEMODEBIAS mensagem (Richedit.h)
description: Recupera o desvio de modo do IME (Editor de Método de Entrada) para um controle Microsoft Rich Edit.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- EM_GETIMEMODEBIAS controles Windows mensagem
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad5504ca2e5ac1a332657c4f539c9f983292617b6e74b949598488ceb38dfa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019534"
---
# <a name="em_getimemodebias-message"></a>Mensagem EM \_ GETIMEMODEBIAS

Recupera o desvio de modo do IME (Editor de Método de Entrada) para um controle Microsoft Rich Edit.

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

Essa mensagem retorna a configuração de desvio de modo IME atual.

## <a name="remarks"></a>Comentários

Para obter o desvio Estrutura de Serviços de Texto modo de uso, use [**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md).

O aplicativo deve chamar [**EM \_ ISIME antes**](em-isime.md) de chamar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> </dl>

 

 





