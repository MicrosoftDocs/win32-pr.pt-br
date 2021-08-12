---
title: EM_SETIMEMODEBIAS mensagem (Richedit.h)
description: Definir o desvio de modo do IME (Editor de Método de Entrada) para um controle de edição rico.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS controles Windows mensagem
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
ms.openlocfilehash: b4812c21558fba07be2709c0fd1a011f31d79fad17e0b4146fa0c7d65843a087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672666"
---
# <a name="em_setimemodebias-message"></a>Mensagem EM \_ SETIMEMODEBIAS

Definir o desvio de modo do IME (Editor de Método de Entrada) para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de desvio do modo IME. Pode ser um dos seguintes.



| Valor                                                                                                                                                                                        | Significado                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**IMF \_ SMODE \_ PLAURALCLAUSE**</dt> </dl> | Define o desvio de modo IME como Nome.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**IMF \_ SMODE \_ NONE**</dt> </dl>                            | Sem desvio.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse deve ser o mesmo valor que *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem retorna a nova configuração de desvio de modo IME.

## <a name="remarks"></a>Comentários

Quando o IME gera uma lista de opções alternativas para um conjunto de caracteres, essa mensagem define os critérios pelos quais algumas das opções aparecerão na parte superior da lista.

Para definir o desvio Estrutura de Serviços de Texto (TSF), use [**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md).

O aplicativo deve chamar [**EM \_ ISIME antes**](em-isime.md) de chamar essa função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 





