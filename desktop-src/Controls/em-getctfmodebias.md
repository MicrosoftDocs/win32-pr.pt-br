---
title: Mensagem de EM_GETCTFMODEBIAS (RichEdit. h)
description: Obtém os valores de tendência do modo de estrutura de serviços de texto para um controle de edição rico da Microsoft.
ms.assetid: 2421d37d-169d-480f-a5f7-4c6033ca6c1a
keywords:
- Controles de EM_GETCTFMODEBIAS de mensagens do Windows
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
ms.openlocfilehash: 109d5eabbddca1c13fefae99c29d8c550fbd274e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085676"
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

## <a name="return-value"></a>Retornar valor

O valor de tendência do modo de estrutura de serviços de texto atual.

## <a name="remarks"></a>Comentários

Para obter a tendência do modo IME, chame em [**\_ GETIMEMODEBIAS**](em-getimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> <dt>

[**em \_ GETIMEMODEBIAS**](em-getimemodebias.md)
</dt> </dl>

 

 





