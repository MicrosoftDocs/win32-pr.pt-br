---
title: Mensagem de EM_GETCTFMODEBIAS (RichEdit. h)
description: Obtém os valores de tendência do modo de estrutura de serviços de texto para um controle de edição rico da Microsoft.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- controles de Windows de mensagem de EM_GETCTFMODEBIAS
topic_type:
- apiref
api_name:
- EM_GETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d6e030e3080ec9bf3d801583b9ade182483ba8560b3eccb2fb9813be7d39cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019744"
---
# <a name="em_getctfmodebias-message"></a>\_Mensagem em GETCTFMODEBIAS

Obtém os valores de tendência do modo de estrutura de serviços de texto para um controle de edição rico da Microsoft.

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

O valor de tendência do modo de estrutura de serviços de texto atual.

## <a name="remarks"></a>Comentários

Para obter a tendência do modo IME, chame em [**\_ GETIMEMODEBIAS**](em-getimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho do SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**em \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





