---
title: Mensagem de EM_SETIMEMODEBIAS (RichEdit. h)
description: Defina a tendência do modo IME (editor de método de entrada) para um controle de edição rico.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Controles de EM_SETIMEMODEBIAS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455347"
---
# <a name="em_setimemodebias-message"></a>\_Mensagem em SETIMEMODEBIAS

Defina a tendência do modo IME (editor de método de entrada) para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de tendência do modo IME. Pode ser um dos seguintes.



| Valor                                                                                                                                                                                        | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**\_PLAURALCLAUSE SMODE do IMF \_**</dt> </dl> | Define o ajuste do modo IME para nome.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**SMODE do IMF \_ \_ nenhum**</dt> </dl>                            | Sem tendência.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser o mesmo valor que *wParam*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna a nova configuração de ajuste do modo IME.

## <a name="remarks"></a>Comentários

Quando o IME gera uma lista de opções alternativas para um conjunto de caracteres, essa mensagem define os critérios pelos quais algumas das opções aparecerão na parte superior da lista.

Para definir a tendência do modo TSF (estrutura de serviços de texto), use em [**\_ SETCTFMODEBIAS**](em-setctfmodebias.md).

O aplicativo deve chamar [**em \_ ISIME**](em-isime.md) antes de chamar essa função.

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

[**em \_ ISIME**](em-isime.md)
</dt> <dt>

[**em \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 





