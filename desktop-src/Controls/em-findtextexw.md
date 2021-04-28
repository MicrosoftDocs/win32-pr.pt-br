---
title: Mensagem de EM_FINDTEXTEXW (RichEdit. h)
description: Mensagem de EM_FINDTEXTEXW-localiza o texto Unicode dentro de um controle de edição rico.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- Controles de EM_FINDTEXTEXW de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109804"
---
# <a name="em_findtextexw-message"></a>\_Mensagem em FINDTEXTEXW

Localiza o texto Unicode dentro de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o comportamento da operação de pesquisa. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ para baixo**</dt> </dl>                               | Microsoft rich edit 2,0 e posterior: se definido, a pesquisa será encaminhada de **FINDTEXTEX. chrg. cpMin**; Se não estiver definido, a pesquisa será regressiva de **FINDTEXTEX. chrg. cpMin**. <br/> Microsoft Rich Edit 1,0: o \_ sinalizador fr down é ignorado. A pesquisa está sempre em frente.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**\_MATCHALEFHAMZA fr**</dt> </dl> | Se definido, a pesquisa é diferenciada entre os Alef com acentos diferentes. Se não for definido, os Alef Arábico e Hebraico com acentos diferentes serão todos correspondidos pelo caractere Alef. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**\_MATCHCASE fr**</dt> </dl>                | Se definido, a operação de pesquisa diferencia maiúsculas de minúsculas. Se não for definido, a operação de pesquisa não diferenciará maiúsculas de minúsculas.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Se definido, a operação de pesquisa considerará as marcas de sinais diacríticos. Se não estiver definido, as marcas de diacríticos árabe e Hebraico serão ignoradas. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**\_MATCHKASHIDA fr**</dt> </dl>       | Se definido, a operação de pesquisa considerará kashidas. Se não for definido, os kashidas árabe e Hebraico serão ignorados. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa. Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) que contém informações sobre a operação Find.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência. Se o destino não for encontrado, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

Use esta mensagem para localizar cadeias de caracteres Unicode. Para ANSI;, use [**em \_ FINDTEXTEX**](em-findtextex.md).

O membro **cpMin** de **FINDTEXTEX. chrg** sempre especifica o ponto de partida da pesquisa e **cpMax** especifica o ponto de extremidade. Ao pesquisar em retrocesso, **cpMin** deve ser igual ou maior que **cpMax**. Ao pesquisar em frente, um valor de-1 em **cpMax** estende o intervalo de pesquisa até o final do texto.

Se a operação de pesquisa encontrar uma correspondência, o membro **chrgText** da estrutura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retornará o intervalo de posições de caracteres que contém o texto correspondente.

**Em \_ FINDTEXTEXW** usa a estrutura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , enquanto [**em \_ FINDTEXTW**](em-findtextw.md) usa a estrutura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) . A diferença é que **em \_ FINDTEXTEXW** relata o intervalo de texto que foi encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**em \_ FINDTEXTW**](em-findtextw.md)
</dt> </dl>

 

 





