---
title: Mensagem de EM_GETIMEMODEBIAS (RichEdit. h)
description: Recupera o ajuste do modo IME (editor de método de entrada) para um controle de edição rico da Microsoft.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Controles de EM_GETIMEMODEBIAS de mensagens do Windows
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
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009564"
---
# <a name="em_getimemodebias-message"></a>\_Mensagem em GETIMEMODEBIAS

Recupera o ajuste do modo IME (editor de método de entrada) para um controle de edição rico da Microsoft.

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

Essa mensagem retorna a configuração de ajuste do modo IME atual.

## <a name="remarks"></a>Comentários

Para obter a tendência do modo de estrutura de serviços de texto, use em [**\_ GETCTFMODEBIAS**](em-getctfmodebias.md).

O aplicativo deve chamar [**em \_ ISIME**](em-isime.md) antes de chamar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ ISIME**](em-isime.md)
</dt> <dt>

[**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> </dl>

 

 





