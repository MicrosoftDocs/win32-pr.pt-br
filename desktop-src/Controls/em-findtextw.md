---
title: Mensagem de EM_FINDTEXTW (RichEdit. h)
description: Localiza o texto Unicode dentro de um controle de edição rico.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Controles de EM_FINDTEXTW de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644981"
---
# <a name="em_findtextw-message"></a>\_Mensagem em FINDTEXTW

Localiza o texto Unicode dentro de um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica os parâmetros da operação de pesquisa. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ para baixo**</dt> </dl>                               | Se definido, a operação pesquisa do final da seleção atual até o final do documento. Se não estiver definido, a operação pesquisa do final da seleção atual para o início do documento.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**\_MATCHALEFHAMZA fr**</dt> </dl> | Por padrão, os Alef Arábico e Hebraico com acentos diferentes são todos correspondidos pelo caractere Alef. Defina esse sinalizador se desejar que a pesquisa Diferencie entre os Alef com sotaques diferentes.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**\_MATCHCASE fr**</dt> </dl>                | Se definido, a operação de pesquisa diferencia maiúsculas de minúsculas. Se não for definido, a operação de pesquisa não diferenciará maiúsculas de minúsculas.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Por padrão, as marcas de diacríticos árabe e Hebraico são ignoradas. Defina esse sinalizador se desejar que a operação de pesquisa considere as marcas de sinais diacríticos.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**\_MATCHKASHIDA fr**</dt> </dl>       | Por padrão, os kashidas árabe e Hebraico são ignorados. Defina esse sinalizador se desejar que a operação de pesquisa considere os kashidas.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Se definido, a operação pesquisa apenas palavras inteiras que correspondam à cadeia de caracteres de pesquisa. Se não for definido, a operação também pesquisará fragmentos de palavras que correspondam à cadeia de caracteres de pesquisa.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Uma estrutura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) que contém informações sobre a operação Find.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a cadeia de caracteres de destino for encontrada, o valor de retorno será a posição baseada em zero do primeiro caractere da correspondência. Se o destino não for encontrado, o valor de retorno será-1.

## <a name="remarks"></a>Comentários

**Em \_ FINDTEXTW** usa a estrutura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , enquanto [**em \_ FINDTEXTEXW**](em-findtextexw.md) usa a estrutura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) . A diferença é que o **FINDTEXTEXW** relata o intervalo de texto que foi encontrado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ FINDTEXTEXW**](em-findtextexw.md)
</dt> </dl>

 

 





