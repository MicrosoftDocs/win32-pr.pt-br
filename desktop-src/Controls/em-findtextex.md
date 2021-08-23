---
title: Mensagem de EM_FINDTEXTEX (RichEdit. h)
description: Mensagem de EM_FINDTEXTEX-localiza o texto em um controle de edição rico.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- controles de Windows de mensagem de EM_FINDTEXTEX
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f5121108fcd75d3b57b3ef61a8dc789bd92f731a3593314036d4d9507e6252
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541186"
---
# <a name="em_findtextex-message"></a>\_Mensagem em FINDTEXTEX

Localiza texto em um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o comportamento da operação de pesquisa. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ para baixo**</dt> </dl>                               | Microsoft rich edit 2,0 e posterior: se definido, a pesquisa será encaminhada de **FINDTEXTEX. chrg. cpMin**; Se não estiver definido, a pesquisa será regressiva de **FINDTEXTEX. chrg. cpMin**. <br/> Microsoft Rich Edit 1,0: o \_ sinalizador fr down é ignorado. A pesquisa está sempre em frente.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**\_MATCHALEFHAMZA fr**</dt> </dl> | Microsoft Rich Edit 3,0 e posterior: se definido, a pesquisa diferencia entre os Alef árabe e Hebraico com acentos diferentes. Se não estiver definido, todos os Alef serão correspondidos apenas pelo Alef caractere. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**\_MATCHCASE fr**</dt> </dl>                | Se definido, a operação de pesquisa diferencia maiúsculas de minúsculas. Se não for definido, a operação de pesquisa não diferenciará maiúsculas de minúsculas. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará as marcas de diacríticos árabe e Hebraico. Se não estiver definido, as marcas de diacríticos serão ignoradas. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**\_MATCHKASHIDA fr**</dt> </dl>       | Microsoft Rich Edit 3,0 e posterior: se definido, a operação de pesquisa considerará os kashidas árabe e Hebraico. Se não estiver definido, os kashidas serão ignorados. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa. Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contém informações sobre a operação Find.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência. Se o destino não for encontrado, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

Use esta mensagem para localizar cadeias de caracteres ANSI. Para Unicode, use [**em \_ FINDTEXTEXW**](em-findtextexw.md).

O membro **cpMin** de **FINDTEXTEX. chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade. Ao pesquisar em retrocesso, **cpMin** deve ser igual ou maior que **cpMax**. Ao pesquisar em frente, um valor de-1 em **cpMax** estende o intervalo de pesquisa até o final do texto.

Se a operação de pesquisa encontrar uma correspondência, o membro **chrgText** da estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retornará o intervalo de posições de caracteres que contém o texto correspondente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ LocalizarTexto**](em-findtext.md)
</dt> </dl>

 

 





